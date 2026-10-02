---
title: "Neu-PiG: Neural Preconditioned Grids for Fast Dynamic Surface Reconstruction on Long Sequences"
title_zh: Neu-PiG：用于长序列快速动态表面重建的神经预条件网格
authors: "Kaltheuner, Julian, Dröge, Hannah, Plack, Markus, Stotko, Patrick, Klein, Reinhard"
date: 2026
publication_date: 2026
publication_date_precision: year
publication_date_source: conference year only; exact release date unverified
publication_date_kind: unknown
pdf: "https://openaccess.thecvf.com/content/CVPR2026/papers/Kaltheuner_Neu-PiG_Neural_Preconditioned_Grids_for_Fast_Dynamic_Surface_Reconstruction_on_CVPR_2026_paper.pdf"
tags: ["query:dr"]
score: 9.0
evidence: 长序列点云上的快速动态表面重建
tldr: 从非结构化点云对动态三维物体做时间一致表面重建在长序列上尤为困难，现有方法或增量优化易漂移耗时，或依赖类别特定训练。本文提出Neu-PiG，基于预条件隐网格编码的快速形变优化方法，将各时间步形变按多分辨率隐网格编码。实验表明其在长序列上实现快速且时间一致的表面重建，有效抑制漂移并大幅缩短运行时间。
source: CVPR-2026-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-kaltheuner-neu-pig-neural-preconditioned-grids-for-fast-dynamic-surface-reconstruction-on-cvpr-2026-paper/fig-001.webp\", \"caption\": \"\", \"page\": 1, \"index\": 1, \"width\": 7297, \"height\": 1536}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-kaltheuner-neu-pig-neural-preconditioned-grids-for-fast-dynamic-surface-reconstruction-on-cvpr-2026-paper/fig-002.webp\", \"caption\": \"\", \"page\": 3, \"index\": 2, \"width\": 5838, \"height\": 2031}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-kaltheuner-neu-pig-neural-preconditioned-grids-for-fast-dynamic-surface-reconstruction-on-cvpr-2026-paper/fig-003.webp\", \"caption\": \"\", \"page\": 6, \"index\": 3, \"width\": 11811, \"height\": 3145}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-kaltheuner-neu-pig-neural-preconditioned-grids-for-fast-dynamic-surface-reconstruction-on-cvpr-2026-paper/fig-004.webp\", \"caption\": \"\", \"page\": 7, \"index\": 4, \"width\": 8192, \"height\": 2211}]"
motivation: 从非结构化点云对动态三维物体进行时间一致表面重建困难，长序列尤甚。
method: 提出基于预条件隐网格编码的快速形变优化方法，将各时间步形变编码到多分辨率隐网格。
result: 在长序列上实现快速且时间一致的动态表面重建，避免漂移并减少运行时间。
conclusion: 无需类别特定训练即可高效处理长序列动态表面重建。
---

## Abstract
Temporally consistent surface reconstruction of dynamic 3D objects from unstructured point cloud data remains challenging, especially for very long sequences. Existing methods either optimize deformations incrementally, risking drift and requiring long runtimes, or rely on complex learned models that demand category-specific training. We present Neu-PiG, a fast deformation optimization method based on a novel preconditioned latent-grid encoding that distributes spatial features parameterized on the position and normal direction of a keyframe surface. Our method encodes entire deformations across all time steps at various spatial scales into a multi-resolution latent grid, parameterized by the position and normal direction of a reference surface from a single keyframe. This latent representation is then augmented for time modulation and decoded into per-frame 6-DoF deformations via a lightweight multi-layer perceptron (MLP). To achieve high-fidelity, drift-free surface reconstructions in seconds, we employ Sobolev preconditioning during gradient-based training of the latent space, completely avoiding the need for any explicit correspondences or further priors. Experiments across diverse human and animal datasets demonstrate that Neu-PiG outperforms state-the-art approaches, offering both superior accuracy and scalability to long sequences while running at least 60x faster than existing training-free methods and achieving inference speeds on the same order as heavy pre-trained models.

---

## 论文详细总结（自动生成）

# Neu-PiG 论文总结

## 1. 核心问题与整体含义（研究动机与背景）

- **核心问题**：从非结构化点云序列中对动态三维物体进行**时间一致的表面重建**，尤其是在**长序列**（如 40–120 帧以上）场景下仍要保持高保真度、无漂移且计算高效。
- **现有方法的两难困境**：
  - **优化类方法**（如 DynoSurf、PDG）：直接逐序列优化形变，质量高但耗时极长（数十分钟），且长序列下误差累积导致漂移甚至失败。
  - **学习类方法**（如 CaDeX、M2V）：依赖类别特定先验（人体、人脸、手等），推理快但泛化能力差，难以推广到任意类别（如动物）。
