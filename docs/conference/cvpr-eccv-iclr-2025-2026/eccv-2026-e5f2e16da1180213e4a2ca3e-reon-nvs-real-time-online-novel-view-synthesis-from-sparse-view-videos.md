---
title: "REON-NVS: Real-Time Online Novel-View Synthesis from Sparse-View Videos"
title_zh: REON-NVS：面向稀疏视角视频的实时在线新视角合成
authors: "Daeyeon Kim, Jinhyeok Kim, Gangmin Kwon, Seungjoo Shin, Sunghyun Cho"
date: 2026
publication_date: 2026
publication_date_precision: year
publication_date_source: conference year only; exact release date unverified
publication_date_kind: unknown
pdf: "https://media.eventhosts.cc/Conferences/ECCV2026/pdfs/3638.pdf"
tags: ["query:dr"]
score: 8.0
evidence: 面向稀疏视角视频的实时在线动态场景重建
tldr: 现有在线动态场景重建虽视觉质量出色，却需要大量输入视角与耗时迭代优化，且可靠的位姿估计还会引入额外延迟。本文提出REON-NVS，一个面向稀疏视角视频流的前馈式在线新视角合成框架，用前馈位姿估计器与建图模块替代传统相机位姿优化流程。实验表明其可在稀疏视角视频上实现从位姿估计到新视角重建的实时处理，为VR内容流等实时应用提供了高效方案。
source: ECCV-2026-Accepted-Program
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-e5f2e16da1180213e4a2ca3e/fig-001.webp\", \"caption\": \"\", \"page\": 1, \"index\": 1, \"width\": 512, \"height\": 512}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-e5f2e16da1180213e4a2ca3e/fig-002.webp\", \"caption\": \"\", \"page\": 1, \"index\": 2, \"width\": 512, \"height\": 512}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-e5f2e16da1180213e4a2ca3e/fig-003.webp\", \"caption\": \"\", \"page\": 1, \"index\": 3, \"width\": 512, \"height\": 512}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-e5f2e16da1180213e4a2ca3e/fig-004.webp\", \"caption\": \"\", \"page\": 1, \"index\": 4, \"width\": 512, \"height\": 512}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-e5f2e16da1180213e4a2ca3e/fig-005.webp\", \"caption\": \"\", \"page\": 1, \"index\": 5, \"width\": 512, \"height\": 512}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-e5f2e16da1180213e4a2ca3e/fig-006.webp\", \"caption\": \"\", \"page\": 1, \"index\": 6, \"width\": 512, \"height\": 512}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-e5f2e16da1180213e4a2ca3e/fig-007.webp\", \"caption\": \"\", \"page\": 1, \"index\": 7, \"width\": 2145, \"height\": 255}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-e5f2e16da1180213e4a2ca3e/fig-008.webp\", \"caption\": \"\", \"page\": 1, \"index\": 8, \"width\": 967, \"height\": 206}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-e5f2e16da1180213e4a2ca3e/fig-009.webp\", \"caption\": \"\", \"page\": 1, \"index\": 9, \"width\": 629, \"height\": 206}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-e5f2e16da1180213e4a2ca3e/fig-010.webp\", \"caption\": \"\", \"page\": 5, \"index\": 10, \"width\": 1425, \"height\": 596}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-e5f2e16da1180213e4a2ca3e/fig-011.webp\", \"caption\": \"\", \"page\": 5, \"index\": 11, \"width\": 621, \"height\": 358}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-e5f2e16da1180213e4a2ca3e/fig-012.webp\", \"caption\": \"\", \"page\": 5, \"index\": 12, \"width\": 549, \"height\": 400}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-e5f2e16da1180213e4a2ca3e/fig-013.webp\", \"caption\": \"\", \"page\": 5, \"index\": 13, \"width\": 640, \"height\": 400}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-e5f2e16da1180213e4a2ca3e/fig-014.webp\", \"caption\": \"\", \"page\": 5, \"index\": 14, \"width\": 400, \"height\": 400}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-e5f2e16da1180213e4a2ca3e/fig-015.webp\", \"caption\": \"\", \"page\": 5, \"index\": 15, \"width\": 771, \"height\": 919}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-e5f2e16da1180213e4a2ca3e/fig-016.webp\", \"caption\": \"\", \"page\": 5, \"index\": 16, \"width\": 641, \"height\": 849}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-e5f2e16da1180213e4a2ca3e/fig-017.webp\", \"caption\": \"\", \"page\": 5, \"index\": 17, \"width\": 530, \"height\": 533}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-e5f2e16da1180213e4a2ca3e/fig-018.webp\", \"caption\": \"\", \"page\": 5, \"index\": 18, \"width\": 679, \"height\": 1012}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-e5f2e16da1180213e4a2ca3e/fig-019.webp\", \"caption\": \"\", \"page\": 5, \"index\": 19, \"width\": 713, \"height\": 533}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-e5f2e16da1180213e4a2ca3e/fig-020.webp\", \"caption\": \"\", \"page\": 5, \"index\": 20, \"width\": 960, \"height\": 540}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-e5f2e16da1180213e4a2ca3e/fig-021.webp\", \"caption\": \"\", \"page\": 5, \"index\": 21, \"width\": 415, \"height\": 415}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-e5f2e16da1180213e4a2ca3e/fig-022.webp\", \"caption\": \"\", \"page\": 5, \"index\": 22, \"width\": 960, \"height\": 540}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-e5f2e16da1180213e4a2ca3e/fig-023.webp\", \"caption\": \"\", \"page\": 6, \"index\": 23, \"width\": 3325, \"height\": 942}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-e5f2e16da1180213e4a2ca3e/fig-024.webp\", \"caption\": \"\", \"page\": 6, \"index\": 24, \"width\": 3470, \"height\": 878}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-e5f2e16da1180213e4a2ca3e/fig-025.webp\", \"caption\": \"\", \"page\": 10, \"index\": 25, \"width\": 400, \"height\": 400}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-e5f2e16da1180213e4a2ca3e/fig-026.webp\", \"caption\": \"\", \"page\": 10, \"index\": 26, \"width\": 400, \"height\": 400}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-e5f2e16da1180213e4a2ca3e/fig-027.webp\", \"caption\": \"\", \"page\": 10, \"index\": 27, \"width\": 400, \"height\": 400}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-e5f2e16da1180213e4a2ca3e/fig-028.webp\", \"caption\": \"\", \"page\": 10, \"index\": 28, \"width\": 400, \"height\": 400}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-e5f2e16da1180213e4a2ca3e/fig-029.webp\", \"caption\": \"\", \"page\": 10, \"index\": 29, \"width\": 400, \"height\": 400}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-e5f2e16da1180213e4a2ca3e/fig-030.webp\", \"caption\": \"\", \"page\": 10, \"index\": 30, \"width\": 400, \"height\": 400}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-e5f2e16da1180213e4a2ca3e/fig-031.webp\", \"caption\": \"\", \"page\": 10, \"index\": 31, \"width\": 400, \"height\": 400}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-e5f2e16da1180213e4a2ca3e/fig-032.webp\", \"caption\": \"\", \"page\": 10, \"index\": 32, \"width\": 400, \"height\": 400}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-e5f2e16da1180213e4a2ca3e/fig-033.webp\", \"caption\": \"\", \"page\": 12, \"index\": 33, \"width\": 400, \"height\": 400}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-e5f2e16da1180213e4a2ca3e/fig-034.webp\", \"caption\": \"\", \"page\": 12, \"index\": 34, \"width\": 400, \"height\": 400}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-e5f2e16da1180213e4a2ca3e/fig-035.webp\", \"caption\": \"\", \"page\": 12, \"index\": 35, \"width\": 400, \"height\": 400}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-e5f2e16da1180213e4a2ca3e/fig-036.webp\", \"caption\": \"\", \"page\": 12, \"index\": 36, \"width\": 400, \"height\": 400}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-e5f2e16da1180213e4a2ca3e/fig-037.webp\", \"caption\": \"\", \"page\": 12, \"index\": 37, \"width\": 400, \"height\": 400}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-e5f2e16da1180213e4a2ca3e/fig-038.webp\", \"caption\": \"\", \"page\": 12, \"index\": 38, \"width\": 400, \"height\": 400}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-e5f2e16da1180213e4a2ca3e/fig-039.webp\", \"caption\": \"\", \"page\": 13, \"index\": 39, \"width\": 400, \"height\": 400}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-e5f2e16da1180213e4a2ca3e/fig-040.webp\", \"caption\": \"\", \"page\": 13, \"index\": 40, \"width\": 400, \"height\": 400}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-e5f2e16da1180213e4a2ca3e/fig-041.webp\", \"caption\": \"\", \"page\": 13, \"index\": 41, \"width\": 400, \"height\": 400}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-e5f2e16da1180213e4a2ca3e/fig-042.webp\", \"caption\": \"\", \"page\": 13, \"index\": 42, \"width\": 400, \"height\": 400}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-e5f2e16da1180213e4a2ca3e/fig-043.webp\", \"caption\": \"\", \"page\": 13, \"index\": 43, \"width\": 400, \"height\": 400}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-e5f2e16da1180213e4a2ca3e/fig-044.webp\", \"caption\": \"\", \"page\": 13, \"index\": 44, \"width\": 400, \"height\": 400}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-e5f2e16da1180213e4a2ca3e/fig-045.webp\", \"caption\": \"\", \"page\": 13, \"index\": 45, \"width\": 400, \"height\": 400}]"
motivation: 现有在线动态场景重建需大量输入视角与耗时迭代优化，且位姿估计带来额外延迟。
method: 提出REON-NVS前馈式在线新视角合成框架，用前馈位姿估计与建图替代传统位姿优化流程。
result: 在稀疏视角视频流上实现从位姿估计到新视角重建的实时处理。
conclusion: 为VR内容流等实时应用提供高效在线的动态场景合成方案。
---

