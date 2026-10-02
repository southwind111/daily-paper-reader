---
title: "SplitGaussian: Reconstructing Dynamic Scenes via Visual Geometry Decomposition"
title_zh: SplitGaussian：通过视觉几何分解重建动态场景
authors: "Jiahui Li, Shengeng Tang, Jingxuan He, Gang Huang, Zhangye Wang, Yantao Pan, Lechao Cheng"
date: 2026
publication_date: 2026
publication_date_precision: year
publication_date_source: conference year only; exact release date unverified
publication_date_kind: unknown
pdf: "https://openreview.net/pdf?id=3XGqsfKIIK"
tags: ["query:dr"]
score: 9.0
evidence: 几何分解重建单目动态场景
tldr: 针对单目视频动态场景重建中非刚性运动、遮挡、外观变化与缺乏深度监督等难题，以及NeRF计算低效、3DGS统一形变场易产生运动串扰的问题，本文提出SplitGaussian。它通过视觉几何分解将静态与动态元素分离建模，避免运动渗漏。实验表明该方法在保持3DGS实时渲染效率的同时提升动态场景重建质量，为高效稳定的单目动态重建提供新思路。
source: ICLR-2026-Public
selection_source: conference_retrieval
motivation: 单目视频动态场景重建面临非刚性运动、遮挡、外观变化与缺乏深度监督，NeRF效率低，3DGS统一形变场又易产生运动串扰。
method: 提出SplitGaussian，通过视觉几何分解将静态与动态元素分离建模，避免统一形变场的运动渗漏。
result: 该方法在保持3DGS实时渲染效率的同时提升动态场景重建质量。
conclusion: 几何分解为高效、稳定的单目动态重建提供了新思路。
---

## Abstract
Reconstructing dynamic 3D scenes from monocular videos remains a fundamentally challenging problem due to the presence of non-rigid motion, occlusion, appearance variation, and the absence of direct depth supervision. While neural radiance fields (NeRFs) have achieved remarkable results in static scene reconstruction, their computational inefficiency and per-scene optimization make them less practical for large-scale or real-time dynamic applications. Recent advances in 3D Gaussian Splatting (3DGS) provide a more efficient alternative, offering real-time rendering and faster convergence. However, existing 3DGS-based methods typically employ a unified deformation field to model both static and dynamic elements, often leading to motion bleeding, geometric artifacts, and temporal instability. In this paper, we propose SplitGaussian, a novel framework for monocular dynamic scene reconstruction that explicitly separates static and dynamic components within the 3DGS paradigm. By decoupling the learning of deformation for moving and non-moving regions, our method mitigates interference between motion modeling and static geometry preservation. We introduce independent deformation networks for each component, enabling precise motion representation while maintaining the integrity of static regions. Furthermore, to improve rendering quality and training stability, we propose a render-frequency-aware pruning strategy that filters out unreliable or redundant Gaussians with minimal visual contribution. Experiments on complex dynamic scenes demonstrate that our method achieves superior visual fidelity, temporal consistency, and training stability compared to recent baselines. Our approach represents a step toward scalable and artifact-free dynamic reconstruction using Gaussian-based representations.

---

## 论文详细总结（自动生成）

### 1. 检索相关性
几何分解重建单目动态场景。

### 2. 核心内容
针对单目视频动态场景重建中非刚性运动、遮挡、外观变化与缺乏深度监督等难题，以及NeRF计算低效、3DGS统一形变场易产生运动串扰的问题，本文提出SplitGaussian。它通过视觉几何分解将静态与动态元素分离建模，避免运动渗漏。实验表明该方法在保持3DGS实时渲染效率的同时提升动态场景重建质量，为高效稳定的单目动态重建提供新思路。

### 3. 对应检索需求
methods for non rigid and deformable 3D reconstruction of moving objects。

### 4. 来源与原文
- Source：ICLR-2026-Public
- OpenReview：[https://openreview.net/forum?id=3XGqsfKIIK](https://openreview.net/forum?id=3XGqsfKIIK)
