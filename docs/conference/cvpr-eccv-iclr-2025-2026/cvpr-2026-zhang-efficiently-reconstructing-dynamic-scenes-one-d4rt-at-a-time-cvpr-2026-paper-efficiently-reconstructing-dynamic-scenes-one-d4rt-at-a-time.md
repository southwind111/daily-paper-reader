---
title: Efficiently Reconstructing Dynamic Scenes One D4RT at a Time
title_zh: 逐次一个D4RT：高效重建动态场景
authors: "Zhang, Chuhan, Le Moing, Guillaume, Koppula, Skanda, Rocco, Ignacio, Momeni, Liliane, Xie, Junyu, Sun, Shuyang, Sukthankar, Rahul, Barral, Joëlle K., Hadsell, Raia, Ghahramani, Zoubin, Zisserman, Andrew, Zhang, Junlin, Sajjadi, Mehdi S. M."
date: 2026
publication_date: 2026
publication_date_precision: year
publication_date_source: conference year only; exact release date unverified
publication_date_kind: unknown
pdf: "https://openaccess.thecvf.com/content/CVPR2026/papers/Zhang_Efficiently_Reconstructing_Dynamic_Scenes_One_D4RT_at_a_Time_CVPR_2026_paper.pdf"
tags: ["query:dr"]
score: 10.0
evidence: 前馈网络从视频重建动态四维场景几何与运动
tldr: 从视频中理解并重建动态四维场景的几何与运动仍是计算机视觉难题，现有方法往往需要密集逐帧解码或管理多个任务专用解码器，计算开销大。本文提出D4RT，一个简洁高效的前馈Transformer网络，可从单段视频联合推断深度、时空对应关系与完整相机参数，并通过统一解码接口独立查询任意时空点的三维位置。实验表明该方法轻量且可扩展，为动态四维重建提供了高效方案。
source: CVPR-2026-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-zhang-efficiently-reconstructing-dynamic-scenes-one-d4rt-at-a-time-cvpr-2026-paper/fig-001.webp\", \"caption\": \"\", \"page\": 1, \"index\": 1, \"width\": 354, \"height\": 352}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-zhang-efficiently-reconstructing-dynamic-scenes-one-d4rt-at-a-time-cvpr-2026-paper/fig-002.webp\", \"caption\": \"\", \"page\": 1, \"index\": 2, \"width\": 356, \"height\": 356}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-zhang-efficiently-reconstructing-dynamic-scenes-one-d4rt-at-a-time-cvpr-2026-paper/fig-003.webp\", \"caption\": \"\", \"page\": 1, \"index\": 3, \"width\": 358, \"height\": 358}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-zhang-efficiently-reconstructing-dynamic-scenes-one-d4rt-at-a-time-cvpr-2026-paper/fig-004.webp\", \"caption\": \"\", \"page\": 1, \"index\": 4, \"width\": 360, \"height\": 358}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-zhang-efficiently-reconstructing-dynamic-scenes-one-d4rt-at-a-time-cvpr-2026-paper/fig-005.webp\", \"caption\": \"\", \"page\": 1, \"index\": 5, \"width\": 2048, \"height\": 1035}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-zhang-efficiently-reconstructing-dynamic-scenes-one-d4rt-at-a-time-cvpr-2026-paper/fig-006.webp\", \"caption\": \"\", \"page\": 2, \"index\": 6, \"width\": 918, \"height\": 529}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-zhang-efficiently-reconstructing-dynamic-scenes-one-d4rt-at-a-time-cvpr-2026-paper/fig-007.webp\", \"caption\": \"\", \"page\": 2, \"index\": 7, \"width\": 509, \"height\": 472}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-zhang-efficiently-reconstructing-dynamic-scenes-one-d4rt-at-a-time-cvpr-2026-paper/fig-008.webp\", \"caption\": \"\", \"page\": 2, \"index\": 8, \"width\": 360, \"height\": 360}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-zhang-efficiently-reconstructing-dynamic-scenes-one-d4rt-at-a-time-cvpr-2026-paper/fig-009.webp\", \"caption\": \"\", \"page\": 2, \"index\": 9, \"width\": 983, \"height\": 523}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-zhang-efficiently-reconstructing-dynamic-scenes-one-d4rt-at-a-time-cvpr-2026-paper/fig-010.webp\", \"caption\": \"\", \"page\": 2, \"index\": 10, \"width\": 983, \"height\": 523}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-zhang-efficiently-reconstructing-dynamic-scenes-one-d4rt-at-a-time-cvpr-2026-paper/fig-011.webp\", \"caption\": \"\", \"page\": 2, \"index\": 11, \"width\": 983, \"height\": 523}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-zhang-efficiently-reconstructing-dynamic-scenes-one-d4rt-at-a-time-cvpr-2026-paper/fig-012.webp\", \"caption\": \"\", \"page\": 3, \"index\": 12, \"width\": 356, \"height\": 356}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-zhang-efficiently-reconstructing-dynamic-scenes-one-d4rt-at-a-time-cvpr-2026-paper/fig-013.webp\", \"caption\": \"\", \"page\": 3, \"index\": 13, \"width\": 356, \"height\": 358}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-zhang-efficiently-reconstructing-dynamic-scenes-one-d4rt-at-a-time-cvpr-2026-paper/fig-014.webp\", \"caption\": \"\", \"page\": 5, \"index\": 14, \"width\": 1126, \"height\": 569}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-zhang-efficiently-reconstructing-dynamic-scenes-one-d4rt-at-a-time-cvpr-2026-paper/fig-015.webp\", \"caption\": \"\", \"page\": 5, \"index\": 15, \"width\": 1322, \"height\": 767}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-zhang-efficiently-reconstructing-dynamic-scenes-one-d4rt-at-a-time-cvpr-2026-paper/fig-016.webp\", \"caption\": \"\", \"page\": 5, \"index\": 16, \"width\": 2048, \"height\": 1189}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-zhang-efficiently-reconstructing-dynamic-scenes-one-d4rt-at-a-time-cvpr-2026-paper/fig-017.webp\", \"caption\": \"\", \"page\": 5, \"index\": 17, \"width\": 2048, \"height\": 1017}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-zhang-efficiently-reconstructing-dynamic-scenes-one-d4rt-at-a-time-cvpr-2026-paper/fig-018.webp\", \"caption\": \"\", \"page\": 5, \"index\": 18, \"width\": 491, \"height\": 289}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-zhang-efficiently-reconstructing-dynamic-scenes-one-d4rt-at-a-time-cvpr-2026-paper/fig-019.webp\", \"caption\": \"\", \"page\": 5, \"index\": 19, \"width\": 815, \"height\": 471}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-zhang-efficiently-reconstructing-dynamic-scenes-one-d4rt-at-a-time-cvpr-2026-paper/fig-020.webp\", \"caption\": \"\", \"page\": 5, \"index\": 20, \"width\": 678, \"height\": 370}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-zhang-efficiently-reconstructing-dynamic-scenes-one-d4rt-at-a-time-cvpr-2026-paper/fig-021.webp\", \"caption\": \"\", \"page\": 5, \"index\": 21, \"width\": 1138, \"height\": 660}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-zhang-efficiently-reconstructing-dynamic-scenes-one-d4rt-at-a-time-cvpr-2026-paper/fig-022.webp\", \"caption\": \"\", \"page\": 5, \"index\": 22, \"width\": 706, \"height\": 382}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-zhang-efficiently-reconstructing-dynamic-scenes-one-d4rt-at-a-time-cvpr-2026-paper/fig-023.webp\", \"caption\": \"\", \"page\": 5, \"index\": 23, \"width\": 522, \"height\": 249}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-zhang-efficiently-reconstructing-dynamic-scenes-one-d4rt-at-a-time-cvpr-2026-paper/fig-024.webp\", \"caption\": \"\", \"page\": 6, \"index\": 24, \"width\": 1014, \"height\": 627}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-zhang-efficiently-reconstructing-dynamic-scenes-one-d4rt-at-a-time-cvpr-2026-paper/fig-025.webp\", \"caption\": \"\", \"page\": 6, \"index\": 25, \"width\": 652, \"height\": 474}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-zhang-efficiently-reconstructing-dynamic-scenes-one-d4rt-at-a-time-cvpr-2026-paper/fig-026.webp\", \"caption\": \"\", \"page\": 6, \"index\": 26, \"width\": 1023, \"height\": 481}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-zhang-efficiently-reconstructing-dynamic-scenes-one-d4rt-at-a-time-cvpr-2026-paper/fig-027.webp\", \"caption\": \"\", \"page\": 6, \"index\": 27, \"width\": 655, \"height\": 329}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-zhang-efficiently-reconstructing-dynamic-scenes-one-d4rt-at-a-time-cvpr-2026-paper/fig-028.webp\", \"caption\": \"\", \"page\": 6, \"index\": 28, \"width\": 1222, \"height\": 617}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-zhang-efficiently-reconstructing-dynamic-scenes-one-d4rt-at-a-time-cvpr-2026-paper/fig-029.webp\", \"caption\": \"\", \"page\": 6, \"index\": 29, \"width\": 1280, \"height\": 672}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-zhang-efficiently-reconstructing-dynamic-scenes-one-d4rt-at-a-time-cvpr-2026-paper/fig-030.webp\", \"caption\": \"\", \"page\": 6, \"index\": 30, \"width\": 512, \"height\": 333}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-zhang-efficiently-reconstructing-dynamic-scenes-one-d4rt-at-a-time-cvpr-2026-paper/fig-031.webp\", \"caption\": \"\", \"page\": 8, \"index\": 31, \"width\": 1024, \"height\": 436}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-zhang-efficiently-reconstructing-dynamic-scenes-one-d4rt-at-a-time-cvpr-2026-paper/fig-032.webp\", \"caption\": \"\", \"page\": 8, \"index\": 32, \"width\": 1024, \"height\": 436}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-zhang-efficiently-reconstructing-dynamic-scenes-one-d4rt-at-a-time-cvpr-2026-paper/fig-033.webp\", \"caption\": \"\", \"page\": 8, \"index\": 33, \"width\": 1024, \"height\": 436}]"
motivation: 动态四维场景重建计算开销大，现有方法依赖密集逐帧解码与多解码器。
method: 提出统一Transformer前馈网络D4RT，联合推断深度、时空对应与相机参数。
result: 通过统一解码接口可独立查询任意时空点的三维位置，方法轻量可扩展。
conclusion: 为动态四维场景重建提供了高效且可扩展的新范式。
---