- **研究目标**：提出一种**类别无关（category-agnostic）、无需显式对应关系或强先验**的快速优化方法，兼顾精度、长序列可扩展性与运行效率。

## 2. 方法论：核心思想与关键技术细节

### 核心思想
将**所有时间步的完整形变**编码进一个**多分辨率隐体素网格**中，该网格由单个关键帧参考表面的**位置与法线方向**参数化；再通过时间调制与轻量级 MLP 解码出逐帧 6-DoF 形变。关键创新在于对**隐空间**（而非原始形变场）施加 Sobolev 预条件，使梯度更新在空间上平滑、时间上一致。

### 关键技术细节

- **初始化**：
  - 选取关键帧 $t_{key}$（依据点云空间范围并偏向序列时间中点），用 Screened Poisson 重建得到参考网格 $\mathbf{X}_{t_{key}}$。
  - 隐特征初始化为零向量；MLP 除最后一层外随机初始化，最后一层置零，使初始形变为恒等变换，避免优化初期跳跃。

- **多分辨率隐网格**：
  - **位置网格 $G_p$**：8 个层级，从 $2^3$ 到 $32^3$，每层 30 维特征，通过三线性插值采样后对 L 层取平均：
    $$z_p(x_{i,t_{key}}) = \frac{1}{L}\sum_{l=1}^{L} z_p^l(x_{i,t_{key}})$$
  - **法线方向网格 $G_n$**：单分辨率 $4^3$，每格 2 维特征，捕捉局部朝向信息，使相邻但法线不同的区域可独立形变。

- **时间形变模型**：
  - 每个顶点输入向量：$y_i = (z_n, z_p, \gamma(t))^T \in \mathbb{R}^{2+30+8}$。
  - **傅里叶时间编码**：$\gamma(t) = [\sin(\pi \nu_j \tilde{t}), \cos(\pi \nu_j \tilde{t})]_{j=1}^{M}$，$\nu_j = 2^{j-1}$，$M=4$，得到 8 维嵌入。
  - **网络结构**：3 层全连接 MLP，512 隐藏单元，LeakyReLU 激活，输出 7 维（旋转四元数 $q \in \mathbb{R}^4$ + 位移 $d \in \mathbb{R}^3$）。

- **变换映射**：
  - 四元数：$q_w$ 加 1 后归一化，保证零输出对应恒等旋转。
  - 位移：$\hat{d} = \tanh(\alpha d)$，$\alpha = 0.1$，限制位移幅度。
  - 最终变换：$\hat{x}_{i,t} = R(\hat{q}_i) x_{i,t_{key}} + \hat{d}_i$。

- **优化目标**：
  - 总损失：$\mathcal{L} = \mathcal{L}_{def} + w_{iso} \mathcal{L}_{iso}$，$w_{iso}=100$。
  - **形变损失**：时间自适应置信度加权的鲁棒 Chamfer 距离；置信度 $w_{conf}(t)$ 由累积乘积与“追赶变量” $\delta = 1 - \sqrt{\bar{e}}$ 构成。
  - **等距损失**：惩罚边长度变化，保持局部结构。
  - **Sobolev 预条件**：对隐网格参数更新施加 $(I + \lambda_l L_l)^{-2}$ 低通滤波，其中 $L_l$ 为层级 Laplacian，$\lambda_l$ 控制平滑强度。

- **实现细节**：Adam 优化器；MLP 学习率 $10^{-3}$，各网格层学习率 $0.005 \times 2.5^l$，平滑权重 $\lambda = 0.4 \times 1.5^l$。两种配置：250 epochs（Ours†）与 1000 epochs（Ours）。

## 3. 实验设计

- **数据集 / 场景**：
  - **DFAUST**：人体运动。
  - **AMA**：穿衣人体表演。
  - **DT4D**：关节动物运动。
  - 默认设置：每序列 $T=17$ 帧，每时间步 5000 个点。

- **Benchmark 与评价指标**：
  - $\ell_2$-Chamfer Distance（CD）、Normal Consistency（NC）、F-score（阈值 0.5%）、Correspondence Error（Corr.），以及平均单序列运行时间。

