---
title: "Complet4R: Geometric Complete 4D Reconstruction"
title_zh: Complet4R：几何完整四维重建
authors: "Wang, Weibang, Li, Kenan, Chen, Zhuoguang, Yuan, Yijun, Zhao, Hang"
date: 2026
publication_date: 2026
publication_date_precision: year
publication_date_source: conference year only; exact release date unverified
publication_date_kind: unknown
pdf: "https://openaccess.thecvf.com/content/CVPR2026/papers/Wang_Complet4R_Geometric_Complete_4D_Reconstruction_CVPR_2026_paper.pdf"
tags: ["query:dr"]
score: 9.0
evidence: 从视频重建时间一致且几何完整的动态场景
tldr: 以往动态重建方法依赖成对重建或局部运动估计，难以恢复时间一致且几何完整（含遮挡区域）的动态场景几何。本文提出端到端框架Complet4R，将几何完整四维重建形式化为重建与补全的统一任务，用仅解码器Transformer直接从序列视频全局聚合全部上下文，为每个时间戳重建完整几何。实验表明其在自建基准上取得最先进性能，将重建与补全统一，推动了四维动态重建。
source: CVPR-2026-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-wang-complet4r-geometric-complete-4d-reconstruction-cvpr-2026-paper/fig-001.webp\", \"caption\": \"\", \"page\": 1, \"index\": 1, \"width\": 658, \"height\": 323}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-wang-complet4r-geometric-complete-4d-reconstruction-cvpr-2026-paper/fig-002.webp\", \"caption\": \"\", \"page\": 1, \"index\": 2, \"width\": 1022, \"height\": 446}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-wang-complet4r-geometric-complete-4d-reconstruction-cvpr-2026-paper/fig-003.webp\", \"caption\": \"\", \"page\": 1, \"index\": 3, \"width\": 2162, \"height\": 1212}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-wang-complet4r-geometric-complete-4d-reconstruction-cvpr-2026-paper/fig-004.webp\", \"caption\": \"\", \"page\": 3, \"index\": 4, \"width\": 462, \"height\": 278}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-wang-complet4r-geometric-complete-4d-reconstruction-cvpr-2026-paper/fig-005.webp\", \"caption\": \"\", \"page\": 3, \"index\": 5, \"width\": 607, \"height\": 427}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-wang-complet4r-geometric-complete-4d-reconstruction-cvpr-2026-paper/fig-006.webp\", \"caption\": \"\", \"page\": 3, \"index\": 6, \"width\": 502, \"height\": 360}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-wang-complet4r-geometric-complete-4d-reconstruction-cvpr-2026-paper/fig-007.webp\", \"caption\": \"\", \"page\": 7, \"index\": 7, \"width\": 643, \"height\": 410}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-wang-complet4r-geometric-complete-4d-reconstruction-cvpr-2026-paper/fig-008.webp\", \"caption\": \"\", \"page\": 7, \"index\": 8, \"width\": 667, \"height\": 411}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-wang-complet4r-geometric-complete-4d-reconstruction-cvpr-2026-paper/fig-009.webp\", \"caption\": \"\", \"page\": 7, \"index\": 9, \"width\": 497, \"height\": 473}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-wang-complet4r-geometric-complete-4d-reconstruction-cvpr-2026-paper/fig-010.webp\", \"caption\": \"\", \"page\": 7, \"index\": 10, \"width\": 638, \"height\": 446}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-wang-complet4r-geometric-complete-4d-reconstruction-cvpr-2026-paper/fig-011.webp\", \"caption\": \"\", \"page\": 7, \"index\": 11, \"width\": 450, \"height\": 474}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-wang-complet4r-geometric-complete-4d-reconstruction-cvpr-2026-paper/fig-012.webp\", \"caption\": \"\", \"page\": 7, \"index\": 12, \"width\": 705, \"height\": 411}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-wang-complet4r-geometric-complete-4d-reconstruction-cvpr-2026-paper/fig-013.webp\", \"caption\": \"\", \"page\": 7, \"index\": 13, \"width\": 713, \"height\": 388}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-wang-complet4r-geometric-complete-4d-reconstruction-cvpr-2026-paper/fig-014.webp\", \"caption\": \"\", \"page\": 7, \"index\": 14, \"width\": 659, \"height\": 426}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-wang-complet4r-geometric-complete-4d-reconstruction-cvpr-2026-paper/fig-015.webp\", \"caption\": \"\", \"page\": 7, \"index\": 15, \"width\": 996, \"height\": 487}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-wang-complet4r-geometric-complete-4d-reconstruction-cvpr-2026-paper/fig-016.webp\", \"caption\": \"\", \"page\": 8, \"index\": 16, \"width\": 1032, \"height\": 517}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-wang-complet4r-geometric-complete-4d-reconstruction-cvpr-2026-paper/fig-017.webp\", \"caption\": \"\", \"page\": 8, \"index\": 17, \"width\": 942, \"height\": 651}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-wang-complet4r-geometric-complete-4d-reconstruction-cvpr-2026-paper/fig-018.webp\", \"caption\": \"\", \"page\": 8, \"index\": 18, \"width\": 1141, \"height\": 580}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-wang-complet4r-geometric-complete-4d-reconstruction-cvpr-2026-paper/fig-019.webp\", \"caption\": \"\", \"page\": 8, \"index\": 19, \"width\": 1031, \"height\": 546}]"
motivation: 以往方法依赖成对重建或局部运动估计，难以恢复时间一致且几何完整（含遮挡）的动态场景。
method: 提出Complet4R端到端框架，用仅解码器Transformer从序列视频全局聚合上下文，为每个时刻重建完整几何。
result: 在自建基准上取得最先进性能，恢复每个时间戳含遮挡区域的完整几何。
conclusion: 将重建与补全统一，推动几何完整的四维动态重建。
---