## Abstract
Recent advances in online reconstruction of dynamic scenesdemonstrate impressive visual quality, showing potential for real-worldapplications such as VR content streaming. Yet, existing online recon-struction methods still require a large number of input views and time-consuming iterative optimization. Moreover, reliable pose estimation,a prerequisite for NVS, introduces additional delay. In this paper, wepresent REON-NVS, a feedforward online NVS framework for sparse-view input video streams, which goes from pose estimation to novel-viewreconstruction in real time. REON-NVS comprises two main compo-nents. First, our method leverages a feedforward pose estimator andmapper that replace conventional camera pose optimization pipelines.Second, we design a scene reconstructor built upon a state-space model(SSM), which efficiently synthesizes temporally consistent novel-view im-ages by exploiting information from previous frames. To train and eval-uate our approach in realistic in-the-wild streaming scenarios, we intro-duce a new multi-view dynamic scene dataset of 150 dynamic scenescaptured with moving cameras. Extensive experiments demonstrate thatREON-NVS achieves high visual quality while operating in real time (32FPS), validating its applicability in real-world scenarios.

---

## 论文详细总结（自动生成）

# REON-NVS 论文总结

## 1. 核心问题与研究背景

- **应用驱动**：自由视点视频（FVV）、AR/VR、VR内容流等场景需要从视频流中实时重建动态场景，并允许用户自由切换视角。
- **现有方法的两大瓶颈**：
  - **依赖稠密视角**：多数在线动态重建方法（如 3DGStream、HiCoM、IGS）需要较多输入视角才能稳定重建。
  - **延迟累积**：这些方法处理帧的速度远低于 30 FPS，且常依赖 COLMAP 等外部位姿估计流程，进一步引入额外延迟。
