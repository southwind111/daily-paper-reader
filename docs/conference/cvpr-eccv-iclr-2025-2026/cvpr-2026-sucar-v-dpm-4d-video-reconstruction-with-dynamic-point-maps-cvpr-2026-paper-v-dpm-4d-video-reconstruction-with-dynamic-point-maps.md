---
title: "V-DPM: 4D Video Reconstruction with Dynamic Point Maps"
title_zh: V-DPM：基于动态点图的4D视频重建
authors: "Sucar, Edgar, Insafutdinov, Eldar, Lai, Zihang, Vedaldi, Andrea"
date: 2026
publication_date: 2026
publication_date_precision: year
publication_date_source: conference year only; exact release date unverified
publication_date_kind: unknown
pdf: "https://openaccess.thecvf.com/content/CVPR2026/papers/Sucar_V-DPM_4D_Video_Reconstruction_with_Dynamic_Point_Maps_CVPR_2026_paper.pdf"
tags: ["query:dr"]
score: 9.0
evidence: 基于动态点图的4D视频重建
tldr: 动态点图虽能同时表达形状、相机与运动，但此前局限于图像对，多视图时仍需优化后处理。本文提出V-DPM，将动态点图扩展到视频，优化其表征能力并基于VGGT实现前馈神经预测与预训练模型复用。实验表明该方法能高效完成4D视频重建，为动态点图在视频场景中的实用化奠定基础。
source: CVPR-2026-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-sucar-v-dpm-4d-video-reconstruction-with-dynamic-point-maps-cvpr-2026-paper/fig-001.webp\", \"caption\": \"\", \"page\": 1, \"index\": 1, \"width\": 2300, \"height\": 1012}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-sucar-v-dpm-4d-video-reconstruction-with-dynamic-point-maps-cvpr-2026-paper/fig-002.webp\", \"caption\": \"\", \"page\": 5, \"index\": 2, \"width\": 1860, \"height\": 1750}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-sucar-v-dpm-4d-video-reconstruction-with-dynamic-point-maps-cvpr-2026-paper/fig-003.webp\", \"caption\": \"\", \"page\": 6, \"index\": 3, \"width\": 1568, \"height\": 1082}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-sucar-v-dpm-4d-video-reconstruction-with-dynamic-point-maps-cvpr-2026-paper/fig-004.webp\", \"caption\": \"\", \"page\": 7, \"index\": 4, \"width\": 1755, \"height\": 1599}]"
motivation: 动态点图此前仅限图像对，多视图时仍需后处理优化，难以直接用于视频。
method: 将动态点图扩展到视频，基于VGGT构建前馈式动态点图预测并复用预训练模型。
result: 实现高效前馈的4D视频重建，兼顾表征能力与神经预测便利性。
conclusion: 推动动态点图在视频4D重建任务中的实用化。
---

## Abstract
Powerful 3D representations such as DUSt3R's invariant point maps, which encode 3D shape and camera parameters, have significantly advanced feed-forward 3D reconstruction. While point maps assume static scenes, Dynamic Point Maps (DPMs) extend the concept to dynamic 3D content by also representing scene motion. However, DPMs have so far been limited to image pairs and, like DUSt3R, require post-processing via optimisation when more than two views are involved. We argue that DPMs are more useful when applied to videos and introduce V-DPM to demonstrate this. First, we show how to set up DPMs for videos to optimise representational power, facilitate neural prediction, and enable reuse of pretrained models. Second, we implement these ideas on top of VGGT, a recent powerful 3D reconstructor. Although VGGT was trained on static scenes, we show that a modest amount of synthetic data suffices to adapt it into an effective V-DPM predictor. This yields state-of-the-art 3D and 4D reconstruction in dynamic settings. In particular, unlike recent dynamic extensions of VGGT such as P3, DPMs recover not only dynamic depth but also the 3D motion of every point in the scene.

---

## 论文详细总结（自动生成）

# V-DPM：基于动态点图的 4D 视频重建 —— 论文总结

## 1. 核心问题与研究背景

