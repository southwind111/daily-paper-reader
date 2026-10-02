---
title: "MoRe: Motion-aware Feed-forward 4D Reconstruction Transformer"
title_zh: MoRe：运动感知的前馈4D重建Transformer
authors: "Fang, Juntong, Chen, Zequn, Zhang, Weiqi, Di, Donglin, Zhang, Xuancheng, Yang, Chengmin, Liu, Yu-Shen"
date: 2026
publication_date: 2026
publication_date_precision: year
publication_date_source: conference year only; exact release date unverified
publication_date_kind: unknown
pdf: "https://openaccess.thecvf.com/content/CVPR2026/papers/Fang_MoRe_Motion-aware_Feed-forward_4D_Reconstruction_Transformer_CVPR_2026_paper.pdf"
tags: ["query:dr"]
score: 10.0
evidence: 前馈4D重建，从单目视频恢复动态场景
tldr: 针对动态4D场景中运动物体破坏相机位姿估计、现有优化方法计算昂贵难以实时的问题，本文提出MoRe前馈4D重建网络。它基于强静态重建骨干，采用注意力强制策略解耦动态运动与静态结构，并结合分组因果注意力与大规模动静态数据微调。实验表明该方法能高效地从单目视频恢复动态3D场景，显著提升鲁棒性与速度，为实时4D重建提供可行方案。
source: CVPR-2026-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-fang-more-motion-aware-feed-forward-4d-reconstruction-transformer-cvpr-2026-paper/fig-001.webp\", \"caption\": \"\", \"page\": 1, \"index\": 1, \"width\": 511, \"height\": 292}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-fang-more-motion-aware-feed-forward-4d-reconstruction-transformer-cvpr-2026-paper/fig-002.webp\", \"caption\": \"\", \"page\": 1, \"index\": 2, \"width\": 520, \"height\": 292}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-fang-more-motion-aware-feed-forward-4d-reconstruction-transformer-cvpr-2026-paper/fig-003.webp\", \"caption\": \"\", \"page\": 1, \"index\": 3, \"width\": 520, \"height\": 292}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-fang-more-motion-aware-feed-forward-4d-reconstruction-transformer-cvpr-2026-paper/fig-004.webp\", \"caption\": \"\", \"page\": 1, \"index\": 4, \"width\": 520, \"height\": 292}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-fang-more-motion-aware-feed-forward-4d-reconstruction-transformer-cvpr-2026-paper/fig-005.webp\", \"caption\": \"\", \"page\": 1, \"index\": 5, \"width\": 520, \"height\": 292}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-fang-more-motion-aware-feed-forward-4d-reconstruction-transformer-cvpr-2026-paper/fig-006.webp\", \"caption\": \"\", \"page\": 1, \"index\": 6, \"width\": 515, \"height\": 294}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-fang-more-motion-aware-feed-forward-4d-reconstruction-transformer-cvpr-2026-paper/fig-007.webp\", \"caption\": \"\", \"page\": 1, \"index\": 7, \"width\": 520, \"height\": 292}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-fang-more-motion-aware-feed-forward-4d-reconstruction-transformer-cvpr-2026-paper/fig-008.webp\", \"caption\": \"\", \"page\": 1, \"index\": 8, \"width\": 511, \"height\": 287}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-fang-more-motion-aware-feed-forward-4d-reconstruction-transformer-cvpr-2026-paper/fig-009.webp\", \"caption\": \"\", \"page\": 1, \"index\": 9, \"width\": 520, \"height\": 292}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-fang-more-motion-aware-feed-forward-4d-reconstruction-transformer-cvpr-2026-paper/fig-010.webp\", \"caption\": \"\", \"page\": 1, \"index\": 10, \"width\": 861, \"height\": 447}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-fang-more-motion-aware-feed-forward-4d-reconstruction-transformer-cvpr-2026-paper/fig-011.webp\", \"caption\": \"\", \"page\": 4, \"index\": 11, \"width\": 912, \"height\": 643}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-fang-more-motion-aware-feed-forward-4d-reconstruction-transformer-cvpr-2026-paper/fig-012.webp\", \"caption\": \"\", \"page\": 4, \"index\": 12, \"width\": 1215, \"height\": 856}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-fang-more-motion-aware-feed-forward-4d-reconstruction-transformer-cvpr-2026-paper/fig-013.webp\", \"caption\": \"\", \"page\": 6, \"index\": 13, \"width\": 753, \"height\": 530}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-fang-more-motion-aware-feed-forward-4d-reconstruction-transformer-cvpr-2026-paper/fig-014.webp\", \"caption\": \"\", \"page\": 6, \"index\": 14, \"width\": 1128, \"height\": 794}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-fang-more-motion-aware-feed-forward-4d-reconstruction-transformer-cvpr-2026-paper/fig-015.webp\", \"caption\": \"\", \"page\": 6, \"index\": 15, \"width\": 1057, \"height\": 743}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-fang-more-motion-aware-feed-forward-4d-reconstruction-transformer-cvpr-2026-paper/fig-016.webp\", \"caption\": \"\", \"page\": 6, \"index\": 16, \"width\": 756, \"height\": 436}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-fang-more-motion-aware-feed-forward-4d-reconstruction-transformer-cvpr-2026-paper/fig-017.webp\", \"caption\": \"\", \"page\": 6, \"index\": 17, \"width\": 1143, \"height\": 677}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-fang-more-motion-aware-feed-forward-4d-reconstruction-transformer-cvpr-2026-paper/fig-018.webp\", \"caption\": \"\", \"page\": 6, \"index\": 18, \"width\": 753, \"height\": 530}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-fang-more-motion-aware-feed-forward-4d-reconstruction-transformer-cvpr-2026-paper/fig-019.webp\", \"caption\": \"\", \"page\": 6, \"index\": 19, \"width\": 1128, \"height\": 794}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-fang-more-motion-aware-feed-forward-4d-reconstruction-transformer-cvpr-2026-paper/fig-020.webp\", \"caption\": \"\", \"page\": 6, \"index\": 20, \"width\": 1215, \"height\": 855}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-fang-more-motion-aware-feed-forward-4d-reconstruction-transformer-cvpr-2026-paper/fig-021.webp\", \"caption\": \"\", \"page\": 6, \"index\": 21, \"width\": 1357, \"height\": 608}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-fang-more-motion-aware-feed-forward-4d-reconstruction-transformer-cvpr-2026-paper/fig-022.webp\", \"caption\": \"\", \"page\": 6, \"index\": 22, \"width\": 866, \"height\": 514}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-fang-more-motion-aware-feed-forward-4d-reconstruction-transformer-cvpr-2026-paper/fig-023.webp\", \"caption\": \"\", \"page\": 6, \"index\": 23, \"width\": 910, \"height\": 539}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-fang-more-motion-aware-feed-forward-4d-reconstruction-transformer-cvpr-2026-paper/fig-024.webp\", \"caption\": \"\", \"page\": 6, \"index\": 24, \"width\": 910, \"height\": 539}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-fang-more-motion-aware-feed-forward-4d-reconstruction-transformer-cvpr-2026-paper/fig-025.webp\", \"caption\": \"\", \"page\": 7, \"index\": 25, \"width\": 1215, \"height\": 863}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-fang-more-motion-aware-feed-forward-4d-reconstruction-transformer-cvpr-2026-paper/fig-026.webp\", \"caption\": \"\", \"page\": 7, \"index\": 26, \"width\": 519, \"height\": 325}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-fang-more-motion-aware-feed-forward-4d-reconstruction-transformer-cvpr-2026-paper/fig-027.webp\", \"caption\": \"\", \"page\": 7, \"index\": 27, \"width\": 519, \"height\": 325}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-fang-more-motion-aware-feed-forward-4d-reconstruction-transformer-cvpr-2026-paper/fig-028.webp\", \"caption\": \"\", \"page\": 7, \"index\": 28, \"width\": 732, \"height\": 520}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-fang-more-motion-aware-feed-forward-4d-reconstruction-transformer-cvpr-2026-paper/fig-029.webp\", \"caption\": \"\", \"page\": 7, \"index\": 29, \"width\": 865, \"height\": 614}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-fang-more-motion-aware-feed-forward-4d-reconstruction-transformer-cvpr-2026-paper/fig-030.webp\", \"caption\": \"\", \"page\": 7, \"index\": 30, \"width\": 865, \"height\": 614}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-fang-more-motion-aware-feed-forward-4d-reconstruction-transformer-cvpr-2026-paper/fig-031.webp\", \"caption\": \"\", \"page\": 7, \"index\": 31, \"width\": 820, \"height\": 582}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-fang-more-motion-aware-feed-forward-4d-reconstruction-transformer-cvpr-2026-paper/fig-032.webp\", \"caption\": \"\", \"page\": 7, \"index\": 32, \"width\": 1215, \"height\": 863}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-fang-more-motion-aware-feed-forward-4d-reconstruction-transformer-cvpr-2026-paper/fig-033.webp\", \"caption\": \"\", \"page\": 7, \"index\": 33, \"width\": 1215, \"height\": 863}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-fang-more-motion-aware-feed-forward-4d-reconstruction-transformer-cvpr-2026-paper/fig-034.webp\", \"caption\": \"\", \"page\": 7, \"index\": 34, \"width\": 1024, \"height\": 727}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-fang-more-motion-aware-feed-forward-4d-reconstruction-transformer-cvpr-2026-paper/fig-035.webp\", \"caption\": \"\", \"page\": 7, \"index\": 35, \"width\": 1024, \"height\": 727}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-fang-more-motion-aware-feed-forward-4d-reconstruction-transformer-cvpr-2026-paper/fig-036.webp\", \"caption\": \"\", \"page\": 7, \"index\": 36, \"width\": 1215, \"height\": 863}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-fang-more-motion-aware-feed-forward-4d-reconstruction-transformer-cvpr-2026-paper/fig-037.webp\", \"caption\": \"\", \"page\": 7, \"index\": 37, \"width\": 885, \"height\": 629}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-fang-more-motion-aware-feed-forward-4d-reconstruction-transformer-cvpr-2026-paper/fig-038.webp\", \"caption\": \"\", \"page\": 7, \"index\": 38, \"width\": 1215, \"height\": 863}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-fang-more-motion-aware-feed-forward-4d-reconstruction-transformer-cvpr-2026-paper/fig-039.webp\", \"caption\": \"\", \"page\": 7, \"index\": 39, \"width\": 1215, \"height\": 863}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-fang-more-motion-aware-feed-forward-4d-reconstruction-transformer-cvpr-2026-paper/fig-040.webp\", \"caption\": \"\", \"page\": 7, \"index\": 40, \"width\": 1215, \"height\": 863}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-fang-more-motion-aware-feed-forward-4d-reconstruction-transformer-cvpr-2026-paper/fig-041.webp\", \"caption\": \"\", \"page\": 7, \"index\": 41, \"width\": 1215, \"height\": 863}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-fang-more-motion-aware-feed-forward-4d-reconstruction-transformer-cvpr-2026-paper/fig-042.webp\", \"caption\": \"\", \"page\": 7, \"index\": 42, \"width\": 1215, \"height\": 863}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-fang-more-motion-aware-feed-forward-4d-reconstruction-transformer-cvpr-2026-paper/fig-043.webp\", \"caption\": \"\", \"page\": 7, \"index\": 43, \"width\": 1215, \"height\": 863}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-fang-more-motion-aware-feed-forward-4d-reconstruction-transformer-cvpr-2026-paper/fig-044.webp\", \"caption\": \"\", \"page\": 7, \"index\": 44, \"width\": 1215, \"height\": 863}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-fang-more-motion-aware-feed-forward-4d-reconstruction-transformer-cvpr-2026-paper/fig-045.webp\", \"caption\": \"\", \"page\": 7, \"index\": 45, \"width\": 732, \"height\": 520}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-fang-more-motion-aware-feed-forward-4d-reconstruction-transformer-cvpr-2026-paper/fig-046.webp\", \"caption\": \"\", \"page\": 7, \"index\": 46, \"width\": 1215, \"height\": 863}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-fang-more-motion-aware-feed-forward-4d-reconstruction-transformer-cvpr-2026-paper/fig-047.webp\", \"caption\": \"\", \"page\": 7, \"index\": 47, \"width\": 1215, \"height\": 863}]"
motivation: 动态4D场景重建常因运动物体破坏相机位姿估计，而现有优化方法依赖额外监督且计算昂贵，难以实时应用。
method: 提出MoRe前馈4D重建网络，基于静态重建骨干，用注意力强制策略解耦动态运动与静态结构，并引入分组因果注意力。
result: 在大规模动静态混合数据上微调后，模型能高效地从单目视频恢复动态3D场景，兼顾鲁棒性与效率。
conclusion: 该工作表明前馈式注意力解耦可替代昂贵的逐场景优化，为实时动态4D重建提供新思路。
---

