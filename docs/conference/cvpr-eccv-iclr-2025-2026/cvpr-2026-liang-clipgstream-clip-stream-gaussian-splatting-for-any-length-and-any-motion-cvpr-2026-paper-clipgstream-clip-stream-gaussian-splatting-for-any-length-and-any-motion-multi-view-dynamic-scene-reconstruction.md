---
title: "ClipGStream: Clip-Stream Gaussian Splatting for Any Length and Any Motion Multi-View Dynamic Scene Reconstruction"
title_zh: ClipGStream：面向任意长度与运动的多视角动态场景重建的片段流式高斯泼溅
authors: "Liang, Jie, Wu, Jiahao, Wang, Chao, Yang, Jiayu, Zheng, Xiaoyun, Xiong, Kaiqiang, Wang, Zhanke, Yan, Jinbo, Gao, Feng, Wang, Ronggang"
date: 2026
publication_date: 2026
publication_date_precision: year
publication_date_source: conference year only; exact release date unverified
publication_date_kind: unknown
pdf: "https://openaccess.thecvf.com/content/CVPR2026/papers/Liang_ClipGStream_Clip-Stream_Gaussian_Splatting_for_Any_Length_and_Any_Motion_CVPR_2026_paper.pdf"
tags: ["query:dr"]
score: 9.0
evidence: 片段流式高斯泼溅重建多视角动态场景
tldr: 针对长多视角序列与大尺度运动下动态3D场景重建中帧流方法时序不稳定、片段方法内存高且序列长度受限的问题，本文提出混合框架ClipGStream。它在片段级别而非帧级别进行流式优化，用片段独立的时空场和残差锚点补偿高效捕捉局部运动变化。实验表明该方法兼顾可扩展性与时序一致性，可处理任意长度和运动的动态场景，服务VR、MR、XR等沉浸式媒体。
source: CVPR-2026-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liang-clipgstream-clip-stream-gaussian-splatting-for-any-length-and-any-motion-cvpr-2026-paper/fig-001.webp\", \"caption\": \"\", \"page\": 1, \"index\": 1, \"width\": 1280, \"height\": 720}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liang-clipgstream-clip-stream-gaussian-splatting-for-any-length-and-any-motion-cvpr-2026-paper/fig-002.webp\", \"caption\": \"\", \"page\": 1, \"index\": 2, \"width\": 1280, \"height\": 712}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liang-clipgstream-clip-stream-gaussian-splatting-for-any-length-and-any-motion-cvpr-2026-paper/fig-003.webp\", \"caption\": \"\", \"page\": 1, \"index\": 3, \"width\": 2350, \"height\": 1748}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liang-clipgstream-clip-stream-gaussian-splatting-for-any-length-and-any-motion-cvpr-2026-paper/fig-004.webp\", \"caption\": \"\", \"page\": 1, \"index\": 4, \"width\": 512, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liang-clipgstream-clip-stream-gaussian-splatting-for-any-length-and-any-motion-cvpr-2026-paper/fig-005.webp\", \"caption\": \"\", \"page\": 1, \"index\": 5, \"width\": 512, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liang-clipgstream-clip-stream-gaussian-splatting-for-any-length-and-any-motion-cvpr-2026-paper/fig-006.webp\", \"caption\": \"\", \"page\": 4, \"index\": 6, \"width\": 740, \"height\": 461}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liang-clipgstream-clip-stream-gaussian-splatting-for-any-length-and-any-motion-cvpr-2026-paper/fig-007.webp\", \"caption\": \"\", \"page\": 4, \"index\": 7, \"width\": 908, \"height\": 547}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liang-clipgstream-clip-stream-gaussian-splatting-for-any-length-and-any-motion-cvpr-2026-paper/fig-008.webp\", \"caption\": \"\", \"page\": 4, \"index\": 8, \"width\": 1881, \"height\": 1057}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liang-clipgstream-clip-stream-gaussian-splatting-for-any-length-and-any-motion-cvpr-2026-paper/fig-009.webp\", \"caption\": \"\", \"page\": 4, \"index\": 9, \"width\": 1881, \"height\": 1057}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liang-clipgstream-clip-stream-gaussian-splatting-for-any-length-and-any-motion-cvpr-2026-paper/fig-010.webp\", \"caption\": \"\", \"page\": 5, \"index\": 10, \"width\": 563, \"height\": 317}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liang-clipgstream-clip-stream-gaussian-splatting-for-any-length-and-any-motion-cvpr-2026-paper/fig-011.webp\", \"caption\": \"\", \"page\": 5, \"index\": 11, \"width\": 643, \"height\": 338}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liang-clipgstream-clip-stream-gaussian-splatting-for-any-length-and-any-motion-cvpr-2026-paper/fig-012.webp\", \"caption\": \"\", \"page\": 5, \"index\": 12, \"width\": 563, \"height\": 317}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liang-clipgstream-clip-stream-gaussian-splatting-for-any-length-and-any-motion-cvpr-2026-paper/fig-013.webp\", \"caption\": \"\", \"page\": 5, \"index\": 13, \"width\": 563, \"height\": 317}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liang-clipgstream-clip-stream-gaussian-splatting-for-any-length-and-any-motion-cvpr-2026-paper/fig-014.webp\", \"caption\": \"\", \"page\": 7, \"index\": 14, \"width\": 1881, \"height\": 1057}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liang-clipgstream-clip-stream-gaussian-splatting-for-any-length-and-any-motion-cvpr-2026-paper/fig-015.webp\", \"caption\": \"\", \"page\": 7, \"index\": 15, \"width\": 1920, \"height\": 1080}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liang-clipgstream-clip-stream-gaussian-splatting-for-any-length-and-any-motion-cvpr-2026-paper/fig-016.webp\", \"caption\": \"\", \"page\": 7, \"index\": 16, \"width\": 1881, \"height\": 1057}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liang-clipgstream-clip-stream-gaussian-splatting-for-any-length-and-any-motion-cvpr-2026-paper/fig-017.webp\", \"caption\": \"\", \"page\": 7, \"index\": 17, \"width\": 1920, \"height\": 1080}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liang-clipgstream-clip-stream-gaussian-splatting-for-any-length-and-any-motion-cvpr-2026-paper/fig-018.webp\", \"caption\": \"\", \"page\": 7, \"index\": 18, \"width\": 1881, \"height\": 1057}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liang-clipgstream-clip-stream-gaussian-splatting-for-any-length-and-any-motion-cvpr-2026-paper/fig-019.webp\", \"caption\": \"\", \"page\": 7, \"index\": 19, \"width\": 1920, \"height\": 1080}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liang-clipgstream-clip-stream-gaussian-splatting-for-any-length-and-any-motion-cvpr-2026-paper/fig-020.webp\", \"caption\": \"\", \"page\": 7, \"index\": 20, \"width\": 1881, \"height\": 1057}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liang-clipgstream-clip-stream-gaussian-splatting-for-any-length-and-any-motion-cvpr-2026-paper/fig-021.webp\", \"caption\": \"\", \"page\": 7, \"index\": 21, \"width\": 1920, \"height\": 1080}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liang-clipgstream-clip-stream-gaussian-splatting-for-any-length-and-any-motion-cvpr-2026-paper/fig-022.webp\", \"caption\": \"\", \"page\": 7, \"index\": 22, \"width\": 1352, \"height\": 1014}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liang-clipgstream-clip-stream-gaussian-splatting-for-any-length-and-any-motion-cvpr-2026-paper/fig-023.webp\", \"caption\": \"\", \"page\": 7, \"index\": 23, \"width\": 1352, \"height\": 1014}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liang-clipgstream-clip-stream-gaussian-splatting-for-any-length-and-any-motion-cvpr-2026-paper/fig-024.webp\", \"caption\": \"\", \"page\": 7, \"index\": 24, \"width\": 1360, \"height\": 1024}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liang-clipgstream-clip-stream-gaussian-splatting-for-any-length-and-any-motion-cvpr-2026-paper/fig-025.webp\", \"caption\": \"\", \"page\": 8, \"index\": 25, \"width\": 864, \"height\": 648}]"
motivation: 长多视角序列与大尺度运动的动态3D场景重建困难，现有帧流方法时序稳定性差，片段方法内存高且长度受限。
method: 提出混合框架ClipGStream，在片段级别而非帧级别进行流式优化，用片段独立的时空场与残差锚点补偿建模动态运动。
result: 该方法兼顾可扩展性与时序一致性，能处理任意长度和运动的动态场景。
conclusion: 片段级流式优化为长序列动态高斯重建提供了平衡方案。
---

