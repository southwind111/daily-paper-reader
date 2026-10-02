---
title: "Point2Pose: Occlusion-Recovering 6D Pose Tracking and 3D Reconstruction for Multiple Unknown Objects Via 2D Point Trackers"
title_zh: Point2Pose：基于二维点跟踪的多未知物体遮挡恢复6D位姿跟踪与三维重建
authors: "Tzu-Yuan Lin, Ho Lee, Kevin Doherty, Yonghyeon Lee, Sangbae Kim"
date: 2026
publication_date: 2026
publication_date_precision: year
publication_date_source: conference year only; exact release date unverified
publication_date_kind: unknown
pdf: "https://media.eventhosts.cc/Conferences/ECCV2026/pdfs/14346.pdf"
tags: ["query:dr"]
score: 5.0
evidence: 通过跟踪对运动物体进行在线三维重建
tldr: 从单目RGB-D视频中对多个未知物体进行因果6D位姿跟踪与重建具有挑战，通常需要CAD模型或类别先验。Point2Pose是一种无模型方法，仅由物体上稀疏图像点初始化，借助二维点跟踪器获得长程对应，实现完全遮挡后的即时恢复，并增量重建在线TSDF表示。该方法无需物体先验即可跟踪多个未见物体，并附带多物体跟踪数据集。
source: ECCV-2026-Accepted-Program
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-1ecfaf59a98959f65d942ef0/fig-001.webp\", \"caption\": \"\", \"page\": 2, \"index\": 1, \"width\": 6659, \"height\": 2328}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-1ecfaf59a98959f65d942ef0/fig-002.webp\", \"caption\": \"\", \"page\": 5, \"index\": 2, \"width\": 5009, \"height\": 2296}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-1ecfaf59a98959f65d942ef0/fig-003.webp\", \"caption\": \"\", \"page\": 11, \"index\": 3, \"width\": 640, \"height\": 480}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-1ecfaf59a98959f65d942ef0/fig-004.webp\", \"caption\": \"\", \"page\": 11, \"index\": 4, \"width\": 640, \"height\": 480}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-1ecfaf59a98959f65d942ef0/fig-005.webp\", \"caption\": \"\", \"page\": 11, \"index\": 5, \"width\": 640, \"height\": 480}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-1ecfaf59a98959f65d942ef0/fig-006.webp\", \"caption\": \"\", \"page\": 11, \"index\": 6, \"width\": 640, \"height\": 480}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-1ecfaf59a98959f65d942ef0/fig-007.webp\", \"caption\": \"\", \"page\": 12, \"index\": 7, \"width\": 3801, \"height\": 1078}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-1ecfaf59a98959f65d942ef0/fig-008.webp\", \"caption\": \"\", \"page\": 13, \"index\": 8, \"width\": 5779, \"height\": 2062}]"
motivation: 从单目RGB-D视频对多个未知物体进行6D位姿跟踪与重建通常需CAD模型或类别先验。
method: Point2Pose仅由稀疏图像点初始化，用二维点跟踪器获得长程对应，并增量重建在线TSDF表示。
result: 实现完全遮挡后的即时恢复，可跟踪多个未见物体，并发布多物体跟踪数据集。
conclusion: 提供了无需物体先验的因果6D位姿跟踪与重建方法。
---

## Abstract
We present Point2Pose, a model-free method for causal 6Dpose tracking of multiple rigid objects from monocular RGB-D video.Initialized only from sparse image points on the objects, our approachtracks multiple unseen objects without requiring object CAD modelsor category priors. Point2Pose leverages a 2D point tracker to obtainlong-range correspondences, enabling instant recovery after complete oc-clusion. Simultaneously, the system incrementally reconstructs an on-line Truncated Signed Distance Function (TSDF) representation of thetracked targets. Alongside the method, we introduce a new multi-objecttracking dataset comprising both simulation and real-world sequences,with motion-capture ground truth for evaluation. Experiments show thatPoint2Pose trades some single-object pose accuracy for broader model-free tracking capabilities, including multi-object tracking and recoveryfrom complete occlusion. Project page: https://point2pose.github.io/.

---

