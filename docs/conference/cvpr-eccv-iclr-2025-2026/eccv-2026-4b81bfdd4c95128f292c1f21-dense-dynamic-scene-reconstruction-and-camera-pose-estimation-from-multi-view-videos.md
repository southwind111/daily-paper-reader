---
title: Dense Dynamic Scene Reconstruction and Camera Pose Estimation from Multi-View Videos
title_zh: 从多视角视频进行稠密动态场景重建与相机位姿估计
authors: "Shuo Sun, Unal Artan, Malcolm Mielle, Achim Lilienthal, Martin Magnusson"
date: 2026
publication_date: 2026
publication_date_precision: year
publication_date_source: conference year only; exact release date unverified
publication_date_kind: unknown
pdf: "https://media.eventhosts.cc/Conferences/ECCV2026/pdfs/6561.pdf"
tags: ["query:dr"]
score: 9.0
evidence: 从多视角视频进行稠密动态场景重建与相机位姿估计
tldr: 从多台自由移动相机进行稠密动态场景重建与相机位姿估计是自然且困难的问题，先前方法仅支持单相机输入或依赖刚性固定的预标定相机阵列。本文提出两阶段优化框架，将任务解耦为鲁棒的相机跟踪与稠密深度细化，通过构建时空连接图同时利用相机内时间连续性与相机间空间重叠，实现一致尺度与稳健跟踪。该框架提升了多视角动态重建的实用性。
source: ECCV-2026-Accepted-Program
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-4b81bfdd4c95128f292c1f21/fig-001.webp\", \"caption\": \"\", \"page\": 1, \"index\": 1, \"width\": 534, \"height\": 329}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-4b81bfdd4c95128f292c1f21/fig-002.webp\", \"caption\": \"\", \"page\": 1, \"index\": 2, \"width\": 512, \"height\": 384}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-4b81bfdd4c95128f292c1f21/fig-003.webp\", \"caption\": \"\", \"page\": 1, \"index\": 3, \"width\": 512, \"height\": 384}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-4b81bfdd4c95128f292c1f21/fig-004.webp\", \"caption\": \"\", \"page\": 1, \"index\": 4, \"width\": 512, \"height\": 384}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-4b81bfdd4c95128f292c1f21/fig-005.webp\", \"caption\": \"\", \"page\": 1, \"index\": 5, \"width\": 512, \"height\": 384}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-4b81bfdd4c95128f292c1f21/fig-006.webp\", \"caption\": \"\", \"page\": 1, \"index\": 6, \"width\": 512, \"height\": 384}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-4b81bfdd4c95128f292c1f21/fig-007.webp\", \"caption\": \"\", \"page\": 1, \"index\": 7, \"width\": 512, \"height\": 384}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-4b81bfdd4c95128f292c1f21/fig-008.webp\", \"caption\": \"\", \"page\": 1, \"index\": 8, \"width\": 512, \"height\": 384}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-4b81bfdd4c95128f292c1f21/fig-009.webp\", \"caption\": \"\", \"page\": 1, \"index\": 9, \"width\": 512, \"height\": 384}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-4b81bfdd4c95128f292c1f21/fig-010.webp\", \"caption\": \"\", \"page\": 1, \"index\": 10, \"width\": 587, \"height\": 362}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-4b81bfdd4c95128f292c1f21/fig-011.webp\", \"caption\": \"\", \"page\": 1, \"index\": 11, \"width\": 534, \"height\": 329}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-4b81bfdd4c95128f292c1f21/fig-012.webp\", \"caption\": \"\", \"page\": 1, \"index\": 12, \"width\": 512, \"height\": 384}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-4b81bfdd4c95128f292c1f21/fig-013.webp\", \"caption\": \"\", \"page\": 1, \"index\": 13, \"width\": 534, \"height\": 329}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-4b81bfdd4c95128f292c1f21/fig-014.webp\", \"caption\": \"\", \"page\": 1, \"index\": 14, \"width\": 534, \"height\": 329}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-4b81bfdd4c95128f292c1f21/fig-015.webp\", \"caption\": \"\", \"page\": 1, \"index\": 15, \"width\": 512, \"height\": 384}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-4b81bfdd4c95128f292c1f21/fig-016.webp\", \"caption\": \"\", \"page\": 1, \"index\": 16, \"width\": 512, \"height\": 384}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-4b81bfdd4c95128f292c1f21/fig-017.webp\", \"caption\": \"\", \"page\": 1, \"index\": 17, \"width\": 512, \"height\": 384}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-4b81bfdd4c95128f292c1f21/fig-018.webp\", \"caption\": \"\", \"page\": 1, \"index\": 18, \"width\": 512, \"height\": 384}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-4b81bfdd4c95128f292c1f21/fig-019.webp\", \"caption\": \"\", \"page\": 1, \"index\": 19, \"width\": 512, \"height\": 384}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-4b81bfdd4c95128f292c1f21/fig-020.webp\", \"caption\": \"\", \"page\": 1, \"index\": 20, \"width\": 512, \"height\": 384}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-4b81bfdd4c95128f292c1f21/fig-021.webp\", \"caption\": \"\", \"page\": 1, \"index\": 21, \"width\": 512, \"height\": 384}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-4b81bfdd4c95128f292c1f21/fig-022.webp\", \"caption\": \"\", \"page\": 5, \"index\": 22, \"width\": 358, \"height\": 509}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-4b81bfdd4c95128f292c1f21/fig-023.webp\", \"caption\": \"\", \"page\": 5, \"index\": 23, \"width\": 509, \"height\": 313}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-4b81bfdd4c95128f292c1f21/fig-024.webp\", \"caption\": \"\", \"page\": 5, \"index\": 24, \"width\": 477, \"height\": 520}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-4b81bfdd4c95128f292c1f21/fig-025.webp\", \"caption\": \"\", \"page\": 5, \"index\": 25, \"width\": 496, \"height\": 509}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-4b81bfdd4c95128f292c1f21/fig-026.webp\", \"caption\": \"\", \"page\": 5, \"index\": 26, \"width\": 512, \"height\": 384}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-4b81bfdd4c95128f292c1f21/fig-027.webp\", \"caption\": \"\", \"page\": 12, \"index\": 27, \"width\": 795, \"height\": 616}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-4b81bfdd4c95128f292c1f21/fig-028.webp\", \"caption\": \"\", \"page\": 12, \"index\": 28, \"width\": 1164, \"height\": 456}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-4b81bfdd4c95128f292c1f21/fig-029.webp\", \"caption\": \"\", \"page\": 12, \"index\": 29, \"width\": 805, \"height\": 511}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-4b81bfdd4c95128f292c1f21/fig-030.webp\", \"caption\": \"\", \"page\": 14, \"index\": 30, \"width\": 831, \"height\": 481}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-4b81bfdd4c95128f292c1f21/fig-031.webp\", \"caption\": \"\", \"page\": 14, \"index\": 31, \"width\": 859, \"height\": 437}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-4b81bfdd4c95128f292c1f21/fig-032.webp\", \"caption\": \"\", \"page\": 14, \"index\": 32, \"width\": 883, \"height\": 485}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-4b81bfdd4c95128f292c1f21/fig-033.webp\", \"caption\": \"\", \"page\": 14, \"index\": 33, \"width\": 938, \"height\": 432}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-4b81bfdd4c95128f292c1f21/fig-034.webp\", \"caption\": \"\", \"page\": 14, \"index\": 34, \"width\": 1084, \"height\": 1182}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-4b81bfdd4c95128f292c1f21/fig-035.webp\", \"caption\": \"\", \"page\": 14, \"index\": 35, \"width\": 868, \"height\": 456}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-4b81bfdd4c95128f292c1f21/fig-036.webp\", \"caption\": \"\", \"page\": 14, \"index\": 36, \"width\": 857, \"height\": 451}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-4b81bfdd4c95128f292c1f21/fig-037.webp\", \"caption\": \"\", \"page\": 14, \"index\": 37, \"width\": 846, \"height\": 429}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-4b81bfdd4c95128f292c1f21/fig-038.webp\", \"caption\": \"\", \"page\": 14, \"index\": 38, \"width\": 621, \"height\": 380}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-4b81bfdd4c95128f292c1f21/fig-039.webp\", \"caption\": \"\", \"page\": 14, \"index\": 39, \"width\": 1084, \"height\": 1182}]"
motivation: 多自由相机动态重建困难，现有方法仅支持单相机或需刚性标定相机阵列。
method: 提出两阶段优化框架，解耦相机跟踪与稠密深度细化，构建时空连接图联合利用时空连续性。
result: 实现一致尺度与稳健跟踪，支持多自由移动相机下的稠密动态重建。
conclusion: 拓展了动态场景重建在真实多观察者场景中的适用性。
---