## Abstract
Reconstructing dynamic 4D scenes remains challenging due to the presence of moving objects that corrupt camera pose estimation. Existing optimization methods alleviate this issue with additional supervision, but they are mostly computationally expensive and impractical in real-time applications. To address these limitations, we propose MoRe, a feedforward 4D reconstruction network that efficiently recovers dynamic 3D scenes from monocular videos. Built upon a strong static reconstruction backbone, MoRe employs an attention-forcing strategy to disentangle dynamic motion from static structure. To further enhance robustness, we fine-tune the model on large-scale, diverse datasets encompassing both dynamic and static scenes. Moreover, our grouped causal attention captures temporal dependencies and adapts to varying token lengths across frames, ensuring temporally coherent geometry reconstruction. Extensive experiments on multiple benchmarks demonstrate that MoRe achieves high-quality dynamic reconstructions with exceptional efficiency.

---

## 论文详细总结（自动生成）

# MoRe：运动感知的前馈4D重建Transformer——论文总结

## 1. 核心问题与整体含义

- **研究动机**：动态4D场景重建（从单目视频中恢复随时间演化的3D结构）在AR、机器人、数字孪生等领域日益重要。然而，场景中的**运动物体会严重破坏相机位姿估计**，导致几何结构重建失真。
- **现有方法的困境**：
  - 传统几何方法（SfM/MVS、SLAM）假设环境基本静态，面对物体形变、运动或复杂相机运动时失效。
  - 基于学习的实时前馈模型（如VGGT、Dust3R）虽速度快，但**主要在静态场景上训练**，动态物体或大范围相机运动下精度显著下降。
  - 混合优化管线（如MegaSaM、Uni4D）虽对动态场景更鲁棒，但依赖多阶段结构或迭代精化，**计算成本高**，难以处理长序列或流式视频。