- **另一类方法的局限**：BTimer、MoVieS 等前馈方法虽快，但基于 Transformer 的时间建模对序列长度扩展性差，只能在固定窗口内保持时序一致，无法跨窗口连续处理；而 RGB-D 类方法则受限于深度传感器等硬件约束。
- **核心目标**：在**稀疏视角（2 路）**、**无位姿输入**、**移动相机**的条件下，实现**从位姿估计到新视角合成的端到端实时在线处理（>30 FPS）**。

## 2. 方法论

### 2.1 总体框架
- 每个时刻 $t$ 接收多视角帧 $\{I_t^k\}$ 与目标相机位姿 $p_t^T$，输出目标视角图像 $I_t^T$。
- 两大模块：**位姿估计与映射**（前馈、无迭代优化）+ **场景重建**（基于 SSM 的时序建模）。
- 采用**无几何（geometry-free）** 设计，直接合成新视角图像，不依赖显式 3D 表示。

### 2.2 位姿估计与映射
- **参考帧**：以第一帧 $I_1^0$ 作为规范参考帧 $I_r$，其位姿定义为单位旋转、零平移。
- **位姿估计器 $P$**：输入 $I_t^k$ 与 $I_r$，输出 9 维潜位姿向量 $\tilde{p}_t^k$（3D 平移 + 6D 旋转），表示在**潜空间**中。
  - 采用 **RayZer 式自监督学习**：不直接用 GT 位姿监督（SE(3) 监督不稳定、COLMAP 失败会引入噪声），而是通过 RGB 重建损失间接学习潜位姿空间。