## Abstract
Understanding and reconstructing the complex geometry and motion of dynamic 4D scenes from video remains a formidable challenge in computer vision. This paper introduces D4RT, a simple yet powerful feedforward network designed to efficiently solve this task. D4RT utilizes a unified transformer architecture to jointly infer depth, spatio-temporal correspondence, and full camera parameters from a single video. Its core innovation is a novel mechanism that sidesteps the heavy computation of dense, per-frame decoding and the complexity of managing multiple, task-specific decoders. Our unified decoding interface allows the model to independently and efficiently probe the 3D position of any point in space and time. The result is a lightweight and highly scalable method that enables remarkably efficient training and inference. We demonstrate that our approach sets a new state-of-the-art, outperforming previous methods across a wide spectrum of 4D reconstruction tasks.

---

## 论文详细总结（自动生成）

# D4RT 论文结构化总结

## 1. 核心问题与整体含义

- **研究动机**：从视频中理解和重建动态 4D 场景的复杂几何与运动，是计算机视觉中的核心难题。
- **现有问题**：
  - 传统方法常将任务拆分为多个专用组件，如单目深度、度量深度、运动分割等，再通过昂贵的测试时优化融合。
  - 近期前馈方法如 VGGT 虽提升效率，但通常使用多个任务专用解码器，且难以处理动态区域对应。
  - 跟踪方法如 SpatialTrackerV2 能处理动态，但依赖多阶段或迭代细化，速度慢、流程复杂。