## Abstract
We address the challenging problem of dense dynamic scenereconstruction and camera pose estimation from multiple freely movingcameras—a setting that arises naturally when multiple observers capturea shared event. Prior approaches either handle only single-camera input orrequire rigidly mounted, pre-calibrated camera rigs, limiting their practicalapplicability. We propose a two-stage optimization framework that decou-ples the task into robust camera tracking and dense depth refinement. Inthe first stage, we extend single-camera visual SLAM to the multi-camerasetting by constructing a spatiotemporal connection graph that exploitsboth intra-camera temporal continuity and inter-camera spatial overlap,enabling consistent scale and robust tracking. To ensure robustness underlimited overlap, we introduce a wide-baseline initialization strategy usingfeed-forward reconstruction models. In the second stage, we refine depthand camera poses by optimizing dense inter- and intra-camera consistencyusing wide-baseline optical flow. Additionally, we introduce MultiCam-Robolab, a new real-world dataset with ground-truth poses from a motioncapture system. Finally, we demonstrate that our method significantly out-performs state-of-the-art feed-forward models on both synthetic and real-world benchmarks, while requiring less memory. Our code is released at

---

## 论文详细总结（自动生成）

# 论文总结：从多视角视频进行稠密动态场景重建与相机位姿估计

## 1. 核心问题与研究动机