- **位姿映射器 $M$**：由于目标位姿 $p_t^T$ 位于物理空间，而估计位姿在潜空间，两者存在表示错配。
  - 使用 MLP 实现：$\tilde{p} = M(p, (\tilde{p}', p'))$。
  - 参考对 $(\tilde{p}', p')$ 来自第二帧 $I_2^0$ 相对 $I_r$ 的潜位姿与物理位姿（物理位姿由 DA3 等方法计算），用于消除尺度歧义。

### 2.3 场景重建
- **历史融合模块（History Fusion）**：
  - 输入：$\{I_t^k\}$、潜位姿 $\{\tilde{p}_t^k\}$、目标潜位姿 $\tilde{p}_t^T$。
  - 形式化：$I_t^H, \mathcal{H}_t = H([I_t^k, \tilde{P}_t^k], \tilde{P}_t^T, \mathcal{H}_{t-1})$。
  - 使用 **Plücker 射线嵌入** 编码位姿信息，图像切分为 patch 后线性投影为 token。
  - 由 **N 个 Bi-SSM 块** 堆叠，基于 **Mamba2** 并借鉴 Vision Mamba 的双向扫描策略：
    - 前向扫描与后向扫描并行，后向扫描时翻转输入与目标 token，确保目标 token 在输入 token 之后处理。
    - **跨时间步传播 SSM 隐状态**作为时序记忆，前向初始隐状态来自上一时刻末隐状态，共 2N 个隐状态构成 $\mathcal{H}_t$。
  - 最后 n 个 token 经线性层映射为 RGB，得到粗预测 $I_t^H$。
- **视图细化模块（View Refinement）**：
  - 不使用时序线索，仅基于当前多视角输入精修：$I_t^T = R([I_t^k, \tilde{P}_t^k], [I_t^H, \tilde{P}_t^T])$。
  - 采用 **Bi-SSM + Transformer 混合架构**：Bi-SSM 参数量约为 Transformer 的一半，可在相同参数预算下堆叠更深网络以逐步精修；Transformer 弥补 SSM 在细粒度局部细节恢复上的不足。

### 2.4 训练策略
- **两阶段训练**：
  - 第一阶段：联合训练位姿估计器与场景重建模块，**自监督**（无 GT 位姿），目标潜位姿通过对 GT 目标帧应用位姿估计器得到。在 RealEstate10K 上训练 100K 迭代，重建 8 帧序列。
  - 第二阶段：冻结其他模块，**有监督**训练位姿映射器，在静态+动态混合数据（RealEstate10K + 自建数据集 + SelfCap）上微调 20K 迭代，序列扩展至 64 帧；位姿映射器再训练 20K 迭代，batch size 64。