- **整体含义**：论文提出 D4RT，将 4D 重建从“密集逐帧解码 + 多任务解码器”转向“统一场景表征 + 按需查询解码”，试图用单一前馈模型统一深度、点云、相机参数、3D 点跟踪等任务。

## 2. 方法论

- **核心思想**：
  - 采用编码器-解码器架构，类似 Scene Representation Transformer。
  - 编码器先将视频编码为全局场景表征 \(F = E(V)\)，该表征固定，包含全视频时空对应、时间流与场景几何信息。
  - 解码器通过统一查询接口独立预测任意 2D 点在任意目标时刻、任意相机参考下的 3D 位置。

- **查询定义**：
  - 查询 \(q = (u, v, t_{\text{src}}, t_{\text{tgt}}, t_{\text{cam}})\)。
  - \((u,v)\) 为源帧 \(t_{\text{src}}\) 中的归一化 2D 坐标。
  - \(t_{\text{tgt}}\) 为目标时间步，\(t_{\text{cam}}\) 为参考相机坐标系对应的时间步。
  - 解码输出：\(P = D(q, F) \in \mathbb{R}^3\)。

- **统一 4D 任务**：
  - 固定 \((u,v,t_{\text{src}})\)，变化 \(t_{\text{tgt}}=t_{\text{cam}}\)，得到点轨迹。
  - 对所有像素查询并固定参考相机，得到点云。
  - 令 \(t_{\text{src}}=t_{\text{tgt}}=t_{\text{cam}}\)，取输出 Z 维度，得到深度图。
  - 通过查询网格点并求刚体变换，估计相机外参。
  - 通过查询 3D 点并按针孔模型反推焦距，估计相机内参。

