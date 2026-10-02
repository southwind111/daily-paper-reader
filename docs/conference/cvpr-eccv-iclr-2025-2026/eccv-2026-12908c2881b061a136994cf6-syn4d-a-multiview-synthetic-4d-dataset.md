---
title: "Syn4D: A Multiview Synthetic 4D Dataset"
title_zh: Syn4D：一个多视角合成四维数据集
authors: "Zeren Jiang, Yushi Lan, Yihang Luo, Yufan Deng, Zihang Lai, Edgar Sucar, Christian Rupprecht, Iro Laina, Diane Larlus, Chuanxia Zheng, Andrea Vedaldi"
date: 2026
publication_date: 2026
publication_date_precision: year
publication_date_source: conference year only; exact release date unverified
publication_date_kind: unknown
pdf: "https://media.eventhosts.cc/Conferences/ECCV2026/pdfs/585.pdf"
tags: ["query:dr"]
score: 7.0
evidence: 支持动态场景重建与三维点跟踪的多视角合成四维数据集
tldr: 动态场景的三维重建与跟踪受限于缺乏密集完整且精确几何标注的高质量数据集。本文提出Syn4D，一个多视角合成四维动态场景数据集，包含真值相机运动、深度图、稠密跟踪与参数化人体姿态标注，并支持将任意像素反投影到任意时刻与任意相机。在四维场景重建、三维点跟踪、几何感知相机重定向与人体姿态估计等任务上的评估表明该数据集具有实用价值。
source: ECCV-2026-Accepted-Program
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-12908c2881b061a136994cf6/fig-001.webp\", \"caption\": \"\", \"page\": 1, \"index\": 1, \"width\": 1449, \"height\": 1295}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-12908c2881b061a136994cf6/fig-002.webp\", \"caption\": \"\", \"page\": 1, \"index\": 2, \"width\": 640, \"height\": 360}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-12908c2881b061a136994cf6/fig-003.webp\", \"caption\": \"\", \"page\": 1, \"index\": 3, \"width\": 640, \"height\": 360}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-12908c2881b061a136994cf6/fig-004.webp\", \"caption\": \"\", \"page\": 1, \"index\": 4, \"width\": 640, \"height\": 360}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-12908c2881b061a136994cf6/fig-005.webp\", \"caption\": \"\", \"page\": 1, \"index\": 5, \"width\": 640, \"height\": 360}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-12908c2881b061a136994cf6/fig-006.webp\", \"caption\": \"\", \"page\": 1, \"index\": 6, \"width\": 1280, \"height\": 720}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-12908c2881b061a136994cf6/fig-007.webp\", \"caption\": \"\", \"page\": 1, \"index\": 7, \"width\": 1280, \"height\": 720}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-12908c2881b061a136994cf6/fig-008.webp\", \"caption\": \"\", \"page\": 1, \"index\": 8, \"width\": 1280, \"height\": 720}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-12908c2881b061a136994cf6/fig-009.webp\", \"caption\": \"\", \"page\": 1, \"index\": 9, \"width\": 1280, \"height\": 720}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-12908c2881b061a136994cf6/fig-010.webp\", \"caption\": \"\", \"page\": 1, \"index\": 10, \"width\": 1280, \"height\": 720}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-12908c2881b061a136994cf6/fig-011.webp\", \"caption\": \"\", \"page\": 1, \"index\": 11, \"width\": 1280, \"height\": 720}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-12908c2881b061a136994cf6/fig-012.webp\", \"caption\": \"\", \"page\": 1, \"index\": 12, \"width\": 1280, \"height\": 720}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-12908c2881b061a136994cf6/fig-013.webp\", \"caption\": \"\", \"page\": 1, \"index\": 13, \"width\": 1280, \"height\": 720}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-12908c2881b061a136994cf6/fig-014.webp\", \"caption\": \"\", \"page\": 7, \"index\": 14, \"width\": 1280, \"height\": 720}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-12908c2881b061a136994cf6/fig-015.webp\", \"caption\": \"\", \"page\": 7, \"index\": 15, \"width\": 1280, \"height\": 720}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-12908c2881b061a136994cf6/fig-016.webp\", \"caption\": \"\", \"page\": 7, \"index\": 16, \"width\": 1280, \"height\": 720}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-12908c2881b061a136994cf6/fig-017.webp\", \"caption\": \"\", \"page\": 7, \"index\": 17, \"width\": 1280, \"height\": 720}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-12908c2881b061a136994cf6/fig-018.webp\", \"caption\": \"\", \"page\": 7, \"index\": 18, \"width\": 1280, \"height\": 720}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-12908c2881b061a136994cf6/fig-019.webp\", \"caption\": \"\", \"page\": 7, \"index\": 19, \"width\": 1280, \"height\": 720}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-12908c2881b061a136994cf6/fig-020.webp\", \"caption\": \"\", \"page\": 7, \"index\": 20, \"width\": 1280, \"height\": 720}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-12908c2881b061a136994cf6/fig-021.webp\", \"caption\": \"\", \"page\": 7, \"index\": 21, \"width\": 1280, \"height\": 720}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-12908c2881b061a136994cf6/fig-022.webp\", \"caption\": \"\", \"page\": 10, \"index\": 22, \"width\": 1317, \"height\": 1048}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-12908c2881b061a136994cf6/fig-023.webp\", \"caption\": \"\", \"page\": 10, \"index\": 23, \"width\": 1362, \"height\": 1133}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-12908c2881b061a136994cf6/fig-024.webp\", \"caption\": \"\", \"page\": 10, \"index\": 24, \"width\": 1402, \"height\": 1133}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-12908c2881b061a136994cf6/fig-025.webp\", \"caption\": \"\", \"page\": 10, \"index\": 25, \"width\": 1231, \"height\": 1133}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-12908c2881b061a136994cf6/fig-026.webp\", \"caption\": \"\", \"page\": 14, \"index\": 26, \"width\": 605, \"height\": 392}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-12908c2881b061a136994cf6/fig-027.webp\", \"caption\": \"\", \"page\": 14, \"index\": 27, \"width\": 734, \"height\": 505}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-12908c2881b061a136994cf6/fig-028.webp\", \"caption\": \"\", \"page\": 14, \"index\": 28, \"width\": 643, \"height\": 477}]"
motivation: 动态场景重建与跟踪受限于缺乏密集精确几何标注的高质量数据集。
method: 构建多视角合成四维数据集Syn4D，提供相机运动、深度、稠密跟踪与人体姿态标注。
result: 支持任意像素反投影到任意时刻与相机，在多项下游任务上验证有效。
conclusion: 为动态四维重建与跟踪研究提供了高质量评测基准。
---

