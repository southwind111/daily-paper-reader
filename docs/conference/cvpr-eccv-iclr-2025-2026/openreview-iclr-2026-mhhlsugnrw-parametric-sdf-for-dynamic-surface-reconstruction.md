---
title: Parametric SDF for Dynamic Surface Reconstruction
title_zh: 面向动态表面重建的参数化SDF
authors: "Chong Gao, Kai Ye, Qiyu Dai, Yiming Shao, Qiong Zeng, Ding Liang, Yan-Pei Cao, Guanbin Li, Wenzheng Chen"
date: 2026
publication_date: 2026
publication_date_precision: year
publication_date_source: conference year only; exact release date unverified
publication_date_kind: unknown
pdf: "https://openreview.net/pdf?id=mhHlsuGNRW"
tags: ["query:dr"]
score: 9.0
evidence: 面向动态表面的参数化SDF时序重建
tldr: 动态场景的高保真、时序一致表面重建仍是计算机视觉的难题，现有方法虽擅长新视角合成，却难以恢复准确几何，生成含噪或时序不一致的网格。本文提出参数化符号距离场，将静态SDF泛化为随时间演化的参数曲线，为捕捉复杂时序变化提供原则性建模方式。该方法能重建时序一致的动态表面几何，提升仿真与编辑等下游任务的可用性。
source: ICLR-2026-Rejected-Public
selection_source: conference_retrieval
motivation: 现有方法擅长新视角合成却难以恢复准确几何，动态场景网格常含噪且时序不一致。
method: 提出参数化符号距离场，将静态SDF泛化为随时间演化的参数曲线，建模复杂时序变化。
result: 该方法能重建高保真且时序一致的动态表面几何。
conclusion: 为动态表面重建及仿真、编辑等下游任务提供更可用的几何表示。
---

## Abstract
Reconstructing high-fidelity, temporally coherent surfaces of dynamic scenes remains a critical challenge in computer vision. While recent methods excel at novel view synthesis, they often fail to recover accurate geometry, yielding noisy or temporally inconsistent meshes that are suboptimal for downstream applications such as simulation or editing. In this work, we introduce a new paradigm for dynamic surface reconstruction based on a parametric Signed Distance Function ({\nameshort}). Our key insight is to generalize static SDF fields—where each spatial point stores a constant value—into time-dependent parametric curves, where each curve defines a temporally evolving SDF trajectory. Such a parametric SDF modeling provides a principled way to capture complex temporal variations, naturally enforcing smoothness and continuity in shape dynamics. At each timestamp, a static SDF field can be queried from {\nameshort} and converted into an explicit surface mesh via differentiable iso-surfacing. By rendering these meshes with a physically based differentiable renderer, we optimize the underlying parametric curves end-to-end against 2D image observations. Our framework produces high-fidelity, temporally coherent surfaces and inherently disentangles geometry, material, and lighting from multi-view videos. It robustly reconstructs geometry under large-scale motions and resolves appearance ambiguities caused by challenging lighting and occlusions. Experiments on both synthetic and real-world scenes demonstrate that our method achieves state-of-the-art geometric accuracy and temporal consistency, delivering delicate meshes that surpass prior work.

---

## 论文详细总结（自动生成）

### 1. 检索相关性
面向动态表面的参数化SDF时序重建。

### 2. 核心内容
动态场景的高保真、时序一致表面重建仍是计算机视觉的难题，现有方法虽擅长新视角合成，却难以恢复准确几何，生成含噪或时序不一致的网格。本文提出参数化符号距离场，将静态SDF泛化为随时间演化的参数曲线，为捕捉复杂时序变化提供原则性建模方式。该方法能重建时序一致的动态表面几何，提升仿真与编辑等下游任务的可用性。

### 3. 对应检索需求
four-dimensional reconstruction of dynamic geometry over time。

### 4. 来源与原文
- Source：ICLR-2026-Rejected-Public
- OpenReview：[https://openreview.net/forum?id=mhHlsuGNRW](https://openreview.net/forum?id=mhHlsuGNRW)