- **关键技术细节**：
  - 编码器：ViT，含局部帧内注意力和全局自注意力层，输入视频缩放到固定方形分辨率，并额外嵌入原始宽高比 token。
  - 解码器：轻量 cross-attention transformer。查询 token 由 2D 坐标的 Fourier 特征、离散时间步嵌入，以及局部 \(9\times9\) RGB patch 嵌入组成。
  - 查询独立解码：每个查询单独 cross-attend 到 \(F\)，查询之间不进行 self-attention。作者认为这避免计算负担和训练-测试分布偏移，并迫使编码器隐式编码全局一致性。
  - 相机外参：对两帧采样 \(k\) 个源点，分别解码到不同参考坐标系，再用 Umeyama 算法通过 \(3\times3\) SVD 求刚体变换。
  - 相机内参：假设主点在 \((0.5,0.5)\)，由 3D 点反推焦距，如 \(f_x = p_z(u-0.5)/p_x\)、\(f_y = p_z(v-0.5)/p_y\)，并取中位数增强鲁棒性；畸变模型可加非线性精化。
  - 损失：主损失为归一化 3D 点位置的 L1；辅助损失包括 2D 坐标 L1、3D 表面法线余弦相似度、可见性 BCE、点运动 L1，以及置信度惩罚。

- **稠密跟踪算法**：
  - 为避免 \(O(T^2HW)\) 的朴素全像素查询，使用占用网格 \(G \in \{0,1\}^{T\times H\times W}\)。
  - 仅从未访问像素发起新轨迹，每条完整轨迹将可见时空像素标记为已访问。
  - 根据运动复杂度获得约 \(5-15\times\) 自适应加速。

## 3. 实验设计

- **训练数据**：
  - 公开数据集包括 BlendedMVS、Co3Dv2、Dynamic Replica、Kubric、MVS-Synth、PointOdyssey、ScanNet++、ScanNet、Tartanair、VirtualKitti、Waymo Open，以及内部数据集。
  - 训练使用 48 帧片段，分辨率 \(256\times256\)，每视频解码 2048 个随机查询。

- **评估任务与 benchmark**：
  - **4D 重建与 3D 跟踪**：TAPVid-3D，包括 DriveTrack、ADT、PStudio，评估局部相机坐标和世界坐标下的 3D 跟踪。
  - **点云重建**：MPI Sintel 和 ScanNet，报告平均 L1 距离。
  - **视频深度**：Sintel、ScanNet、KITTI、Bonn，采用 scale-only 和 scale-and-shift 对齐后的 AbsRel。
  - **相机位姿**：Sintel、ScanNet、Re10K，报告 ATE、RPE-T、RPE-R、Pose AUC。
  - **效率**：测量不同目标 FPS 下可生成的最大 3D 跟踪数量，以及位姿估计速度。

- **对比方法**：
  - MegaSaM、DUSt3R、VGGT、MapAnything、SpatialTrackerV2、ε3、St4RTrack、CoTracker3 + UniDepthV2、CoTracker3 + VGGT、DELTA 等。

## 4. 资源与算力

- 文中明确提到：
  - 编码器使用 ViT-g 变体，40 层，时空 patch 大小 \(2\times16\times16\)。
  - 编码器约 1B 参数，解码器约 144M 参数。
  - 训练在 64 个 TPU 芯片上进行，local batch size 为 1，AdamW 优化器，训练 500k 步，耗时略超 2 天。
  - 推理效率实验在单张 A100 GPU 上测量，例如位姿估计超过 200 FPS。
- 未明确说明：
  - 总 GPU/TPU 小时数、能耗、单次实验完整成本。
  - 不同消融实验的具体算力开销。