- **研究背景**：多个观察者（如机器人、体育转播、多部手机/运动相机）同时从不同视角拍摄同一动态事件已日益普遍，此类场景对增强现实、动态高斯泼溅、多视角视频分析等应用有重要价值。
- **核心问题**：给定多路自由移动相机拍摄的同步视频，如何同时恢复任意时刻的稠密动态场景并估计各相机位姿。
- **现有方法的局限**：
  - 单相机动态重建方法（如 MegaSAM）仅利用相机内时间连续性，无法利用跨相机的空间一致性。
  - 多相机 SLAM 方法要么假设刚性固定的已标定相机阵列，要么仅面向静态全局地图构建，无法处理自由移动相机下的动态场景。
- **三大技术挑战**：
  1. **尺度歧义**：单目深度本质尺度不定，缺乏共享观测时各相机重建会漂移到不同尺度。
  2. **重叠有限**：自由移动相机之间的视角重叠可能极小甚至间歇性缺失，难以建立跨相机约束。
  3. **动态内容**：运动物体违反经典多视角几何的静态世界假设，需要鲁棒的对应估计。
- **整体含义**：本文首次针对"多自由相机动态场景重建"这一任务提出完整框架，显著提升了多视角动态重建在真实场景中的实用性。

## 2. 方法论

### 2.1 核心思想
采用**两阶段优化框架**，将任务解耦为：(1) 鲁棒的时空多相机跟踪；(2) 多视角稠密深度细化。核心是构建**时空连接图**，同时利用相机内时间连续性与相机间空间重叠。

### 2.2 问题定义
输入为多路时间同步的单目视频序列 $I = \{(I_t^i, K_i)\}$，目标是估计每帧相机状态 $X = \{(T_t^i, D_t^i)\}$，其中 $T_t^i \in SE(3)$ 为位姿，$D_t^i$ 为深度图。

### 2.3 关键技术细节