## 论文详细总结（自动生成）

# Point2Pose 论文总结

## 1. 核心问题与整体含义

- **研究背景**：从单目 RGB-D 视频中估计和跟踪刚性物体的 6D 位姿，是机器人操作、增强现实等任务的核心问题。
- **现有瓶颈**：
  - 许多高性能方法依赖物体 CAD 模型、类别先验，或需要多视角重建后再跟踪，难以用于开放世界中未见过的物体。
  - 现有无模型跟踪器多面向单物体，依赖帧间特征匹配，在完全遮挡、多物体交叉、机械臂遮挡等场景下容易丢失目标，且重定位脆弱。
- **论文目标**：提出 **Point2Pose**，一种无需 CAD 模型和类别先验的在线/因果式 6D 位姿跟踪与三维重建方法，可从单目 RGB-D 视频中同时跟踪多个未知刚性物体，并在完全遮挡后即时恢复。
- **整体含义**：论文强调用长程 2D 点跟踪作为持久的数据关联机制，替代昂贵且易失败的长期特征匹配；同时在线重建物体级 TSDF 模型。作者还提出新数据集 **YCBMultiTrack**，覆盖合成与真实多物体动态遮挡场景。

## 2. 方法论

### 2.1 核心思想

- 仅由物体上的少量稀疏图像点初始化。
- 使用长程 2D 点跟踪器获得跨长时间、跨遮挡的点对应关系。
- 将 2D 跟踪点用深度提升为 3D，并变换到物体坐标系，构建 **object-centric keypoint map**。
- 通过 **frame-to-map registration** 估计物体位姿；用 TSDF 进行假设选择和位姿精化；用因子图优化保持全局一致性；同时在线融合 TSDF 完成三维重建。

### 2.2 算法流程与关键技术

- **初始化与分割**：
  - 输入 RGB-D 视频帧 \(F_t=(I_t,D_t)\)。
  - 用户提供物体上的少量点。
  - 使用 Segment Anything 2 获得每个物体的分割掩码。

- **2D 点跟踪与多物体数据关联**：
  - 对每个物体维护 object-specific query set \(Q_i\)。
  - 在单次 tracker pass 中联合跟踪所有物体的查询点。
  - 跟踪器输出当前像素位置、可见性指示和不确定性。
  - 长程点身份使物体在完全遮挡后重新出现时可直接恢复对应关系，无需独立重定位模块。

- **关键点采样与地图构建**：
  - 当初始点被遮挡或转出视野时，在分割掩码内用 SuperPoint 检测候选点。
  - 采用贪心策略选择关键点，目标函数平衡：
    - 可跟踪性，由 SuperPoint 置信度表示；
    - 空间多样性，鼓励点保持理想间距；
    - 最小间距惩罚，避免点过近。
  - 新点先进入 pending 状态，经过多帧验证后才提升为地图关键点，以抑制深度噪声和错误位姿影响。

- **Frame-to-Map 位姿估计**：
  - 过滤不可见跟踪点，用深度反投影得到当前相机坐标系下的 3D 观测。
  - 与地图中的 3D 关键点建立对应。
  - 理论上可求解最小二乘点云配准问题，并用 SVD 解析求解。
  - 由于 2D 点跟踪存在大量离群点，直接 SVD 可能灾难性失败。

- **多假设 RANSAC + SVD**：
  - 顺序执行 RANSAC 和 SVD，生成多个候选位姿假设。
  - 每次选出最大几何内点集合后，将其从对应池中移除，再在剩余点上重复。
  - 这能保留被主导错误对应掩盖的合理位姿，尤其适合对称物体、重复纹理、圆柱体等几何退化场景。

- **基于 TSDF 的假设选择与 SDF 精化**：
  - 用当前掩码深度图像中的密集 3D 点评估每个位姿假设。
  - 将密集点变换到物体坐标系，计算其 TSDF 绝对值的得分，选最小者。
  - 随后最小化密集点到 TSDF 零水平面的距离，使用 Huber 损失和 Levenberg–Marquardt 迭代优化位姿。