- **核心空白**：如何设计一个**快速、可泛化**的前馈框架，在流式/长序列输入下同时处理相机与物体运动，并输出精确的位姿与深度用于点云重建。
- **整体含义**：MoRe旨在**不引入推理时显式运动先验**的前提下，通过训练阶段教会模型区分动态物体与静态背景，实现运动感知的4D流式重建。

## 2. 方法论

### 2.1 核心思想

- 基于强静态重建骨干网络（VGGT），引入**注意力强制（Attention-Forcing）策略**，在训练阶段显式监督相机token的注意力分布，使其聚焦于静态区域、抑制动态区域。
- 结合**分组因果注意力（Grouped Causal Attention）**与**类BA的token聚合机制**，实现高效的流式推理与全局几何一致性精化。

### 2.2 问题形式化

给定单目视频帧序列 $\{I_t \in \mathbb{R}^{3 \times H \times W}\}_{t=1}^T$，目标是联合估计：
- 每帧深度 $\{D_t\}$
- 相机参数 $\{g_t \in \mathbb{R}^9\}$
- 动态点图 $\{P_t \in \mathbb{R}^{3 \times H \times W}\}$
- 运动掩码 $\{M_t\}$（仅训练时使用，推理时不需要）

流式形式化：$\{D_t, g_t, P_t, M_t\} = f_\theta(\{C_t\}_{t=1}^{T-1}, I_{T-1})$，其中 $C_t$ 为帧 $I_t$ 的缓存信息。

