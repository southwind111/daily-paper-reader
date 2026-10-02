---
title: Uncertainty-Aware 3D Reconstruction for Dynamic Underwater Scenes
title_zh: 面向动态水下场景的不确定性感知三维重建
authors: "Rui Liu, Zhibo Duan, Jianzhe Gao, Yi Yang, Wenguan Wang"
date: 2026
publication_date: 2026
publication_date_precision: year
publication_date_source: conference year only; exact release date unverified
publication_date_kind: unknown
pdf: "https://openreview.net/pdf?id=96DTvuYq4h"
tags: ["query:dr"]
score: 9.0
evidence: 不确定性感知动态场实现水下四维重建
tldr: 水下三维重建受光散射与环境动态耦合影响，现有方法多假设刚性场景，难以刻画时间动态且对观测噪声敏感。本文提出不确定性感知动态场UDF，先用嵌入体介质场的三维高斯初始化规范表示，再映射到四维神经体素空间并查询时空特征，借助形变网络与介质偏移网络联合建模结构与视相关介质。实验表明该方法在动态水下场景中能更稳健地恢复随时间变化的几何与外观。其贡献在于将不确定性建模与四维表示结合，提升了复杂介质下动态重建的鲁棒性。
source: ICLR-2026-Accepted
selection_source: conference_retrieval
motivation: 水下重建受光散射与环境动态耦合困扰，现有刚性假设方法难以捕捉时间动态且对噪声敏感。
method: 提出不确定性感知动态场，用三维高斯初始化规范表示并映射到四维神经体素空间，结合形变与介质偏移网络编码时空特征。
result: 在动态水下场景中实现了对结构与视相关介质随时间变化的联合建模，提升了抗噪与动态恢复能力。
conclusion: 将不确定性建模与四维表示结合，为复杂介质下的动态重建提供了更鲁棒的方案。
---

## Abstract
Underwater 3D reconstruction remains challenging due to the intricate interplay between light scattering and environment dynamics. While existing methods yield plausible reconstruction with rigid scene assumptions, they struggle to capture temporal dynamics and remain sensitive to observation noise. In this work, we propose an Uncertainty-aware Dynamic Field (UDF) that jointly represents underwater structure and view-dependent medium over time. A canonical underwater representation is initialized using a set of 3D Gaussians embedded in a volumetric medium field. Then we map this representation into a 4D neural voxel space and encode spatial-temporal features by querying the voxels. Based on these features, a deformation network and a medium offset network are proposed to model transformations of Gaussians and time-conditioned updates to medium properties, respectively. To address input-dependent noise, we model per-pixel uncertainty guided by surface-view radiance ambiguity and inter-frame scene flow inconsistency. This uncertainty is incorporated into the rendering loss to suppress the noise from low-confidence observations during training. Experiments on both controlled and in-the-wild underwater datasets demonstrate our method achieves both high-quality reconstruction and novel view synthesis.

---

## 论文详细总结（自动生成）

### 1. 检索相关性
不确定性感知动态场实现水下四维重建。

### 2. 核心内容
水下三维重建受光散射与环境动态耦合影响，现有方法多假设刚性场景，难以刻画时间动态且对观测噪声敏感。本文提出不确定性感知动态场UDF，先用嵌入体介质场的三维高斯初始化规范表示，再映射到四维神经体素空间并查询时空特征，借助形变网络与介质偏移网络联合建模结构与视相关介质。实验表明该方法在动态水下场景中能更稳健地恢复随时间变化的几何与外观。其贡献在于将不确定性建模与四维表示结合，提升了复杂介质下动态重建的鲁棒性。

### 3. 对应检索需求
four-dimensional reconstruction of dynamic geometry over time。

### 4. 来源与原文
- Source：ICLR-2026-Accepted
- OpenReview：[https://openreview.net/forum?id=96DTvuYq4h](https://openreview.net/forum?id=96DTvuYq4h)