- **在线因子图优化**：
  - 对每个物体，在新建关键帧时优化关键帧位姿和关键点。
  - 采用 inverse pose 参数化 \(X_m = T^O_C(m)\)。
  - 总损失包括：
    - prior loss：锚定第一关键帧，避免规范自由度歧义；
    - pose consistency loss：约束关键帧间相对运动与 registration 结果一致；
    - observation loss：用 bearing-range 表示衡量预测关键点与 3D 观测的方向和距离误差。
  - 使用 GTSAM 中的 Levenberg–Marquardt 求解。

- **TSDF 三维重建**：
  - 在物体坐标系中定义体积网格。
  - 在线融合分割后的 RGB-D 观测到 TSDF。
  - 新关键帧加入时更新 TSDF。
  - 最终用 marching cubes 提取网格，并过滤深度噪声导致的离散连通分量。
  - TSDF 同时用于位姿假设选择和精化。

## 3. 实验设计

- **数据集 / Benchmark**：
  - **HO3D_v3**：13 个手物交互序列，4 个物体，用于单物体位姿跟踪。
  - **YCBInEOAT**：9 个双机械臂操作 YCB 物体的序列，5 个物体，物体在图像中通常较小。
  - **YCBMultiTrack**：作者新建数据集，包含合成和真实序列。
    - 合成子集：使用 7 个 YCB 物体，包含单物体和双物体场景，物体沿线性或圆形轨迹运动，在 Isaac Lab 中渲染 RGB-D，有精确仿真真值。
    - 真实子集：使用 5 个 YCB 物体，包含 5 个单物体、4 个双物体、2 个三物体场景，用 Intel RealSense D435i 采集，用 OptiTrack 动捕提供近真值位姿，包含严重遮挡、完全消失和重新进入。
  - 评估指标：
    - ADD AUC 和 ADD-S AUC，阈值范围 0–0.1 m。
    - Chamfer distance 评估重建质量。

- **对比方法**：
  - **FoundationPose**：使用提供的物体 CAD 模型。
  - **BundleSDF**：无 CAD 模型，进行未知物体跟踪与重建。
  - **Point2Pose**：无 CAD 模型。
  - 在多物体场景中，FoundationPose 和 BundleSDF 被逐物体顺序运行。

- **主要实验结果**：
  - HO3D：
    - Point2Pose 与 BundleSDF 的 ADD-S AUC 接近，平均 ADD-S AUC 略高。
    - 但 ADD AUC 和 Chamfer distance 低于 BundleSDF。
    - 在 AP12 等低纹理序列上退化明显。
  - YCBInEOAT：
    - BundleSDF 平均 ADD-S 和 ADD AUC 高于 Point2Pose。
    - bleach v1 等纹理不足场景中 Point2Pose 表现较差。
  - YCBMultiTrack-Synthetic：
    - FoundationPose 在 CAD 条件下最好。
    - 在 CAD-free 方法中，Point2Pose 平均 ADD-S 和 ADD 优于 BundleSDF。
  - YCBMultiTrack-Real：
    - Point2Pose 平均 ADD-S AUC 约 89.43，ADD AUC 约 74.17，明显优于 BundleSDF。
    - 在完全遮挡后重新出现时，Point2Pose 能恢复位姿，而 BundleSDF 容易保持错误旧位姿。
  - 消融实验：
    - 移除 multi-hypothesis 后性能下降最大：ADD-S 从 95.07 降至 89.81，ADD 从 82.76 降至 65.52。
    - 移除 SDF refinement：ADD-S 94.40，ADD 77.37。
    - 移除 graph optimization：ADD-S 94.56，ADD 78.80。
  - 长程 vs 短程跟踪：
    - P2P-SH(10) 在点连续不可见 10 帧后永久丢弃。
    - 在遮挡严重序列中，Point2Pose 恢复 5/5 次遮挡事件，P2P-SH(10) 恢复 0/5 次。
    - mustard 序列中，Point2Pose ADD-S 93.79、ADD 84.36，而 P2P-SH(10) 分别降至 38.52 和 31.44。
  - 纹理分析：
    - 使用 Sobel 梯度幅值作为纹理代理。
    - 低纹理视角通常导致更大的 2D
