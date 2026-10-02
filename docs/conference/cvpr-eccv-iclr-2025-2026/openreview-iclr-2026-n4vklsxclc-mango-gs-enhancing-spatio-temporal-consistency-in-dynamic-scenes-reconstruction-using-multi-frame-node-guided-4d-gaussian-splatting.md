---
title: "Mango-GS: Enhancing Spatio-Temporal Consistency in Dynamic Scenes Reconstruction using Multi-Frame Node-Guided 4D Gaussian Splatting"
title_zh: Mango-GS：多帧节点引导四维高斯泼溅提升动态场景重建时空一致性
authors: "Tingxuan Huang, Haowei Zhu, Jun-Hai Yong, Hao Pan, Bin Wang"
date: 2026
publication_date: 2026
publication_date_precision: year
publication_date_source: conference year only; exact release date unverified
publication_date_kind: unknown
pdf: "https://openreview.net/pdf?id=N4VKlSxCLc"
tags: ["query:dr"]
score: 9.0
evidence: 多帧节点引导四维高斯泼溅提升时空一致性
tldr: 高保真且时序一致的动态三维场景重建仍是难题，现有高斯泼溅方法多依赖逐帧优化，易过拟合瞬时状态而学不到真实运动动态。本文提出Mango-GS，一种多帧、节点引导的框架，利用时间Transformer在一段帧窗口内学习复杂运动依赖以生成合理轨迹，并将时序建模限制在稀疏控制节点上以提升效率，这些节点被设计为可解耦表示。实验表明该方法增强了动态场景重建的时空一致性。其贡献在于以多帧时序建模替代逐帧优化，实现更高质量的四维重建。
source: ICLR-2026-Accepted
selection_source: conference_retrieval
motivation: 现有高斯泼溅逐帧优化易过拟合瞬时状态，难以学习真实运动动态，时空一致性不足。
method: 提出多帧节点引导框架，用时间Transformer在稀疏控制节点上学习跨帧运动依赖以生成合理轨迹。
result: 提升了动态场景重建的时空一致性与轨迹合理性，同时保持较高效率。
conclusion: 以多帧时序建模替代逐帧优化，实现更高质量的四维动态重建。
---

## Abstract
Reconstructing dynamic 3D scenes with photorealistic detail and temporal coherence remains a significant challenge. Existing Gaussian splatting approaches modeling scenes rely on per-frame optimization, causing them to overfit to instantaneous states rather than learning true motion dynamics. To address this, we present Mango-GS, a multi-frame, node-guided framework for high-fidelity 4D reconstruction. Our approach leverages a temporal Transformer to learn complex motion dependencies across a window of frames, ensuring the generation of plausible trajectories. For efficiency, this temporal modeling is confined to a sparse set of control nodes. These nodes are uniquely designed with  decoupled position and latent codes, which provide a stable semantic anchor for motion influence and prevents correspondence errors for large movements. Our framework is trained end-to-end, enhanced by a input masking strategy and two multi-frame loss to ensure robustness. Extensive experiments demonstrate that Mango-GS achieves state-of-the-art quality and fast rendering speed, enabling high-fidelity reconstruction and real-time rendering of dynamic scenes.

---

## 论文详细总结（自动生成）

### 1. 检索相关性
多帧节点引导四维高斯泼溅提升时空一致性。

### 2. 核心内容
高保真且时序一致的动态三维场景重建仍是难题，现有高斯泼溅方法多依赖逐帧优化，易过拟合瞬时状态而学不到真实运动动态。本文提出Mango-GS，一种多帧、节点引导的框架，利用时间Transformer在一段帧窗口内学习复杂运动依赖以生成合理轨迹，并将时序建模限制在稀疏控制节点上以提升效率，这些节点被设计为可解耦表示。实验表明该方法增强了动态场景重建的时空一致性。其贡献在于以多帧时序建模替代逐帧优化，实现更高质量的四维重建。

### 3. 对应检索需求
dynamic neural radiance fields and Gaussian splatting for reconstructing dynamic scenes。

### 4. 来源与原文
- Source：ICLR-2026-Accepted
- OpenReview：[https://openreview.net/forum?id=N4VKlSxCLc](https://openreview.net/forum?id=N4VKlSxCLc)