## Abstract
Progress in tasks like 3D reconstruction and tracking of dynamic scenes from monocular video is constrained by the scarcity of high-quality datasets with dense, complete, and accurate geometric annotations. To address this limitation, we introduce Syn4D, a multiview synthetic dataset of dynamic scenes that includes ground-truth camera motion, depth maps, dense tracking, and parametric human pose annotations. A key feature of Syn4D is the ability to unproject any pixel into 3D to any time and to any camera. We conduct extensive evaluations across multiple downstream tasks to demonstrate the utility and e!ectiveness of the proposed dataset, including 4D scene reconstruction, 3D point tracking, geometry-aware camera retargeting, and human pose estimation. The experimental results highlight Syn4D’s potential to facilitate research in dynamic scene understanding and spatiotemporal modeling.

---

## 论文详细总结（自动生成）

# Syn4D：多视角合成四维数据集 —— 论文深度总结

## 1. 核心问题与整体含义（研究动机与背景）

- **核心瓶颈**：单目视频下的动态场景三维重建与跟踪（即 4D 重建）长期受制于**高质量数据集的稀缺**——现有数据缺乏密集、完整且精确的几何标注。作者认为这正是学习型方法迟迟难以比肩 SfM 等传统优化流程的主要原因之一。
- **现有数据的四类缺陷**：
  - 大规模预训练所需的数据集（如 VGGT、DUSt3R 系列所用数据）多为**私有**，且大多只含**静态场景**，不足以支撑 4D 重建；
  - 真实数据集（如 Stereo4D）标注**稀疏且有噪声**；
  - 合成动态数据集（Kubric、PointOdyssey、BEDLAM2）或**缺多视角**、或**缺稠密跟踪**、或**动态物体类型单一/仅含刚体**；
  - 驾驶/城市类合成集（Virtual KITTI、SYNTHIA、SEED4D 等）类别受限（车、行人）。
- **整体含义**：论文主张"数据工程"是 4D 视觉的关键突破口，提出 **Syn4D**——首个公开的、**多视角动态场景 + 稠密 3D 跟踪标注**的合成数据集，规模为 **4.7K 多视角视频片段、共 1.4M 帧**，远超同类带稠密几何与运动标注的数据集（如 Kubric 的 5.6K/274K）。
- **核心特性**：可把**任意像素反投影到任意时刻、任意相机**，从而同时支持 2D/3D 跟踪、深度、相机位姿、人体姿态与新视角合成等任务。

## 2. 方法论

### 2.1 数据表示（内容定义）