## Abstract
We introduce Complet4R, a novel end-to-end framework for Geometric Complete 4D Reconstruction, which aims to recover temporally coherent and geometrically complete reconstruction for dynamic scenes. Our method formalizes the task of Geometric Complete 4D Reconstruction as a unified framework of reconstruction and completion, by directly accumulating full contexts onto each frame. Unlike previous approaches that rely on pairwise reconstruction or local motion estimation, Complet4R utilizes a decoder-only transformer to operate all context globally directly from sequential video input, reconstructing a complete geometry for every single timestamp, including occluded regions visible in other frames. Our method demonstrates the state-of-the-art performance on our proposed benchmark for Geometric Complete 4D Reconstruction and the 3D Point Tracking task. Code will be released to support future research.

---

## 论文详细总结（自动生成）

# Complet4R: Geometric Complete 4D Reconstruction 论文总结

## 1. 核心问题与整体含义
- **研究背景**：传统 SfM/SLAM 面向静态刚性场景，动态物体会破坏刚性假设，常被当作噪声剔除；而动态信息对理解真实世界、构建 4D 世界模型至关重要。
- **核心问题**：现有动态 3D 重建方法多依赖**成对重建**或**局部运动估计**，中间表示仍是帧中心，难以从整个视频序列中蒸馏出全局一致、几何完整的 4D 结构。
- **关键缺口**：单个时刻只能看到场景的一部分，动态物体或静态区域可能在当前帧被遮挡，却在其他帧可见；已有方法通常只重建当前帧可见几何，无法补全遮挡区域。
- **论文含义**：提出新任务 **Geometric Complete 4D Reconstruction**，将“重建”与“补全”统一，为每个时间戳重建包含遮挡区域的完整几何，并保持时间一致性。

