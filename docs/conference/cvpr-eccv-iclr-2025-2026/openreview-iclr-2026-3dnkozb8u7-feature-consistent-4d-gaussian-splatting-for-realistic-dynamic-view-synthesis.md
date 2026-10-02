---
title: Feature Consistent 4D Gaussian Splatting for Realistic Dynamic View Synthesis
title_zh: 面向真实感动态视角合成的特征一致四维高斯泼溅
authors: "Boya Shi, Yuan Chang, Naiyang Guan"
date: 2026
publication_date: 2026
publication_date_precision: year
publication_date_source: conference year only; exact release date unverified
publication_date_kind: unknown
pdf: "https://openreview.net/pdf?id=3dNKozB8U7"
tags: ["query:dr"]
score: 8.0
evidence: 面向动态视角合成的特征一致四维高斯泼溅
tldr: 动态新视角合成因运动模式复杂而困难，四维高斯中时间维度进一步使约束构建复杂，导致渲染时间一致性不足。本文提出4D特征高斯泼溅F4DGS，引入特征一致性正则，联合同步层级语义特征、速度与深度，并将对齐扩展到连续单位时间区间以捕捉时间关联。实验表明其实现运动与外观一致的动态渲染，是首个显式耦合速度与深度的渲染算法，推动了真实感动态视角合成。
source: ICLR-2026-Rejected-Public
selection_source: conference_retrieval
motivation: 四维高斯中时间维度使约束难以构建，导致动态新视角合成的渲染时间一致性不足。
method: 提出F4DGS，引入特征一致性正则，联合同步层级语义特征、速度与深度，并扩展到连续时间区间的时间关联。
result: 实现运动与外观一致的动态渲染，提升时间一致性。
conclusion: 首次显式耦合速度与深度的渲染算法，推动真实感动态视角合成。
---

## Abstract
Dynamic novel view synthesis remains challenging due to the complexity of diverse motion patterns. In 4D Gaussians, the temporal dimension further complicates constraint formulation, making temporally consistent rendering difficult. To address this, we introduce 4D Feature Gaussian Splatting (F4DGS), a dynamic rendering algorithm that introduces feature consistency regularization to enable realistic rendering. This regularization jointly synchronizes hierarchical semantic features, velocity, and depth, ensuring coherent motion and appearance. We further extend the regularization beyond static alignment to capture temporal associations over continuous unit time intervals. F4DGS is the first rendering algorithm to explicitly couple velocity and depth for learning motion-consistent 4D representations, enabling high-fidelity, physically plausible rendering of dynamic content. Through comprehensive evaluations on monocular and multi-view dynamic datasets, F4DGS achieves real-time, high-resolution rendering and consistently outperforms existing methods across both quantitative and qualitative benchmarks. Notably, F4DGS achieves a 3.51 PSNR improvement on the Plenoptic dataset with comparable rendering speed and training time.

---

## 论文详细总结（自动生成）

### 1. 检索相关性
面向动态视角合成的特征一致四维高斯泼溅。

### 2. 核心内容
动态新视角合成因运动模式复杂而困难，四维高斯中时间维度进一步使约束构建复杂，导致渲染时间一致性不足。本文提出4D特征高斯泼溅F4DGS，引入特征一致性正则，联合同步层级语义特征、速度与深度，并将对齐扩展到连续单位时间区间以捕捉时间关联。实验表明其实现运动与外观一致的动态渲染，是首个显式耦合速度与深度的渲染算法，推动了真实感动态视角合成。

### 3. 对应检索需求
dynamic neural radiance fields and Gaussian splatting for reconstructing dynamic scenes。

### 4. 来源与原文
- Source：ICLR-2026-Rejected-Public
- OpenReview：[https://openreview.net/forum?id=3dNKozB8U7](https://openreview.net/forum?id=3dNKozB8U7)
