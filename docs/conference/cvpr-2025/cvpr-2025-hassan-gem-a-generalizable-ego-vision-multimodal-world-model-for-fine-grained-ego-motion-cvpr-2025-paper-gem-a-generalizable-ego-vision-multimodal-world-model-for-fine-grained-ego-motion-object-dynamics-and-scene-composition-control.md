---
title: "GEM: A Generalizable Ego-Vision Multimodal World Model for Fine-Grained Ego-Motion, Object Dynamics, and Scene Composition Control"
authors: "Hassan, Mariam, Stapf, Sebastian, Rahimi, Ahmad, Rezende, Pedro M B, Haghighi, Yasaman, Brüggemann, David, Katircioglu, Isinsu, Zhang, Lin, Chen, Xiaoran, Saha, Suman, Cannici, Marco, Aljalbout, Elie, Ye, Botao, Wang, Xi, Davtyan, Aram, Salzmann, Mathieu, Scaramuzza, Davide, Pollefeys, Marc, Favaro, Paolo, Alahi, Alexandre"
date: 2025
pdf: "https://openaccess.thecvf.com/content/CVPR2025/papers/Hassan_GEM_A_Generalizable_Ego-Vision_Multimodal_World_Model_for_Fine-Grained_Ego-Motion_CVPR_2025_paper.pdf"
tags: ["query:d-world"]
score: 9
source: CVPR-2025-Accepted
selection_source: long-range
publication_date: 2025
publication_date_precision: year
publication_date_source: conference year only; exact release date unverified
publication_date_kind: unknown
id: cvpr-2025-hassan-gem-a-generalizable-ego-vision-multimodal-world-model-for-fine-grained-ego-motion-cvpr-2025-paper
canonical_id: "work:5b4ee352c9f9a8469b74a882"
research_run_id: 20261002-13e431aef9a9
research_mode: starter
---

## Abstract
We present GEM, a Generalizable Ego-vision Multimodal world model that predicts future frames using a reference frame, sparse features, human poses, and ego-trajectories. Hence, our model has precise control over object dynamics, ego-agent motion and human poses. GEM generates paired RGB and depth outputs for richer spatial understanding. We introduce autoregressive noise schedules to enable stable long-horizon generations. Our dataset is comprised of 4000+ hours of multimodal data across domains like autonomous driving, egocentric human activities, and drone flights. Pseudo-labels are used to get depth maps, ego-trajectories, and human poses. We use a comprehensive evaluation framework, including a new Control of Object Manipulation (COM) metric, to assess controllability. Experiments show GEM excels at generating diverse, controllable scenarios and temporal consistency over long generations. Code, models, and datasets are fully open-sourced.

## 专题评审

专题相关性评分：9/10。

论文直接研究多模态世界模型与未来帧预测，属于世界模型主题。