### 2.3 关键技术细节

**（1）运动对齐注意力（Motion-Aligned Attention）**

- **动机观察**：VGGT的相机token在动态场景中注意力分布趋于均匀，表明运动物体干扰了相机估计。
- **实现方式**：
  - 将真值运动掩码 $M_t$ 划分为 $s \times s$ 的patch，与图像tokenization一致。
  - 计算每个图像token的运动分数：$a_i = 1 - \frac{1}{s^2}\sum_{(u,v)\in m_i} m_i(u,v)$，$a_i \in [0,1]$，值越高表示越静态。
  - 将 $a_i$ 作为软监督信号，调制相机token的注意力权重 $\alpha_i$，损失函数为 $L_{attn} = \frac{1}{M}\sum_{i=1}^M \max(0, a_i - C) \cdot \alpha_i$。
- **关键优势**：**完全test-time-free**，推理时无需运动掩码或额外计算。

**（2）分组因果注意力（Grouped Causal Attention）**

- 传统因果注意力将token视为扁平序列，破坏帧内空间一致性。
- MoRe采用**帧级因果掩码**：帧间保持时间因果性，帧内允许双向注意力，兼顾时序推理与空间一致性。
- 流式推理时，首对图像初始化KV缓存，后续帧通过因果注意力处理：$F_t = \text{Attn}(Q_t, [K_{1:t-1}, K_t], [V_{1:t-1}, V_t])$。