## Abstract
Dynamic 3D scene reconstruction is essential for immersive media such as VR, MR, and XR, yet remains challenging for long multi-view sequences with large-scale motion. Existing dynamic Gaussian approaches are either Frame-Stream, offering scalability but poor temporal stability, or Clip, achieving local consistency at the cost of high memory and limited sequence length. We propose ClipGStream, a hybrid reconstruction framework that performs stream optimization at the clip level rather than the frame level. The sequence is divided into short clips, where dynamic motion is modeled using clip-independent spatio-temporal fields and residual anchor compensation to capture local variations efficiently, while inter-clip inherited anchors and decoders maintain structural consistency across clips. This Clip-Stream design enables scalable, flicker-free reconstruction of long dynamic videos with high temporal coherence and reduced memory overhead. Extensive experiments demonstrate that ClipGStream achieves state-of-the-art reconstruction quality and efficiency.

---

## 论文详细总结（自动生成）

## ClipGStream 论文中文总结

### 1. 核心问题与整体含义（研究动机与背景）

- **应用背景**：VR、MR、XR 等沉浸式媒体需要高保真、可交互的三维动态内容，多视角同步视频采集为动态场景重建提供了丰富时空信息。
- **核心难题**：动态场景不仅需要重建几何与外观，还要准确建模时间维度的运动；在**长序列**和**大尺度/快速运动**下，现有方法面临明显瓶颈。
- **现有范式及其矛盾**：
  - **Frame-Stream 方法**（如 Dynamic3DGS、3DGStream、iFVC、HiCoM）：逐帧优化，可扩展至超长序列，但存在帧间抖动和误差累积。
  - **Clip 方法**（如 4DGS、4DGaussian、SpaceTimeGS、LocalDyGS）：对约 300 帧的片段联合优化，局部时序一致性好，但内存与计算开销大，难以扩展到长序列，且跨片段边界易出现时序不连续。
