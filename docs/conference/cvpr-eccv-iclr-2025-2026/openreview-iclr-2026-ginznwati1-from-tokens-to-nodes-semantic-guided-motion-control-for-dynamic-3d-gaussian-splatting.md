---
title: "From Tokens to Nodes: Semantic-Guided Motion Control for Dynamic 3D Gaussian Splatting"
title_zh: 从Token到节点：动态3D高斯泼溅的语义引导运动控制
authors: "Jianing Chen, Zehao Li, Yujun Cai, Hao Jiang, Shuqin Gao, Honglong Zhao, Tianlu Mao, Yucheng Zhang"
date: 2026
publication_date: 2026
publication_date_precision: year
publication_date_source: conference year only; exact release date unverified
publication_date_kind: unknown
pdf: "https://openreview.net/pdf?id=ginzNWATI1"
tags: ["query:dr"]
score: 9.0
evidence: 语义引导的动态3D高斯运动控制
tldr: 针对单目视频动态3D重建中视图不足导致运动推断歧义、建模时变场景计算开销大，以及稀疏控制点按几何分配造成静态冗余动态不足的问题，本文提出运动自适应框架。它利用视觉基础模型的语义与运动先验建立patch-token-node对应，并按运动复杂度压缩，把控制点集中在动态区域。实验表明该方法提升动态重建质量与效率，为高效动态高斯泼溅提供新思路。
source: ICLR-2026-Accepted
selection_source: conference_retrieval
motivation: 单目视频动态3D重建受限于视图不足的运动推断歧义与建模时变场景的计算开销，稀疏控制点按几何分配导致静态冗余、动态不足。
method: 提出运动自适应框架，利用视觉基础模型的语义与运动先验建立patch-token-node对应，并按运动复杂度进行压缩。
result: 该方法将控制点集中于动态区域，提升动态重建质量与效率。
conclusion: 语义引导的运动自适应控制为高效动态高斯重建提供新途径。
---

## Abstract
Dynamic 3D reconstruction from monocular videos remains difficult due to the ambiguity  inferring 3D motion from limited views and computational demands of modeling temporally varying scenes. While recent sparse control methods alleviate computation by reducing millions of Gaussians to thousands of control points, they suffer from a critical limitation: they allocate points purely by geometry, leading to static redundancy and dynamic insufficiency. We propose a motion-adaptive framework that aligns control density with motion complexity. Leveraging semantic and motion priors from vision foundation models, we establish patch-token-node correspondences and apply motion-adaptive compression to concentrate control points in dynamic regions while suppressing redundancy in static backgrounds. Our approach achieves flexible representational density adaptation through iterative voxelization and motion tendency scoring, directly addressing the fundamental mismatch between control point allocation and motion complexity. To capture temporal evolution, we introduce spline-based trajectory parameterization initialized by 2D tracklets, replacing MLP-based deformation fields to achieve smoother motion representation and more stable optimization. Extensive experiments demonstrate significant improvements in reconstruction quality and efficiency over existing state-of-the-art methods.

---

## 论文详细总结（自动生成）

### 1. 检索相关性
语义引导的动态3D高斯运动控制。

### 2. 核心内容
针对单目视频动态3D重建中视图不足导致运动推断歧义、建模时变场景计算开销大，以及稀疏控制点按几何分配造成静态冗余动态不足的问题，本文提出运动自适应框架。它利用视觉基础模型的语义与运动先验建立patch-token-node对应，并按运动复杂度压缩，把控制点集中在动态区域。实验表明该方法提升动态重建质量与效率，为高效动态高斯泼溅提供新思路。

### 3. 对应检索需求
temporal modeling for three-dimensional reconstruction of moving objects and scenes。

### 4. 来源与原文
- Source：ICLR-2026-Accepted
- OpenReview：[https://openreview.net/forum?id=ginzNWATI1](https://openreview.net/forum?id=ginzNWATI1)
