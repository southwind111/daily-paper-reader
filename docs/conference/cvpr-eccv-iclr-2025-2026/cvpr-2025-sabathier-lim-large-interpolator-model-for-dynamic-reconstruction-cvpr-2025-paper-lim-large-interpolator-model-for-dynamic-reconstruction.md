---
title: "LIM: Large Interpolator Model for Dynamic Reconstruction"
title_zh: LIM：用于动态重建的大型插值模型
authors: "Sabathier, Remy, Mitra, Niloy J., Novotny, David"
date: 2025
publication_date: 2025
publication_date_precision: year
publication_date_source: conference year only; exact release date unverified
publication_date_kind: unknown
pdf: "https://openaccess.thecvf.com/content/CVPR2025/papers/Sabathier_LIM_Large_Interpolator_Model_for_Dynamic_Reconstruction_CVPR_2025_paper.pdf"
tags: ["query:dr"]
score: 9.0
evidence: 基于Transformer的前馈模型在时间上插值隐式三维表示以进行四维重建
tldr: 从视频数据重建动态资产是视觉与图形学的核心任务，但现有四维重建方法受限于类别专用模型或缓慢的优化流程。本文提出大插值模型LIM，这是一种基于Transformer的前馈方案，借助新的因果一致性损失在时间维度上插值隐式三维表示。给定t0与t1时刻的隐式表示，LIM能在数秒内生成任意连续时刻的高质量形变形状，并支持显式网格跟踪生成一致的UV纹理网格序列，为动态重建提供了高效通用的途径。
source: CVPR-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-sabathier-lim-large-interpolator-model-for-dynamic-reconstruction-cvpr-2025-paper/fig-001.webp\", \"caption\": \"\", \"page\": 3, \"index\": 1, \"width\": 12040, \"height\": 3310}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-sabathier-lim-large-interpolator-model-for-dynamic-reconstruction-cvpr-2025-paper/fig-002.webp\", \"caption\": \"\", \"page\": 6, \"index\": 2, \"width\": 2882, \"height\": 1142}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-sabathier-lim-large-interpolator-model-for-dynamic-reconstruction-cvpr-2025-paper/fig-003.webp\", \"caption\": \"\", \"page\": 7, \"index\": 3, \"width\": 3731, \"height\": 2298}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-sabathier-lim-large-interpolator-model-for-dynamic-reconstruction-cvpr-2025-paper/fig-004.webp\", \"caption\": \"\", \"page\": 8, \"index\": 4, \"width\": 2928, \"height\": 1082}]"
motivation: 现有四维重建方法受限于类别专用模型或缓慢的优化过程。
method: 提出基于Transformer的前馈大插值模型LIM，配以因果一致性损失，在时间上插值隐式三维表示。
result: 可在秒级生成任意连续时刻的形变形状，并支持显式网格跟踪与UV纹理网格序列。
conclusion: 为动态资产重建提供了快速通用的前馈式解决方案。
---

## Abstract
Reconstructing dynamic assets from video data is central to many in computer vision and graphics tasks. Existing 4D reconstruction approaches are limited by category-specific models or slow optimization-based methods. Inspired by the recent Large Reconstruction Model (LRM), we present the Large Interpolation Model (LIM), a transformer-based feed-forward solution, guided by a novel causal consistency loss, for interpolating implicit 3D representations across time. Given implicit 3D representations at times t_0 and t_1, LIM produces a deformed shape at any continuous time t\in[t_0,t_1] delivering high-quality interpolations in seconds (per frame).Furthermore, LIM allows explicit mesh tracking across time, producing a consistently uv-textured mesh sequence ready for integration into existing production pipelines. We also use LIM, in conjunction with a diffusion-based multiview generator, to produce dynamic 4D reconstructions from monocular videos. We evaluate LIM on various dynamic datasets, benchmarking against image-space interpolation methods (e.g., FiLM) and direct triplane linear interpolation, and demonstrate clear advantages. In summary, LIM is the first feed-forward model capable of high-speed tracked 4D asset reconstruction across diverse categories.

---

## 论文详细总结（自动生成）

# LIM 论文中文总结

## 1. 核心问题与整体含义
- **研究背景**：从视频数据重建动态 4D 资产是计算机视觉与图形学的重要问题，广泛用于 VR/AR、游戏、影视等。
- **现有局限**：
  - 类别专用方法通常只适用于人体、宠物等特定类别。
  - 优化式 4D 重建方法速度慢，往往需要分钟到小时级。
  - 已有前馈 4D 方法如 L4GM 只能重建关键帧，难以连续时间插值，也难以追踪网格形变。
