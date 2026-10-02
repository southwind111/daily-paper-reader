---
title: "STDR: Spatio-Temporal Decoupling for Real-Time Dynamic Scene Rendering"
title_zh: STDR：面向实时动态场景渲染的时空解耦
authors: "Zehao Li, Hao Jiang, Yujun Cai, Jianing Chen, Baolong Bi, Shuqin Gao, Honglong Zhao, Yiwei Wang, Tianlu Mao, Zhaoqi Wang"
date: 2026
publication_date: 2026
publication_date_precision: year
publication_date_source: conference year only; exact release date unverified
publication_date_kind: unknown
pdf: "https://openreview.net/pdf?id=behsr8o1Xz"
tags: ["query:dr"]
score: 9.0
evidence: 时空解耦的实时动态场景渲染
tldr: 动态场景重建长期是三维视觉的基础难题，3D高斯泼溅虽带来高质量实时渲染，但现有动态重建方法在初始化时存在时空不一致，导致表示时空纠缠、难以准确建模运动。本文提出STDR时空解耦模块，作为即插即用组件学习解耦的时空表示。该方法缓解了初始化阶段的时空纠缠问题，提升了动态运动的建模精度与实时渲染质量。
source: ICLR-2026-Rejected-Public
selection_source: conference_retrieval
motivation: 3DGS动态重建方法在初始化时存在时空不一致，导致表示时空纠缠、运动建模不准。
method: 提出STDR即插即用时空解耦模块，学习解耦的时空高斯表示。
result: 缓解初始化阶段的时空纠缠，提升动态运动建模与实时渲染质量。
conclusion: 为实时动态场景渲染提供有效的时空解耦方案。
---

## Abstract
Although dynamic scene reconstruction has long been a fundamental challenge in 3D vision, the recent emergence of 3D Gaussian Splatting (3DGS) offers a promising direction by enabling high-quality, real-time rendering through explicit Gaussian primitives. However, existing 3DGS-based methods for dynamic reconstruction often suffer from spatio-temporal incoherence during initialization, where canonical Gaussians are constructed by aggregating observations from multiple frames without temporal distinction. This results in spatio-temporally entangled representations, making it difficult to model dynamic motion accurately. To overcome this limitation, we propose STDR (Spatio-Temporal Decoupling for Real-time rendering), a plug-and-play module that learns spatio-temporal probability distributions for each Gaussian. STDR introduces a spatio-temporal mask, a separated deformation field, and a consistency regularization to jointly disentangle spatial and temporal patterns. Extensive experiments demonstrate that incorporating our module into existing 3DGS-based dynamic scene reconstruction frameworks leads to notable improvements in both reconstruction quality and spatio-temporal consistency across synthetic and real-world benchmarks.

---

## 论文详细总结（自动生成）

### 1. 检索相关性
时空解耦的实时动态场景渲染。

### 2. 核心内容
动态场景重建长期是三维视觉的基础难题，3D高斯泼溅虽带来高质量实时渲染，但现有动态重建方法在初始化时存在时空不一致，导致表示时空纠缠、难以准确建模运动。本文提出STDR时空解耦模块，作为即插即用组件学习解耦的时空表示。该方法缓解了初始化阶段的时空纠缠问题，提升了动态运动的建模精度与实时渲染质量。

### 3. 对应检索需求
real-time reconstruction of dynamic 3D objects and scenes。

### 4. 来源与原文
- Source：ICLR-2026-Rejected-Public
- OpenReview：[https://openreview.net/forum?id=behsr8o1Xz](https://openreview.net/forum?id=behsr8o1Xz)