## 5. 实验数量与充分性

- **主要实验数量**：
  - 定性分析：图 4 展示动态场景重建失败/成功案例，图 5 展示 in-the-wild 静态与动态视频，图 6 展示局部 patch 对深度细节的影响。
  - 定量主实验：表 3 跟踪吞吐，表 4 4D 跟踪，表 5 点云与深度，表 6 相机位姿。
  - 消融实验：表 7 局部 RGB patch，表 8 编码器规模 ViT-B/L/H/g，表 9 辅助损失。
  - 附录还提到公开数据训练、预训练编码器影响、亚像素精度等额外分析。
- **充分性**：
  - 覆盖多任务、多数据集、多指标，整体较充分。
  - 消融实验验证了局部 patch、编码器规模、辅助损失等关键设计。
  - 使用公开 benchmark 和标准协议，尽量公平。
- **潜在公平性问题**：
  - 训练使用内部数据集，完整复现困难。
  - 部分 baseline 在效率比较中被去除无关解码头，虽为公平加速，但可能与原始系统表现有差异。
  - 相机位姿、深度等评估依赖对齐方式，跨方法比较仍需谨慎。

## 6. 主要结论与发现

- D4RT 通过统一查询接口，在动态 4D 重建和跟踪上取得新 SOTA。
- 在 TAPVid-3D 的局部/世界坐标 3D 跟踪中，D4RT 显著优于 St4RTrack、SpatialTrackerV2、CoTracker3+深度/位姿等组合方法。
- 在点云重建、视频深度、相机位姿估计上均达到或超过现有方法：
  - 点云：Sintel 和 ScanNet 上 L1 最低。
  - 深度：Sintel 等数据集上 AbsRel 表现优异，动态场景尤其突出。
  - 位姿：Sintel、ScanNet、Re10K 上 ATE/RPE 和 Pose AUC 领先，速度远超 MegaSaM、VGGT 等。
- 效率方面：D4RT 可生成全视频 3D 跟踪，速度比 prior 方法快 18–300 倍；位姿估计超过 200 FPS，比 VGGT 快约 9 倍、比 MegaSaM 快约 100 倍。
- 局部 RGB patch 对保持细节、锐化边界和提升深度/位姿性能至关重要。
- 模型性能随 ViT 编码器规模从 ViT-B 到 ViT-g 提升，预训练 VideoMAEv2 权重对成功很关键。

## 7. 优点

- **统一架构**：单一编码器-解码器统一深度、点云、相机内外参、2D/3D 跟踪，无需多个任务专用解码器。
- **查询灵活**：支持稀疏或稠密解码，可在任意空间点和时间点独立查询，天然并行。
- **动态场景能力强**：能对动态区域建立对应，弥补 MegaSaM、VGGT、ε3 等方法的不足。
- **效率高**：轻量解码器与独立查询设计带来高吞吐，适合大规模训练和推理。
- **全局一致性设计**：通过固定全局场景表征和轻量独立解码，隐式鼓励编码器学习全局一致场景，而非依赖重型耦合解码。
- **实验较全面**：多数据集、多任务、多指标，包含定性、定量和消融分析。
- **工程实用性强**：提出占用网格稠密跟踪算法，避免冗余查询，获得 5–15 倍加速。

## 8. 不足与局限

- **数据依赖**：训练依赖多个内部数据集，公开数据消融虽保留 SOTA，但完整复现和公平比较仍受内部数据影响。
- **模型规模较大**：主模型编码器约 1B 参数，训练需 64 TPU 芯片、2 天以上，部署资源要求不低。
- **预训练依赖**：使用 VideoMAEv2 预训练权重对性能关键，随机初始化性能显著下降。
- **查询独立性的潜在限制**：作者强调独立查询优势，但查询间无交互可能限制某些需要全局联合优化的场景。
- **相机模型假设**：内参估计假设主点在图像中心、针孔模型，畸变场景需额外非线性精化。
- **评估覆盖有限**：主要在合成/室内/自动驾驶等 benchmark，极端长视频、严重遮挡、复杂非刚体、多相机变化等真实场景仍待验证。
- **公平性风险**：部分 baseline 被去除无关解码头以加速，且不同方法训练数据、预训练和实现细节不完全一致。
- **应用限制**：高 FPS 和全像素跟踪虽强，但在资源受限设备、实时大规模视频流上的实际部署仍需进一步验证。

（完）