- **核心问题**：能否像静态重建中的 LRM 一样，构建一个前馈模型，在时间维度上连续插值 3D 隐式表示，并输出可追踪、固定拓扑与 UV 纹理的动态网格。
- **整体含义**：论文提出 **LIM（Large Interpolator Model）**，将 LRM 从静态 3D 重建扩展到动态 4D 重建，首次实现跨类别、高速、可追踪的前馈 4D 资产重建，适合接入现有生产管线。

## 2. 方法论
### 2.1 核心思想
- 基于多视图 LRM，输入两个关键帧时刻 \(t_0\)、\(t_1\) 的隐式 3D 表示，输出任意连续时间 \(t \in [t_0,t_1]\) 的插值 triplane。
- LIM 是一个基于 Transformer 的前馈插值器，不依赖逐场景优化。
- 通过新颖的 **因果一致性损失**，使模型在只有离散关键帧监督时，仍能学习连续时间插值。

### 2.2 关键技术细节
- **基础 LRM**：
  - 多视图 LRM 输入 \(N_{src}\) 张源图像及相机参数，像素与 Plücker 射线坐标拼接后送入 DinoV2，得到图像 token。
  - 12 层 Transformer 通过 cross-attention 将固定 shape token 精炼为 triplane 表示。
  - 训练损失包括光度损失、深度损失和 mask 损失，使用 Adam，学习率 \(10^{-4}\)。
- **LIM 架构**：
  - 从 LRM 最后 \(L=6\) 个 Transformer block 提取中间特征 \(F_k\)。
  - 将插值时间 \(\alpha\) 的位置编码广播并拼接到 \(F_k\)。
  - 通过 cross-attention 与下一关键帧 \(I_{k+1}\) 的图像 token 交互，预测插值 triplane \(\hat{T}_{k+\alpha}\)。
  - 形式化：\(\hat{T}_{k+\alpha} := LIM_{\psi}(F_k(I_k,\Pi_k), I_{k+1}, \alpha)\)。
- **训练监督**：
  - 采样源关键帧 \(k_{src}\)、目标关键帧 \(k_{tgt}\)，间隔为 2、3 或 4。
  - 再采样中间关键帧 \(k_m\)，令 \(\alpha_m=(k_m-k_{src})/(k_{tgt}-k_{src})\)。
  - 用 LRM 在 \(k_m\) 输出的 triplane 作为伪 GT，使用 MSE 损失：
    \[
    L_T = \|\hat{T}_{k_{src}+\alpha_m} - T_{k_m}\|^2
    \]
- **因果一致性损失**：
  - 强制“直接插值到 \(k_{src}+\delta\)”与“先插值到 \(k_{src}+\alpha_{rand}\)，再继续插值到 \(k_{src}+\delta\)”保持一致。
  - 公式含义：
    \[
    L_{causal} = \| LIM(\hat{F}_{k_{src}+\alpha_{rand}}, I_{k_{src}+\delta}, \frac{\delta-\alpha_{rand}}{1-\alpha_{rand}}) - \hat{T}_{k_{src}+\delta} \|^2
    \]
  - 第二段插值使用 LIM 自身中间特征，而非 LRM 特征，使模型可递归式连续插值。
  - 总损失为 \(L_T + L_{causal}\)，训练时冻结 LRM 权重。

### 2.3 网格追踪与单目 4D 重建
- **Canonical 坐标扩展**：
  - 额外训练一个 LRM，使其预测支持体函数 \(f:\mathbb{R}^3 \rightarrow \mathbb{R}^3\) 的 triplane，将 3D 点映射到物体 canonical surface coordinate。
  - canonical 坐标通常取源时刻 \(k_{src}\) 的表面 XYZ。
  - 对应损失为 \(L_{can}\)，并同样使用深度和 mask 监督。
  - 类似地训练 LIM 以插值 canonical-coordinate triplane。
- **网格追踪流程**：
  - 从源时刻 triplane 渲染深度，反投影得到多视图 canonical 坐标。
  - 用 LIM 在时间上密集插值 canonical-coordinate triplane。
  - 对第一个 triplane 跑 Marching Cubes 得到初始网格。
  - 后续时刻通过 canonical 坐标最近邻匹配更新顶点，保持面片拓扑与 UV 纹理不变。
  - 输出：时间相关顶点形变 + 时间不变拓扑与纹理的网格序列。
- **单目视频 4D 重建**：
  - 用预训练扩散模型从单目视频生成 3 个额外视角。
  - 奇数关键帧用 LRM 重建，偶数中间帧用 LIM 插值。
  - 避免对每个 4D 资产从头优化。

## 3. 实验设计
- **数据集 / 场景**：
  - 使用大量艺术家创建、带运动动画的 3D 网格数据集，类似 Objaverse。
  - 训练 LRM 和 LIM 均基于渲染多视图图像、深度和 mask。
  - 评估使用 heldout