- 每个 clip 由"3D 环境 + 若干动态物体"随机组合而成，含 **C 个相机、T 帧**，共 N = T·C 个图像。
- 每个样本提供五元组 `{(I_i, P_i, S_i, t_i, ω_i)}`：
  - `I_i`：RGB 帧；`ω_i`：相机内外参；`S_i`：实例分割图；`t_i`：时间索引。
  - `P_i(ω_k, t_j) ∈ R^{3×H×W}`：**动态点图（DPM）**，即图像 I_i 中像素 u 对应的物理点在时刻 t_j、参考系 ω_k 下的三维坐标；深度图 D_i 由点图的 z 通道导出。
- 另有**参数化人体姿态**（SMPL-X，可重拟合为 SMPL）、**全局与局部文本描述**（每 81 帧一个局部 caption）。

### 2.2 稠密跟踪的高效存储（关键技术贡献）

- **朴素表示的复杂度爆炸**：全部 DPM 构成 (3×H×W)×N×N×T 的张量，复杂度 O(HWT³C²)；利用参考系间已知刚性变换可降到 O(HWT²C)，但仍不可行——以 H=W=512、T=300、C=8、4 字节/标量计，**单条 clip 需 2.1 TiB**，而原始 RGB 仅 7 GiB。
- **核心思想**：所有 3D 表面可表示为随时间变形的三角网格（顶点 q_v(t)，固定面片 F），因此每个像素只需记录**"落在哪个三角面 + 该面内的重心坐标"**。
- **重建公式**：对像素 u，其轨迹为
  `Q_i(t)(u) = ε₁·q_{f1}(t) + ε₂·q_{f2}(t) + ε₃·q_{f3}(t)`，t = 0,…,T−1。
- **存储量**：每像素仅 4 个标量（1 个面索引 + 3 个重心坐标），加上顶点轨迹 3×V×T，总复杂度降为 **O(HWTC + VT)**；同例下（V=100K）仅需 **9.3 GiB**。进一步可通过降低位宽、只对动态物体像素存储继续压缩。
- **解码效率**：查询某像素轨迹只需按重心坐标做线性组合，可在数据加载器内高效完成，适合训练/评测。
- **提取流程**：Unreal 无直接渲染通道，故离线计算——由深度图 D、旋转 R、位置 o、内参 K 反投影得 3D 点 `q̄(u) = R⁻¹K⁻¹D(u)(u,1)ᵀ + o`，再通过 **argmin 搜索最近面片与重心坐标** `(f(u), ε(u)) = argmin ‖q̄(u) − Σε_i q_{fi}(t)‖`。

### 2.3 数据生成流程

- **环境**：人工挑选并购买 **30 个 Fab 商店的高质量 3D 场景**，各指定一个根放置位置。
- **动态资产**：**1,674 个** Objaverse(-XL) 动画物体（机器人、动物、怪物等）+ **585 个** BEDLAM2 仿真人体。Objaverse 资产动画噪声大，故先**鸟瞰渲染 + 用相邻帧分割掩码 IoU 估计运动速度与形变**，过滤低 IoU/极端形变样本。
- **构图**：随机选 1–3 个动态物体 + 1 个人，用地面占用图随机初始化布局以避免碰撞。
- **光照**：UE5 Lumen 实时光照（动态光源）+ 静态光源的烘焙 lightmap。
- **相机设计**：水平 FOV 覆盖 **39.6°–90°**，室内/室外动态调整焦距；运动类型含 **static / tracking / dolly / orbit**，并叠加 Perlin 噪声抖动；每 clip **8 个相机**，采用四种多视角模式：
  - 8 条独立 orbit/dolly 镜头；
  - **Paired Orbit**：两条共享起始帧的 orbit；
  - **Paired Static-Orbit**：4 个正交静态镜头作为另 4 条 orbit 的起点。
- **Caption**：用 Tarsier2-7B，全局（全序列采 16 帧）+ 局部（每 81 帧采 32 帧）。

### 2.4 几何感知多视角扩散模型（基于本数据集的新任务）

- **任务定义**：给定源视频 I 及其点图序列 P，以及目标相机轨迹 ω′，同时合成**目标视频 I′ 与对应点图 P′**（即"新视角 + 新几何"）。
- **实现**：以 ReCamMaster 为基座，将其视频编码器 `L_vid = E(V)` 适配为 **DPM 编码器 `L_DPM = E(P)`**，并**空间拼接**两个潜变量 `Z = [L_vid; L_DPM] ∈ R^{H×(2W)×T×d}`；复用预训练扩散先验，**不引入新参数**。

## 3. 实验设计

### 3.1 任务一：几何感知新视角合成（NVS）

- **Benchmark（自建）**：280 个视频对，场景与动态物体**完全未见**。
- **对比方法**：同一模型分别在 **Kubric** 与 **Syn4D**
