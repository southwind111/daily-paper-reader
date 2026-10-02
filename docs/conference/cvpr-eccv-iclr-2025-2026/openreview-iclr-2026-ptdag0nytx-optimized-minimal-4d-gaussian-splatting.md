---
title: Optimized Minimal 4D Gaussian Splatting
title_zh: 优化的极简四维高斯泼溅
authors: "Minseo Lee, Byeonghyeon Lee, Lucas Yunkyu Lee, Eunsoo Lee, Sangmin Kim, Seunghyeon Song, Joo Chan Lee, Jong Hwan Ko, Jaesik Park, Eunbyung Park"
date: 2026
publication_date: 2026
publication_date_precision: year
publication_date_source: conference year only; exact release date unverified
publication_date_kind: unknown
pdf: "https://openreview.net/pdf?id=PTDaG0NytX"
tags: ["query:dr"]
score: 8.0
evidence: 用于动态场景表示与实时渲染的四维高斯泼溅
tldr: 四维高斯泼溅为动态场景表示带来实时渲染能力，但高保真重建需数百万高斯，存储开销巨大，现有压缩方法在压缩率或视觉质量上仍有局限。本文提出OMG4框架，通过高斯采样与渐进剪枝三阶段构建能忠实表示四维高斯模型的紧凑显著高斯集合。实验显示其在压缩率与视觉质量上均优于现有方法，有效缓解存储负担，为四维高斯动态表示的轻量化提供了有效方案。
source: ICLR-2026-Rejected-Public
selection_source: conference_retrieval
motivation: 四维高斯泼溅实现动态场景实时渲染，但高保真重建需数百万高斯，存储开销巨大。
method: 提出OMG4框架，通过高斯采样、剪枝等三阶段渐进式剪枝，构建能忠实表示四维高斯模型的紧凑显著高斯集合。
result: 在压缩率与视觉质量上均优于现有方法，缓解存储负担。
conclusion: 为四维高斯动态表示的轻量化与高效存储提供有效方案。
---

## Abstract
4D Gaussian Splatting has emerged as a new paradigm for dynamic scene representation, enabling real-time rendering of scenes with complex motions. However, it faces a major challenge of storage overhead, as millions of Gaussians are required for high-fidelity reconstruction. While several studies have attempted to alleviate this memory burden, they still face limitations in compression ratio or visual quality.
In this work, we present $\textit{OMG4}$ (Optimized Minimal 4D Gaussian Splatting), a framework that constructs a compact set of salient Gaussians capable of faithfully representing 4D Gaussian models.
Our method progressively prunes Gaussians in three stages: (1) $\textit{Gaussian Sampling}$ to identify primitives critical to reconstruction fidelity, (2) $\textit{Gaussian Pruning}$ to remove redundancies, and (3) $\textit{Gaussian Merging}$ to fuse primitives with similar characteristics.
In addition, we integrate implicit appearance compression and generalize Sub-Vector Quantization (SVQ) to 4D representations, further reducing storage while preserving quality.
Extensive experiments on standard benchmark datasets demonstrate that $\textit{OMG4}$ significantly outperforms recent state-of-the-art methods, reducing model sizes by over 60\% while maintaining reconstruction quality.
These results position $\textit{OMG4}$ as a significant step forward in compact 4D scene representation, opening new possibilities for a wide range of applications.

---

## 论文详细总结（自动生成）

### 1. 检索相关性
用于动态场景表示与实时渲染的四维高斯泼溅。

### 2. 核心内容
四维高斯泼溅为动态场景表示带来实时渲染能力，但高保真重建需数百万高斯，存储开销巨大，现有压缩方法在压缩率或视觉质量上仍有局限。本文提出OMG4框架，通过高斯采样与渐进剪枝三阶段构建能忠实表示四维高斯模型的紧凑显著高斯集合。实验显示其在压缩率与视觉质量上均优于现有方法，有效缓解存储负担，为四维高斯动态表示的轻量化提供了有效方案。

### 3. 对应检索需求
dynamic neural radiance fields and Gaussian splatting for reconstructing dynamic scenes。

### 4. 来源与原文
- Source：ICLR-2026-Rejected-Public
- OpenReview：[https://openreview.net/forum?id=PTDaG0NytX](https://openreview.net/forum?id=PTDaG0NytX)