**（3）类BA的Token聚合精化**

- 严格因果注意力限制长程全局信息交换，导致长序列中位姿精度下降。
- 推理结束后，缓存所有相机query $Q_t^{cam}$，对全部帧的KV特征做额外注意力：$C_t^{opt} = \text{Attn}(Q_t^{cam}, [K_{1:T}], [V_{1:T}])$。
- 类似BA优化步骤，以轻量级后处理恢复全局几何一致性。

### 2.4 训练目标

- **深度/点图回归**：置信度加权损失 $L_{conf} = \sum_{i=1}^N (\hat{c}_i \|\hat{y}_i - y_i\|_2^2 - \lambda \log(\hat{c}_i))$。
- **运动掩码**：标准BCE损失 $L_{motion}$。
- **注意力对齐**：$L_{attn}$ 如上述。
- **相机位姿**：相对位姿监督 $L_{cam} = \frac{1}{T(T-1)}\sum_{i\neq j}(\theta_{\hat{R}_{i\to j}, R_{i\to j}} + \|\hat{t}_{i\to j} - t_{i\to j}\|)$。
- **双路径监督**：训练时复制相机token并移至序列末尾，同时监督流式路径与后处理聚合路径；原始token梯度截断，复制token保留完整梯度流。

## 3. 实验设计

### 3.1 训练数据集

- 大规模、多样化集合，涵盖静态与动态场景：
  - **动态**：Dynamic Replica、PointOdyssey、Spring、Virtual KITTI、TartanAir、OmniWorld-Game
  - **静态**：Co3Dv2、ScanNet、BlendedMVS、Hypersim、ARKitScenes、Waymo
- 少序列数据集按比例重复以平衡分布。

### 3.2 评估Benchmark

| 任务 | 数据集 | 指标 |
|------|--------|------|
| 相机位姿估计 | Sintel、TUM-dynamics、Bonn、ScanNet | ATE↓、RPE trans↓、RPE rot↓ |
| 视频深度估计 | Sintel、Bonn、TUM-dynamics、KITTI | Abs Rel↓、δ<1.25↑ |

- 前三个动态数据集**训练时未见过**，验证零样本泛化能力；ScanNet为静态数据集，验证静态重建能力。
- 位姿评估后Sim(3)对齐，深度评估仅做scale-only对齐。

### 3.3 对比方法

- **全注意力（FA）方法**：MapAnything、VGGT、Flare、π3
- **流式方法**：Spann3R、CUT3R、StreamVGGT、Wint3R、Stream3R
- 对比包括定量表格与定性可视化（图6、图7）。

### 3.4 消融实验

- **注意力强制**：有无attention forcing对比（Sintel、TUM-dynamics）
- **分组因果注意力**：GCA vs 标准因果注意力（Sintel、Bonn、KITTI）
- **类BA精化**：有无duplicated camera token后处理（Sintel、TUM-dynamics）

## 4. 资源与算力

- **论文文本中未明确提及**所使用的GPU型号、数量、训练时长、参数量等算力信息。
- 仅在方法部分提到基于VGGT骨干，训练采用大规模数据集端到端进行，但具体硬件配置与训练开销未披露。
- **这一点属于论文信息透明度的不足**，读者无法据此评估方法的实际训练成本与可复现性。

