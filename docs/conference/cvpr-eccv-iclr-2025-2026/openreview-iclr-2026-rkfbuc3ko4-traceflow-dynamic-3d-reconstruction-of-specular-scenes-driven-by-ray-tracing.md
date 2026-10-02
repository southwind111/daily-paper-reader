---
title: "TraceFlow: Dynamic 3D Reconstruction of Specular Scenes Driven by Ray Tracing"
title_zh: TraceFlow：由光线追踪驱动的动态镜面场景三维重建
authors: "Jiachen Tao, Junyi Wu, Haoxuan Wang, Zongxin Yang, Dawen Cai, Yan Yan"
date: 2026
publication_date: 2026
publication_date_precision: year
publication_date_source: conference year only; exact release date unverified
publication_date_kind: unknown
pdf: "https://openreview.net/pdf?id=rkfbUc3kO4"
tags: ["query:dr"]
score: 8.0
evidence: 基于光线追踪的动态镜面场景三维重建
tldr: 动态镜面场景的高保真渲染面临反射方向估计不精确与反射建模不物理两大挑战。本文提出TraceFlow框架，采用残差材质增强的二维高斯泼溅表示来建模动态几何与材质属性，从而准确计算反射光线，并引入动态环境高斯与混合渲染管线，将渲染分解为漫反射与镜面分量，结合光栅化与光线追踪实现物理可信的镜面合成，同时设计由粗到细的训练策略提升优化稳定性。结果表明该方法在动态镜面场景中取得高保真渲染效果。其贡献在于把光线追踪与高斯表示结合，推进了动态外观与几何的联合重建。
source: ICLR-2026-Rejected-Public
selection_source: conference_retrieval
motivation: 动态镜面场景渲染需精确估计反射方向并物理准确地建模反射，现有方法难以兼顾。
method: 提出残差材质增强的二维高斯泼溅表示与动态环境高斯，配合光栅化加光线追踪的混合渲染及由粗到细训练。
result: 实现了动态几何与材质的联合建模，获得物理可信的高保真镜面渲染效果。
conclusion: 将光线追踪与高斯表示结合，为动态镜面场景的高质量重建与渲染提供了新途径。
---

## Abstract
We present TraceFlow, a novel framework for high-fidelity rendering of dynamic specular scenes by addressing two key challenges: precise reflection direction estimation and physically accurate reflection modeling. To achieve this, we propose a Residual Material-Augmented 2D Gaussian Splatting representation that models dynamic geometry and material properties, allowing accurate reflection ray computation. Furthermore, we introduce a Dynamic Environment Gaussian representation and a hybrid rendering pipeline that decomposes rendering into diffuse and specular components, enabling physically grounded specular synthesis via rasterization and ray tracing. Finally, we devise a coarse-to-fine training strategy to improve optimization stability and promote physically meaningful decomposition. Extensive experiments on dynamic scene benchmarks demonstrate that TraceFlow outperforms prior methods both quantitatively and qualitatively, producing sharper and more realistic specular reflections in complex dynamic environments.

---

## 论文详细总结（自动生成）

### 1. 检索相关性
基于光线追踪的动态镜面场景三维重建。

### 2. 核心内容
动态镜面场景的高保真渲染面临反射方向估计不精确与反射建模不物理两大挑战。本文提出TraceFlow框架，采用残差材质增强的二维高斯泼溅表示来建模动态几何与材质属性，从而准确计算反射光线，并引入动态环境高斯与混合渲染管线，将渲染分解为漫反射与镜面分量，结合光栅化与光线追踪实现物理可信的镜面合成，同时设计由粗到细的训练策略提升优化稳定性。结果表明该方法在动态镜面场景中取得高保真渲染效果。其贡献在于把光线追踪与高斯表示结合，推进了动态外观与几何的联合重建。

### 3. 对应检索需求
four-dimensional reconstruction of dynamic geometry over time。

### 4. 来源与原文
- Source：ICLR-2026-Rejected-Public
- OpenReview：[https://openreview.net/forum?id=rkfbUc3kO4](https://openreview.net/forum?id=rkfbUc3kO4)
