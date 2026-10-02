---
title: "StreamSplat: Towards Online Dynamic 3D Reconstruction from Uncalibrated Video Streams"
title_zh: StreamSplat：面向无标定视频流的在线动态三维重建
authors: "Zike Wu, Qi Yan, Xuanyu Yi, Lele Wang, Renjie Liao"
date: 2026
publication_date: 2026
publication_date_precision: year
publication_date_source: conference year only; exact release date unverified
publication_date_kind: unknown
pdf: "https://openreview.net/pdf?id=SaiDRQU7Ez"
tags: ["query:dr"]
score: 9.0
evidence: 从未标定视频流在线重建动态三维高斯表示
tldr: 现有动态重建方法多依赖整段序列的小时级逐场景优化，难以在严格时延与内存约束下在线部署。本文提出StreamSplat前馈框架，通过概率采样机制从无标定输入稳健预测三维高斯，并结合双向变形建模，将任意长度视频流即时转化为动态3DGS表示。该方法实现了在线、实时的动态三维重建，显著降低了对逐场景优化的依赖，推动了动态重建的实际部署。
source: ICLR-2026-Accepted
selection_source: conference_retrieval
motivation: 动态重建方法多依赖整段序列的逐场景长时间优化，难以满足在线部署的时延与内存约束。
method: 提出全前馈框架，用概率采样从无标定输入预测三维高斯，并用双向变形建模将视频流即时转为动态3DGS。
result: 可将任意长度无标定视频流在线、即时地重建为动态三维高斯表示，无需逐场景优化。
conclusion: 实现了在线实时的动态三维重建，降低了动态重建方法的部署门槛。
---

## Abstract
Real-time reconstruction of dynamic 3D scenes from uncalibrated video streams demands robust online methods that recover scene dynamics from sparse observations under strict latency and memory constraints. Yet most dynamic reconstruction methods rely on hours of per-scene optimization under full-sequence access, limiting practical deployment.
In this work, we introduce **StreamSplat**, a fully feed-forward framework that instantly transforms uncalibrated video streams of arbitrary length into dynamic 3D Gaussian Splatting (3DGS) representations in an online manner. 
It is achieved via three key technical innovations: 1) a probabilistic sampling mechanism that robustly predicts 3D Gaussians from uncalibrated inputs; 2) a bidirectional deformation field that yields reliable associations across frames and mitigates long-term error accumulation; 3) an adaptive Gaussian fusion operation that propagates persistent Gaussians while handling emerging and vanishing ones.
Extensive experiments on standard dynamic and static benchmarks demonstrate that StreamSplat achieves state-of-the-art reconstruction quality and dynamic scene modeling. Uniquely, our method supports the online reconstruction of arbitrarily long video streams with a $1200\times$ speedup over optimization-based methods. 
Our code and models are available at https://streamsplat3d.github.io/.

---

## 论文详细总结（自动生成）

### 1. 检索相关性
从未标定视频流在线重建动态三维高斯表示。

### 2. 核心内容
现有动态重建方法多依赖整段序列的小时级逐场景优化，难以在严格时延与内存约束下在线部署。本文提出StreamSplat前馈框架，通过概率采样机制从无标定输入稳健预测三维高斯，并结合双向变形建模，将任意长度视频流即时转化为动态3DGS表示。该方法实现了在线、实时的动态三维重建，显著降低了对逐场景优化的依赖，推动了动态重建的实际部署。

### 3. 对应检索需求
papers on dynamic 3D reconstruction that recover time varying geometry from video or sensor sequences。

### 4. 来源与原文
- Source：ICLR-2026-Accepted
- OpenReview：[https://openreview.net/forum?id=SaiDRQU7Ez](https://openreview.net/forum?id=SaiDRQU7Ez)
