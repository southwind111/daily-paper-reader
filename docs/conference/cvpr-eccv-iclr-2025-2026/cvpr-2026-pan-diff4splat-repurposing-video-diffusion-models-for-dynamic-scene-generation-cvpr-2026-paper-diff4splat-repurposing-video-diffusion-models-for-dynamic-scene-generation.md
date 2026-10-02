---
title: "Diff4Splat: Repurposing Video Diffusion Models for Dynamic Scene Generation"
title_zh: Diff4Splat：复用视频扩散模型进行动态场景生成
authors: "Pan, Panwang, Lin, Chenguo, Li, Chenxin, Zhao, Jingjing, Lin, Yuchen, Li, Haopeng, Lin, Yunlong, Wen, Kairun, Yuan, Yixuan, MU, Yadong"
date: 2026
publication_date: 2026
publication_date_precision: year
publication_date_source: conference year only; exact release date unverified
publication_date_kind: unknown
pdf: "https://openaccess.thecvf.com/content/CVPR2026/papers/Pan_Diff4Splat_Repurposing_Video_Diffusion_Models_for_Dynamic_Scene_Generation_CVPR_2026_paper.pdf"
tags: ["query:dr"]
score: 7.0
evidence: 动态场景生成，预测可变形三维高斯场与运动
tldr: 从单张图像生成动态场景通常依赖测试时优化或后处理，难以一次性建模外观、几何与运动。本文提出Diff4Splat前馈框架，复用视频扩散模型的生成先验，并结合大规模4D数据学到的几何与运动约束，直接预测可变形三维高斯场。该方法在单次前向中同时捕获外观、几何与运动，无需测试时优化，为四维动态场景生成提供了高效的一体化方案。
source: CVPR-2026-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-pan-diff4splat-repurposing-video-diffusion-models-for-dynamic-scene-generation-cvpr-2026-paper/fig-001.webp\", \"caption\": \"\", \"page\": 2, \"index\": 1, \"width\": 6837, \"height\": 3897}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-pan-diff4splat-repurposing-video-diffusion-models-for-dynamic-scene-generation-cvpr-2026-paper/fig-002.webp\", \"caption\": \"\", \"page\": 5, \"index\": 2, \"width\": 11462, \"height\": 3899}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-pan-diff4splat-repurposing-video-diffusion-models-for-dynamic-scene-generation-cvpr-2026-paper/fig-003.webp\", \"caption\": \"\", \"page\": 6, \"index\": 3, \"width\": 6999, \"height\": 4639}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-pan-diff4splat-repurposing-video-diffusion-models-for-dynamic-scene-generation-cvpr-2026-paper/fig-004.webp\", \"caption\": \"\", \"page\": 7, \"index\": 4, \"width\": 11843, \"height\": 5200}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-pan-diff4splat-repurposing-video-diffusion-models-for-dynamic-scene-generation-cvpr-2026-paper/fig-005.webp\", \"caption\": \"\", \"page\": 8, \"index\": 5, \"width\": 11635, \"height\": 3899}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-pan-diff4splat-repurposing-video-diffusion-models-for-dynamic-scene-generation-cvpr-2026-paper/fig-006.webp\", \"caption\": \"\", \"page\": 8, \"index\": 6, \"width\": 9031, \"height\": 3087}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-pan-diff4splat-repurposing-video-diffusion-models-for-dynamic-scene-generation-cvpr-2026-paper/fig-007.webp\", \"caption\": \"\", \"page\": 8, \"index\": 7, \"width\": 4081, \"height\": 1949}]"
motivation: 从单张图像生成动态场景往往需要测试时优化与后处理，难以一次性统一建模外观、几何和运动。
method: 复用视频扩散先验，结合大规模4D数据学到的几何与运动约束，用视频隐变换器直接预测可变形三维高斯场。
result: 单次前向即可生成包含外观、几何与运动的动态场景，无需测试时优化或后处理。
conclusion: 为四维动态场景生成提供了高效的前馈式一体化框架，拓展了扩散模型在动态几何建模中的应用。
---

