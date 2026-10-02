---
title: "HiMoR: Monocular Deformable Gaussian Reconstruction with Hierarchical Motion Representation"
title_zh: HiMoR：基于层次运动表示的单目可变形高斯重建
authors: "Liang, Yiming, Xu, Tianhan, Kikuchi, Yuta"
date: 2025
publication_date: 2025
publication_date_precision: year
publication_date_source: conference year only; exact release date unverified
publication_date_kind: unknown
pdf: "https://openaccess.thecvf.com/content/CVPR2025/papers/Liang_HiMoR_Monocular_Deformable_Gaussian_Reconstruction_with_Hierarchical_Motion_Representation_CVPR_2025_paper.pdf"
tags: ["query:dr"]
score: 9.0
evidence: 基于运动表示的单目可变形高斯重建
tldr: 单目动态三维重建中，如何表示三维高斯图元的形变以刻画复杂运动是关键。HiMoR提出层次运动表示，将日常场景运动分解为由粗到细的层级，用树结构节点表示不同细节层次的运动，浅层节点建模平滑的粗运动，深层节点捕捉精细运动，并以少量共享运动基表示节点运动。该设计假设运动平滑且简单，实现了高质量单目动态重建。
source: CVPR-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-liang-himor-monocular-deformable-gaussian-reconstruction-with-hierarchical-motion-representation-cvpr-2025-paper/fig-001.webp\", \"caption\": \"\", \"page\": 3, \"index\": 1, \"width\": 1883, \"height\": 869}]"
motivation: 单目动态三维重建中，三维高斯图元的形变表示难以兼顾粗运动平滑与精细运动细节。
method: HiMoR提出树结构层次运动表示，浅层节点建模粗运动，深层节点捕捉精细运动，并以少量共享运动基表示节点运动。
result: 该表示假设运动平滑简单，实现高质量单目动态三维重建。
conclusion: 为可变形高斯重建提供了有效的层次化运动表示。
---

## Abstract
We present Hierarchical Motion Representation (HiMoR), a novel deformation representation for 3D Gaussian primitives capable of achieving high-quality monocular dynamic 3D reconstruction. The insight behind HiMoR is that motions in everyday scenes can be decomposed into coarser motions that serve as the foundation for finer details. Using a tree structure, HiMoR's nodes represent different levels of motion detail, with shallower nodes modeling coarse motion for temporal smoothness and deeper nodes capturing finer motion. Additionally, our model uses a few shared motion bases to represent motions of different sets of nodes, aligning with the assumption that motion tends to be smooth and simple. This motion representation design provides Gaussians with a more structured deformation, maximizing the use of temporal relationships to tackle the challenging task of monocular dynamic 3D reconstruction. We also propose using a more reliable perceptual metric as an alternative, given that pixel-level metrics for evaluating monocular dynamic 3D reconstruction can sometimes fail to accurately reflect the true quality of reconstruction. Extensive experiments demonstrate our method's efficacy in achieving superior novel view synthesis from challenging monocular videos with complex motions.

---

## 论文详细总结（自动生成）

# HiMoR 论文总结

## 1. 论文的核心问题与整体含义

- **研究背景**：动态 3D 场景重建目标是从视频中恢复几何、外观与运动，实现自由视角渲染。3D Gaussian Splatting（3DGS）推动了静态与动态场景重建，但**单目视频**因缺少多视角一致性约束、信息不足，仍是极具挑战的任务。
- **核心问题**：如何为 3D 高斯图元设计合理的**形变/运动表示**，在单目动态重建中同时保持时空平滑性、细节表达能力，并避免过拟合或几何塌陷。
- **现有方法局限**：
  - SoM 等使用全局共享运动基，符合运动低秩假设，但全局基数量有限，难以捕捉精细运动。
  - MoSca 等使用大量 3D 运动节点，自由度高，容易过拟合训练视角。
  - NeRF 类形变场平滑但细节不足，常产生模糊结果；3DGS 类形变场也可能过平滑或计算慢。
- **整体含义**：论文提出 **HiMoR（Hierarchical Motion Representation）**，将日常场景运动分解为“粗到细”的层次结构，为高斯提供更结构化的形变表示，从而提升单目动态 3D 重建的新视角合成与跟踪质量。

## 2. 论文提出的方法论

- **核心思想**：
  - 运动可分解为粗运动与细运动：浅层节点建模平滑、粗粒度运动；深层节点捕捉精细、局部运动。
  - 使用树结构表示运动层级，每个节点表示相对于父节点的 **SE(3) 运动序列**，根节点固定在世界坐标原点。
  - 运动具有低秩、平滑、简单的特点，因此用少量共享运动基表示不同节点集合的运动。
- **关键技术细节**：
  - **层次运动表示**：节点运动定义为共享运动基的线性组合：  
    \(D = \sum_{m=1}^{M} v_m B_m\)，其中 \(B_m\) 是运动基，\(v_m\) 是节点系数。全局运动通过沿树结构组合相对 SE(3) 变换得到。
  - **高斯形变**：叶节点拥有最精细运动，每个高斯的形变由其 K 近邻叶节点运动插值得到：  
    \(T = \sum_{k \in N(G,V)} w_k D_k\)。权重 \(w_k\) 基于高斯中心与节点位置的距离，用高斯函数计算，并使用**双四元数**提升插值质量。
  - **初始化**：
    - 使用预训练 2D 跟踪和深度估计，将前景 2D 轨迹反投影为 3D 轨迹。
    - 对 3D 轨迹做 K-Means，得到 M 个聚类中心轨迹；通过 Procrustes 求解得到 M 个 SE(3) 运动基。
    - 选择可见 3D 轨迹最多的帧为 canonical frame；节点位置从 3D 轨迹采样，系数按到运动基中心的距离做反距离加权初始化。
    - 更细层级节点在优化中逐步加入：对周围高斯的相对运动聚类，得到子节点运动基，子节点从周围高斯子采样。
  - **节点致密化**：
    - 仅靠光度梯度可能导致颜色均匀但节点稀疏区域缺少节点。
    - 论文用轨迹间**曲线距离**衡量节点密度：  
      \(d_{curve}(X,Y)=\max_{t=1...T}\|x_t-y_t\|\)。
    - 对曲线距离超过阈值的高斯周围添加新节点，后期再结合梯度进行节点增删。
  - **损失设计**：
    - 总损失包括渲染损失 \(L_{rgb}\)、前景掩码损失 \(L_{mask}\)、深度损失 \(L_{depth}\)、跟踪损失 \(L_{track}\)、刚性损失 \(L_{rigid}\)。
    - **分层刚性约束**：浅层节点施加更强刚性约束以保持粗运动平滑，深层节点约束更弱以保留细节。
  - **感知评估指标**：提出用 CLIP-I、CLIP-T 等感知指标补充 PSNR 等像素级指标，因为单目动态重建中深度歧义、相机参数误差等会导致像素错位，PSNR 未必反映真实质量。

## 3. 实验设计

- **数据集/场景**：
  - **iPhone 数据集**：包含 14 个场景，其中 7 个有多相机捕获。论文遵循 SoM 设置，使用 5 个场景，排除 2 个相机参数不准确场景。
  - **Nvidia 数据集**：7 个场景，12 相机 rig。论文采用严格单目设置：相机 4 视频训练，相机 3、5、6 用于评估。
- **Benchmark 与指标**：
  - iPhone：CLIP-I、CLIP-T、LPIPS、PCK-T。CL