- **整体含义**：论文提出 **ClipGStream**，一种融合 Frame-Stream 可扩展性与 Clip 局部一致性优势的 **Clip-Stream 混合框架**，目标是在任意长度、任意运动幅度的多视角动态场景中实现稳定、无闪烁、可扩展的高质量重建。

---

### 2. 论文提出的方法论

#### 2.1 核心思想

- 将长视频划分为 **N 个短片段（Clip）**，每个片段包含 **M 个多视角帧**。
- 第一个片段 `Clip0` 作为 **Reference Clip**，完整优化以建立稳定的时空表示；其余 `Clip1...ClipN-1` 作为 **Source Clip**，在 Reference Clip 的基础上训练。
- 在 **片段内（Intra-clip）** 使用片段独立的时空场建模局部运动，并用残差锚点补偿大运动；在 **片段间（Inter-clip）** 继承锚点、静态特征与解码器，并冻结共享组件，以保持跨片段时序一致性。

#### 2.2 关键技术细节

- **基础表示**：采用类似 ScaffoldGS 的锚点结构。每个锚点包含 3D 位置 `μ`、静态特征 `fs ∈ R64` 和动态特征 `fd ∈ R64`；动态特征由时空场（STF）生成。
- **Reference Clip 训练**：
  - 锚点 `A0` 由 `Clip0` 内所有帧的 COLMAP 点云初始化。
  - STF0 实现为 **4D hash grid + fully fused MLP**，在时刻 `t` 计算动态特征：`fd,0 = φ0(h0(μ0, t))`。
  - 将 `[fs,0; fd,0]` 拼接后送入解码器 `d(·)`，得到 Temporal Gaussians：`Gt,0 = d([fs,0; fd,0])`，再经光栅化渲染并由真值图像监督。
  - 联合优化锚点位置、静态特征和 STF0 参数。
- **Source Clip 的片段内训练（Intra-clip）**：
  - **残差锚点补偿（RAC）**：对当前片段的 COLMAP 锚点 `Ac_n` 与 Reference Clip 锚点 `A0` 做几何感知去重，得到残差锚点 `Ar_n`，再合并为 `An = A0 ∪ Dedup(Ac_n, A0)`。
  - **几何感知去重**：每个 `A0` 中的锚点 `p` 表示为一个球，半径 `r` 为其到最近三个邻居的平均欧氏距离，形成球形覆盖场；对候选点 `q` 计算其到覆盖表面的有符号距离，若 `SDF(q) > 0` 则保留为残差锚点，否则丢弃。
  - **片段独立 STF**：每个片段分配独立的 `STF1...STFN-1`，避免共享 STF 导致后续片段覆盖先前学习的动态特征，从而提升长序列重建质量。
