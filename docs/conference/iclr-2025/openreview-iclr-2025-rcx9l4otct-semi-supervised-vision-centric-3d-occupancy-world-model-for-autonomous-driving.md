---
title: Semi-Supervised Vision-Centric 3D Occupancy World Model for Autonomous Driving
authors: "Xiang Li, Pengfei Li, Yupeng Zheng, Wei Sun, Yan Wang, yilun chen"
date: 2025
pdf: "https://proceedings.iclr.cc/paper_files/paper/2025/file/9c979c7a7bcc6a791c3b492697f97e1e-Paper-Conference.pdf"
tags: ["query:d-world"]
score: 9
source: ICLR-2025-Accepted
selection_source: long-range
publication_date: 2025
publication_date_precision: year
publication_date_source: conference year only; exact release date unverified
publication_date_kind: unknown
id: openreview-iclr-2025-rcx9l4otct
canonical_id: "work:52b2234172cc135f8275082f"
research_run_id: 20261002-13e431aef9a9
research_mode: starter
reading_status: pending
---

## Abstract
Understanding world dynamics is crucial for planning in autonomous driving. Recent methods attempt to achieve this by learning a 3D occupancy world model that forecasts future surrounding scenes based on current observation. However, 3D occupancy labels are still required to produce promising results. Considering the high annotation cost for 3D outdoor scenes, we propose a semi-supervised vision-centric 3D occupancy world model, **PreWorld**, to leverage the potential of 2D labels through a novel two-stage training paradigm: the self-supervised pre-training stage and the fully-supervised fine-tuning stage. Specifically, during the pre-training stage, we utilize an attribute projection head to generate different attribute fields of a scene (e.g., RGB, density, semantic), thus enabling temporal supervision from 2D labels via volume rendering techniques. Furthermore, we introduce a simple yet effective state-conditioned forecasting module to recursively forecast future occupancy and ego trajectory in a direct manner. Extensive experiments on the nuScenes dataset validate the effectiveness and scalability of our method, and demonstrate that PreWorld achieves competitive performance across 3D occupancy prediction, 4D occupancy forecasting and motion planning tasks.

## 专题评审

专题相关性评分：9/10。

该文提出半监督视觉中心3D占用世界模型用于自动驾驶场景预测，直接契合世界模型与3D视觉主题。

<!-- research-reading-pending -->
中文总结与全文内容待生成；当前仅提供原始论文元数据与摘要。
<!-- /research-reading-pending -->
