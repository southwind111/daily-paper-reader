---
title: "SurstSplat: Dynamic Surgical Gaussian Reconstruction  with Spatiotemporal Graph Matching"
title_zh: SurstSplat：基于时空图匹配的动态外科高斯重建
authors: "Chenxin Li, Hengyu Liu, Zhiqin Yang, Yifan Liu, Wuyang Li, Kai Yang, Xiao Xu, Xingzhong Xu, Zhiwen Fan, Yixuan Yuan"
date: 2026
publication_date: 2026
publication_date_precision: year
publication_date_source: conference year only; exact release date unverified
publication_date_kind: unknown
pdf: "https://openreview.net/pdf?id=FXV9cv3Csg"
tags: ["query:dr"]
score: 8.0
evidence: 从手术视频重建可形变组织的动态三维高斯模型
tldr: 手术视频的动态三维重建对医疗应用至关重要，但面临纹理有限、光照不一致与组织复杂形变的挑战。本文提出SurstSplat框架，将预训练二维基础模型的多模态特征融入三维高斯表示，并借助时空语义图匹配机制捕捉组织形变与器械交互。实验表明其相比标准高斯方法更能处理可形变组织，同时支持实时语义分割、语言引导编辑与医学视觉问答，为手术场景的动态可形变重建提供新思路。
source: ICLR-2026-Rejected-Public
selection_source: conference_retrieval
motivation: 手术视频存在纹理有限、光照不一致与组织复杂形变，动态三维重建困难。
method: 提出SurstSplat，将预训练二维基础模型的多模态特征融入三维高斯，并用时空语义图匹配捕捉组织形变与器械交互。
result: 相比标准高斯方法更好地处理可形变组织，并支持实时语义分割与语言引导编辑。
conclusion: 为手术场景的动态可形变三维重建与理解提供新框架。
---

## Abstract
Reconstructing dynamic 3D models from surgical videos is crucial for advanced medical applications, but faces challenges from limited textures, inconsistent lighting, and complex tissue deformations. We present \method, a framework that enhances dynamic Gaussian reconstruction through spatiotemporal semantic graph matching. By integrating multimodal features from pre-trained 2D foundation models into 3D Gaussian representations, our approach effectively captures tissue deformations and tool interactions. The spatiotemporal graph matching mechanism improves handling of deformable tissues over standard Gaussian methods while enabling real-time semantic segmentation, language-guided editing, and medical visual question answering. Experiments demonstrate that \method~enhances rendering quality in challenging surgical conditions and allows clinical 3D models to leverage pre-trained 2D multimodal foundation models. Our approach improves both rendering quality and computational efficiency, supporting advanced intraoperative applications and advancing robot-assisted surgery.

---

## 论文详细总结（自动生成）

### 1. 检索相关性
从手术视频重建可形变组织的动态三维高斯模型。

### 2. 核心内容
手术视频的动态三维重建对医疗应用至关重要，但面临纹理有限、光照不一致与组织复杂形变的挑战。本文提出SurstSplat框架，将预训练二维基础模型的多模态特征融入三维高斯表示，并借助时空语义图匹配机制捕捉组织形变与器械交互。实验表明其相比标准高斯方法更能处理可形变组织，同时支持实时语义分割、语言引导编辑与医学视觉问答，为手术场景的动态可形变重建提供新思路。

### 3. 对应检索需求
methods for non rigid and deformable 3D reconstruction of moving objects。

### 4. 来源与原文
- Source：ICLR-2026-Rejected-Public
- OpenReview：[https://openreview.net/forum?id=FXV9cv3Csg](https://openreview.net/forum?id=FXV9cv3Csg)