## 2. 方法论
### 2.1 核心思想
- 给定 \(N\) 帧连续 RGB 图像和一个目标聚合时间戳 \(a\)，模型聚合所有其他帧 \(\{I_i\}_{i\neq a}\) 的几何线索，推断目标时刻的完整点图 \(P_a\)。
- 与以往“成对匹配/局部运动估计”不同，Complet4R 使用 **decoder-only transformer** 直接全局处理整个序列视频，将所有帧的 3D 点图聚合到目标时间戳。
- 通过轮流将每一帧设为目标时间戳，模型可输出每个时刻的完整几何；这一过程隐含建立点轨迹，因此 **3D 点跟踪可作为重建的副产品**。

### 2.2 架构与流程
- 输入图像被切分为 patch，用 **DINOv2** 提取视觉 token。
- 引入两类特殊 token：
  - **Aggregation tokens**：目标时间戳一组，其他时间戳共享另一组，用于显式标识聚合目标。
  - **Camera tokens 与 registration tokens**：继承 VGGT 思路，编码相机位姿并统一到第一帧坐标系。
- 在 **frame attention** 和 **global attention** 中，目标帧与其余帧的 aggregation tokens 通过自注意力交互，逐步对齐并聚合过去与未来信息。
- 预测头包括：
  - **Camera head**：预测相机参数 \(g_i\)。
  - **Depth head**：预测深度图 \(D_i\)。
  - **Aggregation head**：基于 DPT 风格解码器，预测每帧对齐到目标时间戳的 3D 点图。
- 模型形式化映射为：
  \[
  f((I_i)_{i=0}^{N-1}, a) = (P_a^i, g_i, D_i)_{i=0}^{N-1}
  \]

### 2.3 训练与损失
- 多任务损失：
  \[
  L = \lambda L_{\text{point}} + L_{\text{camera}} + L_{\text{depth}}
  \]
- 提出 **Focal-Weighted Point Loss**：在 VGGT 不确定性加权基础上，加入 focal 风格权重 \(w_i^a = |\beta e_i^a|^\gamma\)，其中 \(e_i^a\) 为预测点与真值点的误差，以增强对高动态、难对齐区域的监督。
- 点损失同时约束点坐标、点坐标梯度以及预测不确定性。
- 训练设置：从 VGGT 初始化，冻结 camera 和 depth heads；用 aggregation head 替换原 point head 并继承参数；AdamW 优化 10 epochs，余弦学习率，峰值 \(1e-5\)，0.5 iteration warmup。
- 输入长边不超过 518 像素，宽高比随机采样于 0.5–3.4，使用颜色抖动、高斯模糊、灰度化等增强。

## 3. 实验设计
### 3.1 4D 完整重建
- **数据集/benchmark**：从 SAIL-VOS 3D 验证集选取 44 个序列构成 **SAIL-VOS 3D-test**，作为提出的 Complet4R-benchmark。
- **指标**：Accuracy、Completion、Normal Consistency，均报告 Mean 和 Median；评估协议参考 CUT3R，点随机下采样。
- **对比方法**：由于任务新颖，无直接可用方法；主要对比 **St4RTrack-seq** 和 **St4RTrack-pairs**，需对每帧锚定后聚合跟踪结果。
- **结果**：Complet4R 在所有指标上领先。Accuracy Mean 从约 0.92 降至 0.50，Completion Mean 从 2.67/3.10 降至 0.26，Normal Consistency 保持或略优。论文称 Accuracy 相对提升近 50%，Completion 均值有数量级提升。

### 3.2 3D 点跟踪
- **数据集**：使用 St4RTrack 发布的 **WorldTrack**，构建自 Aerial Digital Twin、Panoptic Studio，并经 TAPVid-3D，增强 PointOdyssey 和 DynamicReplica。
- **指标**：APD 和 EPE，APD 使用四个 3D 阈值 \(\{0.1,0.3,0.5,1.0\}\) 米。
- **对比方法**：SpaTracker、MonST3R、St4RTrack，以及 SpaTracker+RANSAC-Procrustes、SpaTracker+MonST3R 等组合。
- **结果**：Complet4R 在 PO、