## Abstract
We introduce Diff4Splat, a feed-forward framework for dynamic scene generation from a single image. Our method synergizes the powerful generative priors of video diffusion models with geometric and motion constraints learned from a large-scale 4D dataset. Given a single image, a camera trajectory, and an optional text prompt, our model directly predicts a dynamic scene represented by a deformable 3D Gaussian field. This approach captures appearance, geometry, and motion in a single pass, eliminating the need for test-time optimization or post-hoc processing. At the core of our framework is a video latent transformer that enhances existing video diffusion models, enabling them to jointly model spatio-temporal dependencies and predict 3D Gaussian Primitives over time. Supervised by objectives targeting appearance fidelity, geometric accuracy, and motion consistency, Diff4Splat generates high-fidelity dynamic scenes within 30 seconds. We demonstrate the effectiveness of Diff4Splat across video generation, novel view synthesis, and geometry extraction, where it matches or surpasses optimization-based methods for dynamic scene synthesis while being significantly more efficient.

---

## 论文详细总结（自动生成）

# Diff4Splat 论文中文总结

## 1. 核心问题与研究动机

- **任务定义**：从**单张图像**（外加相机轨迹与可选文本提示）生成**动态 3D 场景**，即显式的 4D 表示。
- **现有范式的两难**：
  - **多阶段流水线**：先生成视频，再做 3D 重建（如 AC3D + Mosca）。缺点是慢、易出错、缺乏端到端可控性。
  - **直接前馈生成**：目前大多只能产出 **2D 视频帧**或**静态 3D 场景**，无法刻画显式、动态的 3D 几何。
- **核心缺口**：缺少一个能**直接且高效**合成显式、可控场景表示的框架。
- **效率痛点量化**：DimensionX 需数小时 GPU 时间，Mosca 需约半小时；这类开销使其难以实用化。
- **整体含义**：作者提出将"生成"与"表示"统一到单次前馈中，把整条流水线压缩到约 30 秒，相对 SOTA 优化式方法实现约 **60 倍加速**。

## 2. 方法论

### 2.1 核心思想
- 在**单个端到端可训练模型**中，把**视频扩散骨干**与**可变形 3D 高斯场**表示统一起来。
- 关键桥梁是 **Video Latent Transformer / Latent Dynamic Reconstruction Model（LDRM）**：把 2D 时空隐特征解释为动态点云，在相机与时间嵌入条件下回归可变形高斯的参数。
- 设计意图：迫使扩散模型学习**关于显式 3D 几何与运动的强先验**，区别于以往只做 2D 视频或静态 3D 的工作。

### 2.2 输入与整体流程
- 输入：图像 $I_0 \in \mathbb{R}^{H\times W\times 3}$、文本提示 $C_{ctx}$、相机位姿 $P \in \mathbb{R}^{T\times H\times W\times 6}$（Plücker 嵌入）。
- 步骤一：预训练视频扩散模型在 $I_0$ 与 $P$ 条件下生成隐张量 $z \in \mathbb{R}^{n\times h\times w\times c}$。
- 步骤二：LDRM 处理 $z$ 与相机条件，预测可变形高斯场。
- 步骤三：用统一的光度 / 几何 / 运动监督 + 渐进式训练策略完成优化。

### 2.3 LDRM（隐空间动态重建模型）
- 将隐张量与位姿 token 拼接成**等长序列**，送入 Transformer 块（16 个标准 Transformer block）。
- 隐特征通道 $c=32$，先投影到 64 维嵌入；patch size 为 $2\times2$。
- 轻量解码器回归 3D 高斯属性，再经 3D 反卷积层映射回源视频像素。
- 每个 DiT 块带交叉注意力层，融合 T5 文本嵌入。
- 目的：避免昂贵的 per-scene 优化。