- **对比方法**：
  - **学习类基线**：CaDeX、M2V（需预定义帧间对应）。
  - **免训练优化基线**：DynoSurf、PDG。

- **可扩展性实验**：将 AMA 拆分为 40/60/80/100/120 帧的序列，对比 DynoSurf 与 PDG。

- **消融实验**：
  - **架构组件**：移除法线编码、去掉预条件、替换为 hash 编码、改为单分辨率。
  - **时间频率函数**：多项式基、高斯傅里叶映射、可学习嵌入 vs 本文傅里叶编码。
  - **稳定性函数**：δ 的 4 种调度（常数/线性/指数/插值），ω 的 4 种定义。

## 4. 资源与算力

- 论文明确提到评估使用 **NVIDIA RTX 4090**（单卡），并报告了两种优化长度：**250 epochs（Ours†）** 与 **1000 epochs（Ours）**。
- **未明确说明**：GPU 数量、总训练时长、完整训练能耗等细节。仅能从运行时间表间接推断：在 DFAUST 上 Ours† 为 8 秒、Ours 为 32 秒；在 AMA 长序列（120 帧）上 Ours 为 110 秒。

## 5. 实验数量与充分性

- **实验组数概览**：
  - 3 个数据集上的主实验（含 2 种配置）。
  - 1 组可扩展性实验（5 种序列长度 × 3 种方法）。
  - 3 大类消融实验（架构组件、时间编码、稳定性函数），共约 5 + 4 + 8 = 17 种变体配置。
- **充分性评价**：
  - **较充分**：覆盖了人体、穿衣人体、动物三类场景，兼顾精度、时间一致性与效率指标；消融实验系统性地验证了各模块的互补作用。
  - **客观公平**：对比方法涵盖学习类与免训练类，指标全面（CD、NC、F-score、Corr.、时间）。
  - **可补充之处**：未在真实扫描/噪声点云上验证；长序列实验仅在 AMA 上进行，未覆盖 DT4D 的更长序列；未与更多近期方法（如 4D Gaussian Splatting 类）对比。

## 6. 主要结论与发现

- Neu-PiG 在 **DFAUST、AMA、DT4D** 三个基准上均取得**最低 Chamfer Distance 与 Correspondence Error**，以及**最高的 Normal Consistency 与 F-score**。
- 相比免训练方法（DynoSurf、PDG），**运行速度快 60 倍以上**；推理速度与重型预训练模型处于同一量级。
- 在长序列（40–120 帧）上，PDG 运行时间急剧增加且最终失败，DynoSurf 精度显著退化，而 Neu-PiG 保持稳定对应关系与高几何保真度，**全程重建在 2 分钟内完成**。
- 消融表明：**法线方向编码、Sobolev 预条件、多分辨率网格、傅里叶时间编码、稳定性项**均对最终性能有正向贡献；hash 编码虽内存高效但牺牲空间平滑性。

## 7. 优点

- **类别无关**：不依赖 SMPL/FLAME 等类别特定模板，可泛化至人体与动物。
- **无需对应关系与强先验**：完全通过 Chamfer 距离隐式推断对应，避免了对显式匹配的依赖。
- **单隐空间共享**：与 PDG 的逐时间步形变网格不同，本文维护一个跨所有帧共享的预条件隐网格，有效抑制长序列漂移。
- **预条件作用于隐空间**：相比 PDG 对原始形变场预条件，本文对高维隐向量预条件，表达能力更强。
- **效率与精度兼顾**：8 秒（Ours†）即可获得接近 1000 epochs 的精度，实用性强。
- **消融设计系统**：从架构、时间编码到稳定性函数均有定量对比，结论可信。

## 8. 不足与局限

- **固定拓扑假设**：依赖关键帧网格的拓扑，若初始表面错误或不完整，无法恢复。
- **容量受限**：隐网格与网络表示能力限制了可建模的序列长度上限。
- **大运动/遮挡敏感**：极端非均匀形变（如强局部收缩）可能导致面片翻转。
- **实验覆盖有限**：
  - 未在真实噪声点云、稀疏点云或含遮挡的扫描数据上验证。
  - 长序列可扩展性仅在 AMA 上测试，未覆盖 DT4D 等更复杂动物运动。
  - 未与最新 4D Gaussian Splatting 或动态 NeRF 类方法对比。
- **算力细节不透明**：未报告 GPU 数量、总训练时长与能耗。
- **依赖关键帧选择策略**：虽沿用 PDG 的启发式，但关键帧质量对整体结果影响未做专门分析。

（完）
