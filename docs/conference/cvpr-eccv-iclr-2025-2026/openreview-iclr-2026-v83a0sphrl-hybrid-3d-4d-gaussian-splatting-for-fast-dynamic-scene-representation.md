---
title: Hybrid 3D-4D Gaussian Splatting for Fast Dynamic Scene Representation
title_zh: 用于快速动态场景表示的混合三维—四维高斯泼溅
authors: "Seungjun Oh, Minseo Lee, Byeonghyeon Lee, Younggeun Lee, Hyejin Jeon, Eunbyung Park"
date: 2026
publication_date: 2026
publication_date_precision: year
publication_date_source: conference year only; exact release date unverified
publication_date_kind: unknown
pdf: "https://openreview.net/pdf?id=V83a0sPhRl"
tags: ["query:dr"]
score: 9.0
evidence: 用于快速动态场景表示的混合三维—四维高斯泼溅
tldr: 动态三维场景重建已能实现高保真新视角合成，但现有四维高斯泼溅方法因向静态区域冗余分配四维高斯而带来巨大的计算与显存开销，甚至降低图像质量。本文提出混合三维—四维高斯泼溅框架3D-4DGS，自适应地用三维高斯表示静态区域，仅在动态元素上保留四维高斯。该方法在保持高保真时空变化建模的同时显著降低开销，实现了快速动态场景表示。
source: ICLR-2026-Public
selection_source: conference_retrieval
motivation: 现有四维高斯泼溅向静态区域冗余分配高斯，导致计算与显存开销大且降低画质。
method: 提出混合三维—四维高斯泼溅框架，静态区域用三维高斯、动态元素用四维高斯。
result: 在保持高保真时空变化建模的同时降低计算与存储开销，实现快速表示。
conclusion: 为高效动态场景表示提供了自适应的高斯分配方案。
---

## Abstract
Recent advancements in dynamic 3D scene reconstruction have shown promising results, enabling high-fidelity 3D novel view synthesis with improved temporal consistency. Among these, 4D Gaussian Splatting (4DGS) has emerged as an appealing approach due to its ability to model high-fidelity spatial and temporal variations. However, existing methods suffer from substantial computational and memory overhead due to the redundant allocation of 4D Gaussians to static regions, which can also degrade image quality. In this work, we introduce hybrid 3D–4D Gaussian Splatting (3D-4DGS), a novel framework that adaptively represents static regions with 3D Gaussians while reserving 4D Gaussians for dynamic elements. Our method begins with a fully 4D Gaussian representation and iteratively converts temporally invariant Gaussians into 3D, significantly reducing the number of parameters and improving computational efficiency. Meanwhile, dynamic Gaussians retain their full 4D representation, capturing complex motions with high fidelity. Our approach achieves significantly faster training times compared to baseline 4D Gaussian Splatting methods while maintaining or improving the visual quality.

---

## 论文详细总结（自动生成）

### 1. 检索相关性
用于快速动态场景表示的混合三维—四维高斯泼溅。

### 2. 核心内容
动态三维场景重建已能实现高保真新视角合成，但现有四维高斯泼溅方法因向静态区域冗余分配四维高斯而带来巨大的计算与显存开销，甚至降低图像质量。本文提出混合三维—四维高斯泼溅框架3D-4DGS，自适应地用三维高斯表示静态区域，仅在动态元素上保留四维高斯。该方法在保持高保真时空变化建模的同时显著降低开销，实现了快速动态场景表示。

### 3. 对应检索需求
dynamic neural radiance fields and Gaussian splatting for reconstructing dynamic scenes。

### 4. 来源与原文
- Source：ICLR-2026-Public
- OpenReview：[https://openreview.net/forum?id=V83a0sPhRl](https://openreview.net/forum?id=V83a0sPhRl)
