---
title: "Forge4D: Feed-Forward 4D Human Reconstruction and Interpolation from Uncalibrated Sparse Videos"
title_zh: Forge4D：从无标定稀疏视频的前馈4D人体重建与插值
authors: "Yingdong Hu, Yisheng He, Jinnan Chen, Weihao Yuan, Kejie Qiu, Zehong Lin, Siyu Zhu, Zilong Dong, Jun Zhang"
date: 2026
publication_date: 2026
publication_date_precision: year
publication_date_source: conference year only; exact release date unverified
publication_date_kind: unknown
pdf: "https://openreview.net/pdf?id=iRIoT8NUu2"
tags: ["query:dr"]
score: 10.0
evidence: 稀疏视频前馈4D人体重建与插值
tldr: 针对从无标定稀疏视角视频即时重建动态3D人体时现有方法速度慢或无法生成新时刻表示的问题，本文提出Forge4D前馈模型。它把4D重建与插值简化为流式3D高斯重建与稠密运动预测的联合任务，从稀疏视频高效重建时间对齐的表示。实验表明该模型同时支持新视角与新时刻合成，为动态人体重建及下游应用提供快速可扩展方案。
source: ICLR-2026-Public
selection_source: conference_retrieval
motivation: 从无标定稀疏视角视频即时重建动态3D人体，现有方法或速度慢，或无法生成新时刻表示。
method: 提出前馈模型Forge4D，将4D重建与插值化为流式3D高斯重建与稠密运动预测的联合任务。
result: 模型能高效重建时间对齐的表示，同时支持新视角与新时刻合成。
conclusion: 该工作实现了快速且可外推时间的4D人体重建，服务众多下游应用。
---

## Abstract
Instant reconstruction of dynamic 3D humans from uncalibrated sparse-view videos is critical for numerous downstream applications. Existing methods, however, are either limited by the slow reconstruction speeds or incapable of generating novel-time representations. To address these challenges, we propose *Forge4D*, a feed-forward 4D human reconstruction and interpolation model that efficiently reconstructs temporally aligned representations from uncalibrated sparse-view videos, enabling both novel view and novel time synthesis. Our model simplifies the 4D reconstruction and interpolation problem as a joint task of streaming 3D Gaussian reconstruction and dense motion prediction. For the task of streaming 3D Gaussian reconstruction, we first reconstruct static 3D Gaussians from uncalibrated sparse-view images and then introduce learnable state tokens to enforce temporal consistency in a memory-friendly manner by interactively updating shared information across different timestamps. 
To overcome the lack of the ground truth for dense motion supervision, we formulate dense motion prediction as a dense point matching task and introduce a self-supervised *retargeting loss* to optimize this module. An additional occlusion-aware *optical flow loss*  is introduced to ensure motion consistency with plausible human movement, providing stronger regularization. Extensive experiments demonstrate the effectiveness of our model on both in-domain and out-of-domain datasets.

---

## 论文详细总结（自动生成）

### 1. 检索相关性
稀疏视频前馈4D人体重建与插值。

### 2. 核心内容
针对从无标定稀疏视角视频即时重建动态3D人体时现有方法速度慢或无法生成新时刻表示的问题，本文提出Forge4D前馈模型。它把4D重建与插值简化为流式3D高斯重建与稠密运动预测的联合任务，从稀疏视频高效重建时间对齐的表示。实验表明该模型同时支持新视角与新时刻合成，为动态人体重建及下游应用提供快速可扩展方案。

### 3. 对应检索需求
four-dimensional reconstruction of dynamic geometry over time。

### 4. 来源与原文
- Source：ICLR-2026-Public
- OpenReview：[https://openreview.net/forum?id=iRIoT8NUu2](https://openreview.net/forum?id=iRIoT8NUu2)