## 5. 实验数量与充分性

- **实验组数概览**：
  - 相机位姿估计：4个数据集 × 3个指标，对比9种方法（含FA与Streaming两类）
  - 视频深度估计：4个数据集 × 2个指标，对比8种方法
  - 消融实验：3组（注意力强制、GCA、BA精化），覆盖2-3个数据集
  - 定性对比：2组（全注意力模型 vs 其他；流式模型 vs 其他）
- **充分性评价**：
  - **优点**：覆盖动态与静态、合成与真实、室内与室外多种场景；零样本泛化验证有说服力；消融实验针对性强。
  - **不足**：
    - 消融实验仅在部分数据集上进行，未全面覆盖所有benchmark。
    - 未报告推理速度/内存占用的定量数据（虽强调高效，但缺乏具体吞吐量、延迟对比表）。
    - 未与π3进行完整定量对比（文中仅提及"comparable"但未列表）。
    - 缺少失败案例分析或边界条件讨论。
  - **公平性**：消融实验保持相同架构、训练计划与数据配置，对比公平；但不同方法间的训练数据规模差异未被充分控制（文中承认MoRe训练数据少于π3）。

## 6. 主要结论与发现

- MoRe在动态场景相机位姿估计上**显著优于所有流式方法**，在Sintel上ATE达0.1474（Streaming）与0.0877（FA），大幅领先CUT3R、StreamVGGT等。
- 在全注意力方法中，MoRe与SOTA的π3性能相当，但**训练数据量显著更少**。
- 视频深度估计中，MoRe在流式方法中表现最佳，Sintel Abs Rel低至0.254，KITTI δ<1.25达0.966。
- **注意力强制策略**有效引导模型解耦动态运动与静态结构，显著提升位姿精度。
- **分组因果注意力**在保持时间因果性的同时维护帧内空间一致性，持续提升深度估计性能。
- **类BA精化**通过复制相机token的全局注意力后处理，有效改善流式重建的位姿精度与时间一致性。
- 整体而言，MoRe在**精度与效率之间取得良好平衡**，适合实时/流式4D重建。

## 7. 优点

- **方法设计优雅**：注意力强制策略完全test-time-free，推理时无需运动掩码或额外模块，保持了前馈架构的简洁性。
- **训练与推理解耦**：通过训练阶段显式监督实现运动感知，避免推理时的额外开销，适合流式/实时场景。
- **流式推理机制创新**：帧级因果掩码兼顾时序因果与空间一致性；类BA token聚合以轻量后处理弥补因果注意力的长程信息局限。
- **双路径监督策略**：同时监督流式路径与聚合路径，保证两条路径预测一致性，设计巧妙。
- **实验覆盖全面**：训练数据涵盖12个数据集，评估覆盖4个位姿+4个深度benchmark，零样本泛化验证有说服力。
- **定性结果丰富**：多组可视化对比展示真实场景下的重建质量与鲁棒性。

## 8. 不足与局限

- **算力信息缺失**：未报告GPU型号、数量、训练时长、参数量等，影响可复现性与成本评估。
- **推理效率缺乏定量验证**：虽强调"高效""实时"，但未提供FPS、延迟、内存占用等具体数据，也未与流式方法进行速度对比表。
- **消融实验覆盖有限**：仅3组消融，且未在所有benchmark上验证；未分析运动掩码质量对性能的影响。
- **对比公平性存疑**：与π3的对比未完整列表；不同方法训练数据规模差异大，可能影响结论的公平性。
- **应用限制**：
  - 依赖训练时真值运动掩码，若训练数据运动标注质量差，可能影响解耦效果。
  - 类BA精化需缓存全部帧的KV特征，长序列下内存开销可能成为瓶颈（文中未讨论）。
  - 仅在单目视频上验证，未扩展至多目或RGB-D输入。
- **失败案例与边界条件未讨论**：缺少对极端动态、遮挡、快速运动等困难场景的失败分析。
- **与同期工作对比不完整**：部分引用（如Spann3R、π3）的对比细节有限。

（完）