- **前馈 3D 重建的进展**：以 DUSt3R 为代表的"视角不变点图（viewpoint-invariant point maps）"将 3D 形状与相机参数统一编码，极大推动了单次前馈的 3D 重建；后续 MV-DUSt3R、Fast3R、MapAnything、VGGT 等进一步扩展到多视图。
- **静态假设的局限**：原始点图表示不支持动态内容，而娱乐、机器人等真实场景普遍存在物体运动与形变。
- **动态点图（DPM）的提出与遗留问题**：DPM [17] 将点图扩展为同时具备视角不变性与时间不变性的表示，可统一表达 3D 形状、3D 运动、相机内参与外参。但它**仅支持图像对**，多于两视图时仍需像 DUSt3R 一样通过优化后处理融合；而且 DPM 向多图的推广方式并不显然——理论上点图数量可能随序列长度**二次增长**。
- **其他 4D 方法的不足**：MonST3R、CUT3R、π3、Align3R 等只能恢复并对齐动态深度，若不借助外部 2D 点跟踪器则无法直接得到场景运动（scene flow）。
- **论文立场**：DPM 应用于**视频**才更有价值，因此提出 **V-DPM**，实现多帧/视频的一次性（one-shot）前馈 4D 重建。

## 2. 方法论

### 2.1 核心思想：把"时间不变性"拆成两个阶段

- 沿用 DPM 定义：给定图像序列 $I_i$ 与时间戳 $t_i$、视点 $\pi_i$，点图 $P_i(t_j,\pi_k)\in\mathbb{R}^{3\times H\times W}$ 表示"图像 $I_i$ 的像素在时刻 $t_j$、相对视点 $\pi_k$ 的 3D 位置"。
- **冗余性分析**：令 $i,j,k$ 任意变化会得到 $N^3$ 个点图；但仅视点不同的点图之间只差刚体变换，固定公共视点 $\pi_0$ 后可降至 $N^2$；再从中挑选**有用的子集**，只需预测 $2N-1$ 个点图。
- 于是顺序计算两组点图：
  - **时间可变点图 P（黄色）**：$P=(P_0(t_0,\pi_0),P_1(t_1,\pi_0),\dots,P_{N-1}(t_{N-1},\pi_0))$。共享视点 $\pi_0$ 故视角不变，但各自使用输入帧自身的时间戳，**不具备时间不变性**，因而无法直接给出场景流。其形式与 VGGT 等静态模型对静态场景的输出高度相似，便于微调。
  - **时间不变点图 Q（红色）**：$Q=(P_0(t_j,\pi_0),P_1(t_j,\pi_0),\dots,P_{N-1}(t_j,\pi_0))$，把全部点统一表达在参考时刻 $t_j$，从而同时实现视角不变与时间不变。
- **两阶段的直觉**：要确定 $P_1(t_j,\pi_0)$，第二阶段可将 $P_1(t_1,\pi_0)$ 与第一阶段算出的 $P_i(t_j,\pi_0)$ 匹配，从而推断 3D 点如何"移动"；这相当于隐式地建立了跨时间的动态对应。
- **效率优势**：改变参考时刻 $t_j$ 只需重跑第二阶段解码器，第一阶段点图与绝大部分 backbone 计算可复用。

### 2.2 实现：基于 VGGT 的架构

- **骨干网络**：直接使用预训练的 VGGT（Alternating Attention Transformer），输入图像 patch token、camera token、register token；**移除冗余的深度图预测分支**，其余微调。
- **时间可变分支**：复用 VGGT 原有的 DPT head（从 backbone 四个层抽取 token）解码出时间可变点图 P；相机内参/外参沿用原相机回归头从 camera token 预测。
- **时间条件解码器（关键新增组件）**：
  - 结构为交替的 **frame attention + global attention** Transformer 块，输入仍是 backbone 特征 $\hat{p}_i$；
  - 迭代地将各帧特征对齐到 $P_j(t_j,\pi_0)$（其对应特征保持不变）；
  - 由于 DPT 需要四层特征，解码器对每层分别应用后拼接再送入 DPT head，且 DPT head 与时间可变分支**共享权重**，保证特征分布一致。