**（1）时空多相机跟踪**
- **基础**：采用 MegaSAM 的学习式稠密光流估计器，通过最小化加权重投影误差优化位姿 $T$ 与视差 $d$：$L(T,d) = \sum_{(i,j)\in\Omega} \|u_{ij}^{reproj} - u_{ij}^{flow}\|^2_{\Sigma_{ij}}$，其中动态物体被赋予低权重。
- **时空连接图** $\Omega = \Omega_{temp} \cup \Omega_{spat} \cup \Omega_{st}$：
  - $\Omega_{temp}$：单相机内维护时间窗口的相邻关键帧连接。
  - $\Omega_{spat}$：同一时刻不同相机间，若投影像素超过 75% 落在图像边界内则建立空间连接。
  - $\Omega_{st}$：当前关键帧与其他相机历史非活跃关键帧之间的跨相机历史连接。
  - **连接平衡策略**：设定最大边数，均匀分配跨相机连接，超出时移除最旧连接以防内存爆炸。

**（2）宽基线初始化**
- 使用前馈重建模型 **VGGT** 对每个相机流的前 $N_{init}$ 帧进行初始化，获得全局一致的粗略位姿与深度 $D_{VGGT}$。
- 使用单目深度模型 **UniDepth** 预测 $D_{mono}$，通过优化全局尺度 $s$ 与偏移 $o$ 对齐到初始化尺度：$\min \sum_k \|sD_k^{mono} + o - D_k^{VGGT}\|^2$。
- 跟踪阶段的 BA 目标函数加入先验深度正则项：$L(T,d) = \sum \|u^{reproj} - u^{flow}\|^2_{\Sigma} + \lambda\|d_i - D_i^s\|^2$。

**（3）多视角场景一致性细化**
- **稠密对应估计**：构建增强连接图 $\Omega_{refine}$，包含跟踪阶段的 $\Omega$ 以及每帧与偏移 $\{+2, +4, +8\}$ 的额外稠密时间连接，使用 **UFM** 模型估计宽基线光流。
- **优化目标**：$L_{reproj} = w_f L_{flow} + w_d L_{disp}$，其中 $L_{flow}$ 为光流重投影项（含可优化置信度 $c_i$ 与 $\lambda\log(1/c_i)$ 防止置信度坍塌），$L_{disp}$ 为视差一致性项以抑制深度闪烁。
- **两阶段优化**：
  - **Phase 1**：固定位姿，优化逐帧仿射参数 $\{s_i, \beta_i\}$ 与置信度图，建立跨帧一致尺度。
  - **Phase 2**：固定仿射参数，交替迭代优化逐像素深度与相机位姿；位姿优化加入先验正则 $L_{prior}$ 与时间平滑正则 $L_{smooth}$（旋转/平移），总损失 $L = L_{reproj} + L_{pose}$。

## 3. 实验设计

### 3.1 数据集与场景
- **MultiCamVideo-Dataset**（合成）：Unreal Engine 渲染，每片段 81 帧、10 个视角；随机抽取 50 个片段、每片段 3 个随机相机；图像裁剪至 512×384。
- **MultiCam-Robolab**（本文新建真实数据集）：24 个 RGB-D 序列，2–3 台 Microsoft Azure Kinect，30 FPS，150–300 帧；由 Qualisys 动捕系统提供真值位姿；分 5 类场景：Robodog 有重叠、Robodog 无重叠、RoboArm、DynamicHuman、三相机场景。

### 3.2 评价指标
- **位姿**：ATE、RTE、RRE（将多相机轨迹视为单一轨迹评估）。
- **深度**：Abs.Rel、$\delta_{1.25}$。
- **场景一致性**：点对点欧氏距离中位数 Md。

### 3.3 对比方法
- **经典 SfM**：COLMAP、GLOMAP（另测试"加动态掩码"与"加 NetVLAD 检索"两个变体）。
- **前馈模型**：VGGT、Fast3R、FastVGGT、CUT3R。

## 4. 资源与算力

- 文中**未提及训练时长**，因为该方法是基于优化的框架，不涉及大规模训练。
- 推理硬件明确说明：
  - Fast3R、FastVGGT 使用单张 **NVIDIA A100（40 GiB）**；
  - 其他所有方法（含本文方法）使用单张 **NVIDIA RTX 4090**。
- VGGT 因内存限制无法处理全部帧，评估时以间隔 8 采样。
- 报告了峰值推理显存：本文方法 **20.04 GB**，FastVGGT 22.08 GB，CUT3R 22.43 GB，Fast3R 39.20 GB，VGGT 则 OOM。