- **片段间继承策略（Inter-clip Inheritance）**：
  - 继承 Reference Clip 的锚点 `A0`、静态特征 `fs,0` 和解码器 `d`，并在后续片段训练中**保持冻结**。
  - 新片段的静态特征可写为 `fs,1 = [fs,0; fr_s,1]`，其中 `fr_s,1` 为与残差锚点关联的可学习残差分量。
  - 动态特征由片段专属 STF 生成：`fd,1 = φ1(h1(μ1, t))`，再送入冻结解码器得到 `Gt,1 = d([fs,1; fd,1])`。
  - 该设计保证跨片段几何与外观属性解码一致，显著抑制静态区域闪烁。
- **损失函数**：
  - 体积正则项 `Lv = Σ Prod(si_t)`，约束高斯尺度，促进紧凑表示。
  - 总损失：`L = (1 − λSSIM)L1 + λSSIM LSSIM + λv Lv`。
- **优化细节**：使用 Adam 优化器，学习率调度沿用 3DGS，但**每个片段重新初始化学习率调度器**，防止学习率过小影响后续片段优化。

---

### 3. 实验设计

#### 3.1 数据集与场景

- **Long 360**：1,400 帧、4K 分辨率、36 台相机 360 度环形布置，拍摄动态篮球比赛，用于挑战高速运动与长序列。测试相机为 0、10、20、30，其余 32 台用于训练，图像下采样 2 倍。
- **N3DV**：21 相机多视角系统，2704×2028、30 FPS，包含五个 300 帧场景，用于精细运动动态重建；另在 `flame salmon` 序列（1,200 帧）上验证可扩展性。
- **VRU (GZ)**：34 相机系统，1920×1080、25 FPS，真实篮球比赛，约 250 帧，运动范围更大，用于评估真实场景鲁棒性。

#### 3.2 Benchmark 与评价指标

- 指标包括：**PSNR、DSSIM1、DSSIM2、LPIPS**，以及效率指标 **FPS、训练时间、模型大小**。
- 静态方法在 Long 360 和 VRU 上仅在第 0 帧测试，作为动态重建的上界参考。

#### 3.3 对比方法

- **静态方法**：2DGS、3DGS、ScaffoldGS、GOF。
- **Frame-Stream 方法**：StreamRF、3DGStream、iFVC、HiCoM、4DGC、Dy3DGS。
- **Clip 方法**：4DGaussian、SpaceTimeGS、Swift4D、LocalDyGS、K-Planes、HexPlane、MixVoxels、NeRFPlayer、HyperReel、RealTimeGS、Grid4D、4K4D、ENeRF。
- **本文方法**：ClipGStream。

#### 3.4 消融实验

- **Decoder Inheritance（DI）**：验证解码器继承对动态区域渲染质量的影响。
- **Residual Anchors Compensation（RAC）**：验证残差锚点对大运动捕捉与闪烁抑制的作用。
- **Clip-Specific STF**：对比独立训练、共享 STF 与本文片段独立 STF。
- **Anchors Inheritance（AI）**：验证锚点继承对静态区域一致性的作用。
- **特征分解**：分别解码 `fs` 与 `fd`，分析静态/动态特征分工。
- **M 与 N 的消融**：研究片段长度 M 与总帧数 N 的关系，验证 `M < N` 时仍可无闪烁重建。

---

### 4. 资源与算力

- 论文**未明确报告所使用的 GPU 型号、数量、显存规模或具体训练硬件配置**。
- 文中提供了部分训练时间与模型大小对比，例如：
  - N3DV 上 ClipGStream 训练时间约 **0.5 小时**，模型大小约 **98 MB**；
  - 3DGStream 约 1.0 小时、1230 MB；LocalDyGS 约 0.58 小时、100 MB；SpaceTimeGS 超过 5 小时、200 MB。
- 因此，可以认为论文在效率层面给出了训练时长和模型体积指标，但**算力资源细节缺失**，复现时需自行推断或参考项目页。

---

### 5. 实验数量与充分性