- **时间条件的注入方式**：
  1. 在输入 token 中增加一个 **target-time token** $t_j$，由 backbone 编码为 $\hat{t}_j$；
  2. 采用 **adaLN（自适应 LayerNorm，借鉴 FiLM / DiT）**：去掉 LayerNorm 中的可学习 scale/shift，改用 $\hat{t}_j$ 的线性投影去调制归一化后的 patch token，并对自注意力输出施加第二个投影做门控。
- **推理模式**：backbone 只前向一次，之后可对任意 $t_j$ 仅评估轻量解码器，显著节省计算。

### 2.3 训练策略

- 混合**静态 + 动态**数据微调：静态用 ScanNet++、BlendedMVS；动态用 Kubric-F、Kubric-G、PointOdyssey、Waymo。
- 处理方式沿用 DPM 并扩展到视频片段；与 DPM 不同的是，把 GT 点图缩放到"到原点平均距离为单位 1"，让网络像 VGGT 那样自行预测正确尺度。
- 训练采样 5 / 9 / 19 帧的片段（更长样本带来更好的复杂运动泛化）。
- 损失函数：DPM 的**置信度校准损失** + VGGT 的相机位姿回归损失。

## 3. 实验设计

### 3.1 任务与 benchmark

| 任务 | 数据集 | 指标 |
|---|---|---|
| 2 视图 4D 重建 | PointOdyssey、Kubric-F、Kubric-G、Waymo | 四个点图 $P_0(t_0),P_0(t_1),P_1(t_0),P_1(t_1)$ 的 EPE |
| 10 帧视频密集 3D 跟踪 | 同上四个数据集 | 首帧全部像素的 3D 轨迹 EPE |
| 视频深度估计 | Sintel、Bonn | Abs Rel、$\delta<1.25$ |
| 相机位姿估计 | Sintel、TUM-dynamics | ATE、RPE trans、RPE rot |
| 定性 4D 重建 | DAVIS（10 帧片段） | 可视化对比 |

- 2 视图实验分别采样间隔 **2 帧**与 **8 帧**的视图对；评估在**第一视图定义的世界坐标系**下进行（而非各视图局部相机系），使指标同时隐含衡量相机估计与点跟踪精度。
- 长序列（数百帧）采用**滑窗 + 类 DUSt3R 的 bundle adjustment** 优化融合，但约束形式从两两约束升级为**窗口约束**。

### 3.2 对比方法

- **4D 重建 / 跟踪**：DPM、St4RTrack、TraceAnything，以及"逐对独立运行的 V-DPM"作为消融式对照。
- **视频深度**：Marigold、DepthAnythingV2、NVDS、ChronoDepth、DepthCrafter、Robust-CVD、CasualSAM、MonST3R、DPM、CUT3R、VGGT、π3。
- **相机位姿**：Robust-CVD、CasualSAM、DUSt3R、MonST3R、DPM、CUT3R、VGGT、π3。

## 4. 资源与算力

- **论文未明确给出 GPU 型号、数量、训练时长或总计算量**，仅提到"具体训练超参数详见附录"（附录内容未包含在给定文本中）。
- 可获取的线索：
  - 作者提到受硬件限制，**只能微调到最长 20 帧的片段**（测试时可泛化到约 50 帧）；
  - 致谢中说明使用了英国 **Isambard-AI 国家 AI 研究资源（AIRR）**，由布里斯托大学运营。
- 结论：**算力细节披露不足**，无法据此评估训练成本与可复现性。

## 5. 实验数量与充分性

- **实验规模**：共覆盖 4 类任务、约 6 个不同数据集（PointOdyssey / Kubric-F / Kubric-G / Waymo / Sintel / Bonn / TUM-dynamics / DAVIS），另加 2 视图与 10 帧视频两种输入配置，整体覆盖面尚可。
- **客观性与公平性**：
  - 评估在统一世界坐标系下归一化后计算 EPE，指标定义与 DPM 一致，可比性较好；
  -
