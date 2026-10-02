---
title: "STream3R: Scalable Sequential 3D Reconstruction with Causal Transformer"
title_zh: STream3R：基于因果Transformer的可扩展序列化三维重建
authors: "Yushi LAN, Yihang Luo, Fangzhou Hong, Shangchen Zhou, Honghua Chen, Zhaoyang Lyu, Bo Dai, Shuai Yang, Chen Change Loy, Xingang Pan"
date: 2026
publication_date: 2026
publication_date_precision: year
publication_date_source: conference year only; exact release date unverified
publication_date_kind: unknown
pdf: "https://openreview.net/pdf?id=RTTYGeC2Io"
tags: ["query:dr"]
score: 8.0
evidence: 面向动态场景的流式序列三维重建
tldr: 现有三维重建方法依赖昂贵的全局优化或简单记忆机制，难以处理长序列，且在动态场景中容易失效。STream3R将点图预测重构为仅解码器Transformer问题，利用因果注意力实现高效的流式重建，并从大规模三维数据中学习几何先验。实验表明该方法在多样且具挑战性的场景（包括动态场景）中持续优于先前工作，为可扩展的序列化重建提供了新范式。
source: ICLR-2026-Accepted
selection_source: conference_retrieval
motivation: 多视图三维重建依赖昂贵全局优化或难以扩展的简单记忆机制，动态长序列场景表现不佳。
method: STream3R将点图预测重构为仅解码器Transformer，用因果注意力构建流式重建框架，并从大规模三维数据学习几何先验。
result: 实验显示其在包括动态场景在内的多样挑战场景中持续优于先前方法。
conclusion: 该方法为可扩展的序列化三维重建提供了高效新范式。
---

## Abstract
We present STream3R, a novel approach to 3D reconstruction that reformulates pointmap prediction as a decoder-only Transformer problem. Existing state-of-the-art methods for multi-view reconstruction either depend on expensive global optimization or rely on simplistic memory mechanisms that scale poorly with sequence length. In contrast, STream3R introduces a streaming framework that processes image sequences efficiently using causal attention, inspired by advances in modern language modeling. By learning geometric priors from large-scale 3D datasets, STream3R generalizes well to diverse and challenging scenarios, including dynamic scenes where traditional methods often fail. Extensive experiments show that our method consistently outperforms prior work across both static and dynamic scene benchmarks. Moreover, STream3R is inherently compatible with LLM-style training infrastructure, enabling efficient large-scale pretraining and fine-tuning for various downstream 3D tasks. Our results underscore the potential of causal Transformer models for online 3D perception, paving the way for real-time 3D understanding in streaming environments.

---

## 论文详细总结（自动生成）

### 1. 检索相关性
面向动态场景的流式序列三维重建。

### 2. 核心内容
现有三维重建方法依赖昂贵的全局优化或简单记忆机制，难以处理长序列，且在动态场景中容易失效。STream3R将点图预测重构为仅解码器Transformer问题，利用因果注意力实现高效的流式重建，并从大规模三维数据中学习几何先验。实验表明该方法在多样且具挑战性的场景（包括动态场景）中持续优于先前工作，为可扩展的序列化重建提供了新范式。

### 3. 对应检索需求
papers on dynamic 3D reconstruction that recover time varying geometry from video or sensor sequences。

### 4. 来源与原文
- Source：ICLR-2026-Accepted
- OpenReview：[https://openreview.net/forum?id=RTTYGeC2Io](https://openreview.net/forum?id=RTTYGeC2Io)
