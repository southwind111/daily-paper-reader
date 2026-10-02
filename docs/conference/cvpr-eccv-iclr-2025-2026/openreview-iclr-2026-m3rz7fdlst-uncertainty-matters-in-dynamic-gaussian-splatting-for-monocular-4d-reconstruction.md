---
title: Uncertainty Matters in Dynamic Gaussian Splatting for Monocular 4D Reconstruction
title_zh: 不确定性在单目四维重建动态高斯泼溅中的重要性
authors: "Fengzhi Guo, Chih-Chuan Hsu, Sihao Ding, Cheng Zhang"
date: 2026
publication_date: 2026
publication_date_precision: year
publication_date_source: conference year only; exact release date unverified
publication_date_kind: unknown
pdf: "https://openreview.net/pdf?id=m3rZ7Fdlst"
tags: ["query:dr"]
score: 9.0
evidence: 不确定性感知动态高斯泼溅用于单目四维重建
tldr: 单目输入下重建动态三维场景本质欠约束，遮挡与极端新视角带来歧义。动态高斯泼溅虽高效，但原始模型对所有高斯统一优化，忽略其是否被充分观测，导致遮挡下运动漂移与新视角合成退化。本文提出USplat4D，一种不确定性感知的动态高斯泼溅框架，将跨视角与时间反复被观测的高斯视为可靠锚点以引导运动，而将可见性差的高斯视为不可靠并降低其影响。实验表明该方法缓解了遮挡下的运动漂移并改善了新视角合成质量。其贡献在于把不确定性引入动态高斯优化，提升单目四维重建的稳健性。
source: ICLR-2026-Accepted
selection_source: conference_retrieval
motivation: 单目动态重建受遮挡与新视角歧义约束，动态高斯泼溅对所有高斯统一优化导致运动漂移。
method: 提出不确定性感知动态高斯泼溅，将反复被观测的高斯作为可靠锚点引导运动，降低欠观测高斯的影响。
result: 缓解了遮挡下的运动漂移，改善了新视角合成与重建质量。
conclusion: 将不确定性引入动态高斯优化，提升了单目四维重建的稳健性。
---

## Abstract
Reconstructing dynamic 3D scenes from monocular input is fundamentally under-constrained, with ambiguities arising from occlusion and extreme novel views. While dynamic Gaussian Splatting offers an efficient representation, vanilla models optimize all Gaussian primitives uniformly, ignoring whether they are well or poorly observed. This limitation leads to motion drifts under occlusion and degraded synthesis when extrapolating to unseen views. We argue that uncertainty matters: Gaussians with recurring observations across views and time act as reliable anchors to guide motion, whereas those with limited visibility are treated as less reliable. To this end, we introduce USplat4D, a novel Uncertainty-aware dynamic Gaussian Splatting framework that propagates reliable motion cues to enhance 4D reconstruction. Our approach estimates time-varying per-Gaussian uncertainty and leverages it to construct a spatio-temporal graph for uncertainty-aware optimization. Experiments on diverse real and synthetic datasets show that explicitly modeling uncertainty consistently improves dynamic Gaussian Splatting models, yielding more stable geometry under occlusion and high-quality synthesis at extreme viewpoints. Project page: https://tamu-visual-ai.github.io/usplat4d/.

---

## 论文详细总结（自动生成）

### 1. 检索相关性
不确定性感知动态高斯泼溅用于单目四维重建。

### 2. 核心内容
单目输入下重建动态三维场景本质欠约束，遮挡与极端新视角带来歧义。动态高斯泼溅虽高效，但原始模型对所有高斯统一优化，忽略其是否被充分观测，导致遮挡下运动漂移与新视角合成退化。本文提出USplat4D，一种不确定性感知的动态高斯泼溅框架，将跨视角与时间反复被观测的高斯视为可靠锚点以引导运动，而将可见性差的高斯视为不可靠并降低其影响。实验表明该方法缓解了遮挡下的运动漂移并改善了新视角合成质量。其贡献在于把不确定性引入动态高斯优化，提升单目四维重建的稳健性。

### 3. 对应检索需求
four-dimensional reconstruction of dynamic geometry over time。

### 4. 来源与原文
- Source：ICLR-2026-Accepted
- OpenReview：[https://openreview.net/forum?id=m3rZ7Fdlst](https://openreview.net/forum?id=m3rZ7Fdlst)