### 2.4 可变形高斯场
- 静态基元 $G_p$：均值 $\mu_p\in\mathbb{R}^3$、缩放 $s_p\in\mathbb{R}^3$、旋转四元数 $q_p\in\mathbb{R}^4$、不透明度 $\alpha_p$、颜色特征 $c_p$（用球谐 SH 建模视角相关效果）。
- 高斯核：$G_p(x)=\exp\left(-\tfrac12 (x-\mu_p)^\top \Sigma_p^{-1}(x-\mu_p)\right)$，$\Sigma_p$ 由 $s_p,q_p$ 导出。
- **形变建模**（逐时间步 $t$）：
  - $\mu_p^t := \mu_p^0 + \Delta\mu_p^t$
  - $q_p^t := q_p^0 \otimes \Delta q_p^t$（四元数乘法）
  - $s_p^t := s_p^0 + \Delta s_p^t$
- LDRM 输出**高斯特征图** $G\in\mathbb{R}^{(T\times H\times W)\times K_g}$ 与**形变图** $D\in\mathbb{R}^{(T\times H\times W)\times K_d}$，其中 $K_d=10$（$\Delta\mu\in\mathbb{R}^3$、$\Delta q\in\mathbb{R}^4$、$\Delta s\in\mathbb{R}^3$）。
- 渲染：可微分高斯光栅化；训练/推理时按不透明度剪枝，阈值 $\tau_{opacity}=0.005$。

### 2.5 训练目标
- 总损失：$L = L_{FM} + \lambda_{photo}L_{photo} + \lambda_{geo}L_{geo} + \lambda_{motion}L_{motion}$，权重 $\lambda_{photo}=1.0$、$\lambda_{geo}=0.5$、$\lambda_{motion}=2.0$。
- **Flow Matching 损失**：仅作用于基座视频扩散模型参数，用于在自建 4D 数据上微调，对齐隐空间；LDRM 与高斯预测头仅用渲染损失训练。
- **光度损失**：$\text{MSE}(\hat I_k, I_k) + \lambda_p\cdot\text{LPIPS}$，$\lambda_p=0.5$。
- **几何损失**：深度图相关性形式 $1-\frac{\text{Cov}(\hat D_k, D_k^*)}{\sqrt{\text{Var}(\hat D_k)\text{Var}(D_k^*)}}$，另加全变分正则 $L_{TV}=\|\nabla \hat D_k\|_1$。
- **运动损失**：基于 3D 点跟踪位移 $\Delta x_j$，$L_{motion}=\frac{1}{|O|}\sum_{j\in O}(\lambda_m\|\Delta\hat x_j-\Delta x_j\|_2+\|\Delta\hat x_j\|_1)$，$\lambda_m=2$；真实视频用 **CoTracker** 提取并按置信度过滤。
- **渐进式训练（共 100K 迭代）**：
  - ① **静态几何预训练**（40K iters，256×256，冻结形变模块，仅光度+几何损失）
  - ② **高分辨率精修**（40K iters，512×512，仍冻结形变模块）
  - ③ **动态场景微调**（20K iters，解冻全模型，启用完整损失含运动项）

### 2.6 数据构建
- **7 个合成数据集**：TartanAir、MatrixCity、PointOdyssey、DynamicReplica、Spring、VKITTI2、MultiCamVideo（提供精确几何/运动 GT，含静态与运动相机轨迹）。
- **2 个真实数据集**：RealEstate10K、Stereo4D（提供真实复杂度与自然变化，但相机运动有限、无度量尺度）。
- **度量尺度恢复（Algorithm 1）**：用 VideoDepthAnything 得到相对深度，用 MegaSaM 得到分割掩码，在掩码内查询度量深度真值，取相对深度中位数构成锚点对 $(d_{rel,i}, d_{gt,i})$，最小二乘求尺度 $s^*$ 与偏移 $t^*$，再应用到整幅相对深度图。
- **规模与质控**：约 **130,000** 个高质量 4D 训练场景；含动态物体掩码与重投影误差过滤。数据集将开源。

## 3. 实验设计