## 5. 实验数量与充分性

- **数据集覆盖**：1 个合成数据集 + 1 个新建真实数据集（5 类场景）。
- **对比实验**：位姿对比（表 1、2、3）、深度与场景一致性对比（表 4）、定性轨迹可视化（图 4）与重建可视化（图 5）。
- **消融实验**：
  - 表 5：去除宽基线初始化（w/o W.B. Init.）与去除时空图（w/o ST-Graph）的影响。
  - 表 6：对初始化位姿加入 3° 旋转噪声与 0.02/0.05/0.10 m 平移噪声的鲁棒性测试。
  - 表 7：细化阶段 Phase 1 / Phase 2 的贡献分析。
- **充分性评价**：实验覆盖面较广，含合成与真实、位姿与深度、多方法对比与多组消融，且提供了公平性设置（如 COLMAP/GLOMAP 的额外配置、VGGT 的采样说明）。但真实数据集规模有限（24 个序列、最多 3 相机），且消融主要在真实数据集上进行，合成数据集上缺少深度真值评估。

## 6. 主要结论与发现

- 本文方法在 MultiCamVideo 合成数据集上取得最优位姿结果（ATE 0.005，RRE 0.011），显著优于 COLMAP、Fast3R、FastVGGT、CUT3R。
- 在 MultiCamRobolab 真实数据集上总体表现最佳且显存消耗最少（20.04 GB），仅在 RoboDog 无重叠场景中略逊（此时时空连接退化为纯时间连接）。
- 深度与场景一致性评估中取得最一致结果。
- 一个反直觉发现：**剔除动态物体并不总能提升重建质量**——同步相机下动态物体瞬间静态一致，可提供有效的跨相机对应；在纹理匮乏环境中动态物体还提供关键点。
- FastVGGT 在所有前馈模型中表现最佳，说明"整体处理所有帧"优于 CUT3R 的测试时优化方式。
- 消融表明：宽基线初始化对跟踪至关重要；时空图能提升跟踪精度（在无重叠场景中帮助最小）；两阶段细化能提升深度精度与场景一致性；方法对轻度初始化噪声具有鲁棒性。

## 7. 优点

- **任务新颖性**：据作者所述，是首个面向多自由移动相机稠密动态场景重建与位姿估计的框架。
- **解耦设计**：将位姿估计与深度优化解耦，兼顾重建质量与长序列可扩展性。
- **时空连接图**：创新性地同时利用相机内时间连续性与相机间空间重叠，并通过连接平衡策略控制内存。
- **鲁棒初始化**：利用 VGGT + UniDepth 解决自由相机间重叠有限时的初始化难题，并提供全局尺度锚点。
- **数据集贡献**：公开 MultiCam-Robolab 真实数据集，含动捕真值，支持定量评估。
- **效率优势**：在取得更优结果的同时显存消耗低于同类前馈模型。
- **公平实验**：为基线方法设置了多种配置，并明确了内存受限时的采样策略。

## 8. 不足与局限

- **低重叠场景失效**：在 RoboDog 无重叠场景中，时空连接退化为纯时间连接，性能不及 FastVGGT，说明方法对相机间重叠仍有依赖。
- **依赖多个预训练模型**：框架串联了 MegaSAM、VGGT、UniDepth、UFM 等多个外部模型，工程复杂度高，且性能受各组件质量制约。
- **真实数据集规模有限**：仅 24 个序列、最多 3 台相机、5 类场景，场景多样性（如户外、大尺度、快速运动）不足。
- **缺少训练/推理时长报告**：未给出完整运行时间或效率对比，仅报告显存。
- **动态物体处理为隐式**：通过权重下采样处理动态物体，未显式建模物体运动，可能在大幅运动或长时间序列中失效。
- **合成数据集缺少深度真值评估**：MultiCamVideo 未提供深度真值，深度与一致性评估仅在真实数据集上进行。
- **场景一致性指标单一**：主要依赖点对点距离中位数 Md，可能无法全面反映重建的几何质量。

（完）
