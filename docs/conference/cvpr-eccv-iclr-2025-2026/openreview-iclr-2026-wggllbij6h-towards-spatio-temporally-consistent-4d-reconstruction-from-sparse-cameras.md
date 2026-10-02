---
title: Towards Spatio-Temporally Consistent 4D Reconstruction from Sparse Cameras
title_zh: 面向稀疏相机的时空一致4D重建
authors: "Weihong Pan, Xiaoyu Zhang, Zhuang Zhang, Zhichao Ye, Nan Wang, Haomin Liu, Guofeng Zhang"
date: 2026
publication_date: 2026
publication_date_precision: year
publication_date_source: conference year only; exact release date unverified
publication_date_kind: unknown
pdf: "https://openreview.net/pdf?id=wgGlLBIJ6h"
tags: ["query:dr"]
score: 9.0
evidence: 稀疏相机的时空一致4D重建
tldr: 高质量4D重建通常依赖约20台以上同步相机阵列，昂贵的实验室配置严重限制其可扩展性。本文提出稀疏相机动态重建框架，利用丰富但不一致的生成观测，核心创新是时空畸变场，统一建模生成观测在空间与时间维度上的不一致性。实验表明该方法在稀疏相机条件下实现时空一致的4D重建，降低了对密集相机阵列的依赖。
source: ICLR-2026-Public
selection_source: conference_retrieval
motivation: 高质量4D重建依赖约20台同步相机阵列，成本高昂且限制可扩展性。
method: 提出利用生成观测的稀疏相机动态重建框架，设计时空畸变场建模空间与时间不一致性。
result: 在稀疏相机条件下实现时空一致的4D重建。
conclusion: 降低动态重建对密集相机阵列的依赖。
---

## Abstract
High-quality 4D reconstruction enables photorealistic and immersive rendering of the dynamic real world. However, unlike static scenes that can be fully captured with a single camera, high-quality dynamic scene benchmarks typically use dense arrays of approximately 20 synchronized cameras or more. The reliance on such costly lab setups severely limits practical scalability. To this end, we propose a sparse-camera dynamic reconstruction framework that exploits abundant yet inconsistent generative observations. Our key innovation is the Spatio-Temporal Distortion Field, which provides a unified mechanism for modeling inconsistencies in generative observations across both spatial and temporal dimensions. Building on this, we develop a complete pipeline that enables 4D reconstruction from sparse and uncalibrated camera inputs. We evaluate our method on multi-camera dynamic scene benchmarks, achieving spatio-temporally consistent high-fidelity renderings and significantly outperforming existing approaches.

---

## 论文详细总结（自动生成）

### 1. 检索相关性
稀疏相机的时空一致4D重建。

### 2. 核心内容
高质量4D重建通常依赖约20台以上同步相机阵列，昂贵的实验室配置严重限制其可扩展性。本文提出稀疏相机动态重建框架，利用丰富但不一致的生成观测，核心创新是时空畸变场，统一建模生成观测在空间与时间维度上的不一致性。实验表明该方法在稀疏相机条件下实现时空一致的4D重建，降低了对密集相机阵列的依赖。

### 3. 对应检索需求
reconstructing dynamic three-dimensional scenes from images or sensor data over time。

### 4. 来源与原文
- Source：ICLR-2026-Public
- OpenReview：[https://openreview.net/forum?id=wgGlLBIJ6h](https://openreview.net/forum?id=wgGlLBIJ6h)