- **实验规模**：
  - 在 **Long 360（1,400 帧）**、**VRU GZ（约 250 帧）**、**N3DV（五个 300 帧场景）** 以及 **N3DV flame salmon（1,200 帧）** 上进行了定量与定性比较。
  - 消融实验覆盖 **DI、RAC、Clip-Specific STF、AI、特征分解、M/N 设置** 等多个维度。
- **充分性**：
  - 整体实验数量较多，覆盖长序列、大运动、精细运动、真实比赛等不同难度场景，主实验和消融较完整。
  - 定性结果包括残差热力图、跨片段闪烁对比、动态区域细节对比，能够支撑核心主张。
- **客观性与公平性**：
  - 对比方法多为已发表 SOTA，训练/测试设置尽量遵循先前工作（如 N3DV 遵循 3DGStream 等设置，VRU 遵循 Swift4D 设置）。
  - 但部分对比方法在效率指标上存在缺失（如 FPS、训练时间、模型大小），静态方法仅在第 0 帧评估，属于上界参考而非完全同条件动态比较。
  - 论文未报告多次运行的方差或置信区间，统计显著性未量化。

---

### 6. 论文的主要结论与发现

- **Clip-Stream 框架有效**：在片段级别而非帧级别进行流式优化，可同时兼顾长序列可扩展性与跨片段时序一致性。
- **重建质量 SOTA**：
  - Long 360 上 PSNR 24.54，优于 3DGStream（21.94）、iFVC（22.35）、4DGaussian（22.01）、Swift4D（23.01）、LocalDyGS（23.11）等。
  - N3DV 上 PSNR 32.53，优于 SpaceTimeGS（32.05）、LocalDyGS（32.28）、RealTimeGS（32.01）等。
  - flame salmon（1,200 帧）上 PSNR 29.40，优于 4DGaussian（28.89）、LocalDyGS（28.15）等。
  - VRU GZ 上 PSNR 30.67，LPIPS 0.137，表现具有竞争力。
- **效率优势**：N3DV 上训练约 0.5 小时、模型约 98 MB，优于或接近多数对比方法。
- **关键模块必要性**：
  - 残差锚点补偿与锚点继承共同抑制跨片段闪烁。
  - 解码器继承显著提升动态区域清晰度。
  - 片段独立 STF 明显优于共享 STF 和独立训练。
- **可扩展性**：在 `M < N` 的分段设置下仍能实现无闪烁重建，突破传统 Clip 方法要求 `M = N` 的限制。

---

### 7. 优点

- **范式创新**：首次提出 Clip-Stream 动态重建框架，统一了 Frame-Stream 的可扩展性与 Clip 的局部一致性。
- **残差锚点补偿设计巧妙**：利用 COLMAP 点云与几何感知去重（球覆盖场 + SDF）选择性保留新出现或位移较大的结构，避免锚点冗余增长。
- **继承与冻结策略清晰**：锚点、静态特征、解码器跨片段继承并冻结，直接针对跨片段闪烁与表示不一致问题。
- **片段独立 STF**：避免共享时空场导致动态特征被后续片段覆盖，符合长序列局部运动建模需求。
- **实验覆盖较广**：包含 1,400 帧长序列、1,200 帧精细运动、真实篮球比赛等场景，定量、定性、消融较完整。
- **效率表现良好**：模型紧凑（98 MB）、训练时间较短（0.5 小时），具备实际部署潜力。

---

### 8. 不足与局限

- **依赖 COLMAP 位姿**：论文明确承认，在低图像重叠或大纹理缺失区域，COLMAP 可能给出不准确标定，影响重建质量；未来需集成更鲁棒的位姿估计。
- **算力信息缺失**：未报告 GPU 型号、数量、显存与训练硬件，影响复现与效率对比的完整判断。
- **对比公平性存在一定限制**：
  - 静态方法仅在第 0 帧评估，不能完全代表动态重建能力。
  - 部分对比方法在 FPS、训练时间、模型大小等指标上缺失数据。
  - 未报告随机种子、多次运行方差或统计检验。
- **应用限制**：
  - 方法针对多视角同步采集场景，单目或稀疏视角不适用。
  - 残差锚点依赖 COLMAP 点云质量，对拓扑剧烈变化、新物体突然出现等场景可能受限。
  - 超长序列验证主要在 1,400 帧规模，更长序列（如数万帧）的稳定性仍需进一步验证。
- **超参数敏感性**：片段长度 M、片段数量 N、学习率重初始化等对结果有影响，论文未系统分析其敏感性边界。

（完）
