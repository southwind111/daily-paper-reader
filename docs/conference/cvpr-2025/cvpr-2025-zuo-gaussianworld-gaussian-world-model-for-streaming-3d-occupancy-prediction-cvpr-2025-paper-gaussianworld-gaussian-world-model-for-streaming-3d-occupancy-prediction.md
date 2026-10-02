---
title: "GaussianWorld: Gaussian World Model for Streaming 3D Occupancy Prediction"
authors: "Zuo, Sicheng, Zheng, Wenzhao, Huang, Yuanhui, Zhou, Jie, Lu, Jiwen"
date: 2025
pdf: "https://openaccess.thecvf.com/content/CVPR2025/papers/Zuo_GaussianWorld_Gaussian_World_Model_for_Streaming_3D_Occupancy_Prediction_CVPR_2025_paper.pdf"
tags: ["query:d-world"]
score: 9
source: CVPR-2025-Accepted
selection_source: long-range
publication_date: 2025
publication_date_precision: year
publication_date_source: conference year only; exact release date unverified
publication_date_kind: unknown
id: cvpr-2025-zuo-gaussianworld-gaussian-world-model-for-streaming-3d-occupancy-prediction-cvpr-2025-paper
canonical_id: "work:4d7c5a04c9af0b691709f6ba"
research_run_id: 20261002-13e431aef9a9
research_mode: starter
reading_status: pending
---

## Abstract
3D occupancy prediction is important for autonomous driving due to its comprehensive perception of the surroundings. To incorporate sequential inputs, most existing methods fuse representations from previous frames to infer the current 3D occupancy. However, they fail to consider the continuity of driving scenarios and ignore the strong prior provided by the evolution of 3D scenes (e.g., only dynamic objects move). In this paper, we propose a world-modelbased framework to exploit the scene evolution for perception. We reformulate 3D occupancy prediction as a 4D occupancy forecasting problem conditioned on the current sensor input. We decompose the scene evolution into three factors: 1) ego motion alignment of static scenes; 2) local movements of dynamic objects; and 3) completion of newly-observed scenes. We then employ a Gaussian world model (GaussianWorld) to explicitly exploit these priors and infer the scene evolution in the 3D Gaussian space considering the current RGB observation. We evaluate the effectiveness of our framework on the widely used nuScenes dataset. Our GaussianWorld improves the performance of the single-frame counterpart by over 2% in mIoU without introducing additional computations.

## 专题评审

专题相关性评分：9/10。

该文明确提出基于世界模型的框架进行3D占用预测与场景演化建模，直接契合世界模型与3D视觉主题。

<!-- research-reading-pending -->
中文总结与全文内容待生成；当前仅提供原始论文元数据与摘要。
<!-- /research-reading-pending -->