- **损失函数**：
  - 总损失：$\mathcal{L} = \mathcal{L}_{photo} + \lambda_{flicker}\mathcal{L}_{flicker}$
  - 光度损失：$\mathcal{L}_{photo} = \mathcal{L}_{MSE} + \lambda_{per}\mathcal{L}_{per}$（MSE + 感知损失）
  - 闪烁损失：$\mathcal{L}_{flicker} = \|[\phi(I_t^T) - \phi(I_{t-1}^T)] - [\phi(I_t^{GT}) - \phi(I_{t-1}^{GT})]\|^2$，其中 $\phi$ 为预训练 VGG 特征，约束相邻帧特征差一致。
  - 损失同时施加于粗预测 $I_t^H$ 与精修输出 $I_t^T$。

## 3. 实验设计

### 3.1 数据集与 Benchmark
- **Neural 3D Video**（6 个动态多视角室内场景，固定相机）——固定相机流式 benchmark。
- **自建数据集**（150 个真实动态场景，手持三相机装置，1920×1200、30 FPS，平均 338 帧/场景，测试用 30 个场景）——移动相机流式 benchmark。
- **SelfCap**（6 场景）用于训练。
- **RealEstate10K** 用于训练与消融实验（pixelSplat 测试划分）。
- 评估设置：每场景 2 个输入视角、300 帧序列、分辨率 256。

### 3.2 对比方法
- **可流式方法**：3DGStream、HiCoM、IGS（均需位姿初始化与迭代优化）。
- **前馈方法**：DepthSplat（需预计算位姿 + 显式 3D 表示）、RayZer（无位姿、无几何、逐帧合成，最直接基线）。
- **逐帧重建**：3DGS。

### 3.3 评价指标
- PSNR、SSIM、LPIPS（渲染质量）；Flicker（时序一致性，即式 (7)）；FPS（运行速度）。
- FPS 统计口径：Ours 与 RayZer 统计完整前馈流程（含位姿估计与映射）；其他方法排除高斯初始化/位姿估计时间。

### 3.4 主要结果
- **Neural 3D Video**：Ours 达 32 FPS、23.63 dB PSNR、0.715 SSIM、0.199 LPIPS、8.97 Flicker，全面领先；与 IGS 在相同两场景比较时，Ours 24.62 dB vs IGS 21.23 dB。
- **自建数据集**：Ours 32 FPS、23.26 dB PSNR、0.617 SSIM、0.274 LPIPS、45.45 Flicker，同样领先；相比可流式方法提升 +3.3 dB，相比 RayZer 提升 +1.7 dB。
- **消融实验**：
  - **时序记忆**：通过检索任务验证，带时序记忆的模型可在数百帧后仍保持稳定 PSNR，并能恢复当前输入视角不可见的区域（图 6、图 7）。
  - **闪烁损失**：在 Neural 3D Video、自建数据集、RealEstate10K 三个数据集上均降低 Flicker 并提升 PSNR/SSIM/LPIPS（表 3）。
  - **双向 SSM 架构**：对比单向基线、双向扫描、Cross 交替扫描、Token Merge（Concat/Add）等配置，最佳组合达 22.04 dB（表 4）。

## 4. 资源与算力

- 论文明确提到：所有定量与定性实验均在**单张 NVIDIA A100 GPU** 上完成。
- 训练迭代次数：第一阶段 100K 迭代（RealEstate10K，8 帧序列），第二阶段 20K 迭代（64 帧序列，混合数据），位姿映射器 20K 迭代（batch size 64）。
- **未明确说明**：总 GPU 训练时长（小时/天数）、是否使用多卡并行训练、具体显存占用等。论文仅给出迭代次数与单卡型号，缺乏完整算力开销披露。

## 5. 实验数量与充分性

- **实验组数概览**：
  - 2 个主流 benchmark（固定相机 + 移动相机）× 多方法对比。
  - 3 组消融实验：时序记忆（检索任务）、闪烁损失（3 个数据集）、双向 SSM 架构（5 种配置）。
  - 与 6 个基线方法对比（3DGS、