- **Benchmark / 评测集**：自建评测集 **160 个样本** = 32 个带文本描述的场景 × 5 种相机轨迹（螺旋、前向、后向、上移、下移）。
- **对比方法**：
  - 相机可控视频生成：**CameraCtrl**、**AC3D**。
  - 优化式显式 3DGS：**AC3D + Shape of Motion**、**AC3D + SaV**、**AC3D + Mosca**（均为 per-scene 优化，标 †）。
- **指标**：
  - 外观/美学：FVD、KVD、CLIP-Score、CLIP-Aesthetic、Q-Align（QA-Quality）。
  - 几何完整性：MASt3R 局部对应平均匹配数、Subject / Background Consistency Score。
  - 相机保真：相对位姿误差 **RPE**（平移/旋转）。
  - 效率：重建耗时。
- **主要量化结果**：
  - 表 1：FVD 210.153（优于 Mosca 的 235.961）；KVD 2.316（略逊于 Mosca 的 2.012）；CLIP-Score 23.123、CLIP-Aesthetic 5.231 均为最优；QA-Quality 2.813（略低于 Mosca 2.842）；**耗时 30 秒 vs Mosca 45 分钟**。
  - 表 2：平均匹配数 5114.22 最优；Subject Consistency 88.32 最优；Background Consistency 89.89（略低于 Mosca 90.43）。
  - 表 3：RPE 平移 0.012、旋转 0.008，远优于 AC3D（3.001 / 0.810）；且支持新视角合成、深度渲染与实时交互。
- **消融实验**：
  - **运动损失**（表 4）：去除后 FVD 从 210.153 恶化到 351.382，KVD 3.351，QA-Quality 2.145，匹配数与一致性全面下降。
  - **可变形高斯模块**（图 6）：去除后无法区分相机运动与前景物体运动，出现运动模糊、尖刺伪影与拖影。
  - **显式表示**（表 3）：带来更优相机可控性、深度光栅化与实时交互能力。
  - **渐进式训练**（图 7）：直接训练动态场景无法初始化 3DGS，训练不稳定、质量退化；需约 3 倍时间（21 天 vs 7 天）才能达到可比基线。
- **定性结果**：图 3 与 SOTA 对比，图 4 极端视角，图 5 应用展示（新视角合成、深度图提取）。

## 4. 资源与算力

- **基座模型**：CogVideoX（视频扩散 Transformer），运行在 3D Causal VAE 隐空间，压缩率 $32\times4\times8\times8$；32 个 block，隐藏维度 4096。
- **训练配置**：AdamW，初始学习率 $10^{-5}$，权重衰减 $10^{-4}$，余弦学习率调度，100,000 次迭代，**BF16 混合精度**。
- **算力规模**：**32 张 A100 GPU，约 7 天**。
- **推理成本**：生成一个动态场景约 **30 秒**。
- **对比说明**：论文指出若不做渐进式训练，直接训练动态场景需约 **21 天**（3 倍开销），说明训练成本压力较大。
- **未明确项**：未给出单次前向的显存占用、不同分辨率下的推理显存、以及数据标注流水线本身消耗的算力。

## 5. 实验数量与充分性

- **实验组数概览**：
  - 主定量对比 2 张表（视频/美学质量、几何完整性）。
  - 相机位姿精度对比 1 张表（表 3，含功能能力对比）。
  - 消融研究 3 组（运动损失、可变形高斯模块、渐进式训练）。
  - 定性对比与极端视角、应用展示（图 3–7）。
- **充分性评价**：
  - 优点：指标维度较全（视频质量 + 美学 + 几何一致性 + 位姿误差 + 效率），且做了逐模块消融，能较好支撑各设计选择的必要性。
  - 局限：评测集仅 **160 个样本 / 32 个场景**，规模偏小，统计稳健性有限。
  - **公平性风险**：论文自述许多近期前馈式 4D 生成方法**未开源或输入要求不同**，因此**无法做直接公平对比**，对比对象主要是"视频生成 + 优化式 3DGS
