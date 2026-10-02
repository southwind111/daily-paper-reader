---
title: "Stereo4D: Learning How Things Move in 3D from Internet Stereo Videos"
title_zh: Stereo4D：从互联网立体视频学习物体在3D中如何运动
authors: "Jin, Linyi, Tucker, Richard, Li, Zhengqi, Fouhey, David, Snavely, Noah, Holynski, Aleksander"
date: 2025
publication_date: 2025
publication_date_precision: year
publication_date_source: conference year only; exact release date unverified
publication_date_kind: unknown
pdf: "https://openaccess.thecvf.com/content/CVPR2025/papers/Jin_Stereo4D_Learning_How_Things_Move_in_3D_from_Internet_Stereo_CVPR_2025_paper.pdf"
tags: ["query:dr"]
score: 9.0
evidence: 从互联网立体视频学习3D运动以进行4D重建
tldr: 从图像理解动态3D场景对机器人与场景重建至关重要，但恢复3D运动缺乏真值标注，难以进行大规模监督训练。本文提出一套系统，从互联网立体广角视频中融合并过滤相机位姿估计、立体深度估计与时间跟踪结果，挖掘高质量4D重建。由此生成大规模世界一致的伪度量3D点云数据，为动态3D运动学习提供监督信号。
source: CVPR-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-jin-stereo4d-learning-how-things-move-in-3d-from-internet-stereo-cvpr-2025-paper/fig-001.webp\", \"caption\": \"\", \"page\": 1, \"index\": 1, \"width\": 2880, \"height\": 2748}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-jin-stereo4d-learning-how-things-move-in-3d-from-internet-stereo-cvpr-2025-paper/fig-002.webp\", \"caption\": \"\", \"page\": 1, \"index\": 2, \"width\": 1974, \"height\": 1656}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-jin-stereo4d-learning-how-things-move-in-3d-from-internet-stereo-cvpr-2025-paper/fig-003.webp\", \"caption\": \"\", \"page\": 1, \"index\": 3, \"width\": 1920, \"height\": 1080}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-jin-stereo4d-learning-how-things-move-in-3d-from-internet-stereo-cvpr-2025-paper/fig-004.webp\", \"caption\": \"\", \"page\": 3, \"index\": 4, \"width\": 1920, \"height\": 1080}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-jin-stereo4d-learning-how-things-move-in-3d-from-internet-stereo-cvpr-2025-paper/fig-005.webp\", \"caption\": \"\", \"page\": 3, \"index\": 5, \"width\": 308, \"height\": 750}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-jin-stereo4d-learning-how-things-move-in-3d-from-internet-stereo-cvpr-2025-paper/fig-006.webp\", \"caption\": \"\", \"page\": 3, \"index\": 6, \"width\": 1024, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-jin-stereo4d-learning-how-things-move-in-3d-from-internet-stereo-cvpr-2025-paper/fig-007.webp\", \"caption\": \"\", \"page\": 3, \"index\": 7, \"width\": 1584, \"height\": 1176}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-jin-stereo4d-learning-how-things-move-in-3d-from-internet-stereo-cvpr-2025-paper/fig-008.webp\", \"caption\": \"\", \"page\": 3, \"index\": 8, \"width\": 512, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-jin-stereo4d-learning-how-things-move-in-3d-from-internet-stereo-cvpr-2025-paper/fig-009.webp\", \"caption\": \"\", \"page\": 3, \"index\": 9, \"width\": 480, \"height\": 480}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-jin-stereo4d-learning-how-things-move-in-3d-from-internet-stereo-cvpr-2025-paper/fig-010.webp\", \"caption\": \"\", \"page\": 3, \"index\": 10, \"width\": 942, \"height\": 802}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-jin-stereo4d-learning-how-things-move-in-3d-from-internet-stereo-cvpr-2025-paper/fig-011.webp\", \"caption\": \"\", \"page\": 4, \"index\": 11, \"width\": 1646, \"height\": 1638}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-jin-stereo4d-learning-how-things-move-in-3d-from-internet-stereo-cvpr-2025-paper/fig-012.webp\", \"caption\": \"\", \"page\": 4, \"index\": 12, \"width\": 1852, \"height\": 1898}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-jin-stereo4d-learning-how-things-move-in-3d-from-internet-stereo-cvpr-2025-paper/fig-013.webp\", \"caption\": \"\", \"page\": 4, \"index\": 13, \"width\": 600, \"height\": 832}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-jin-stereo4d-learning-how-things-move-in-3d-from-internet-stereo-cvpr-2025-paper/fig-014.webp\", \"caption\": \"\", \"page\": 4, \"index\": 14, \"width\": 2598, \"height\": 2302}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-jin-stereo4d-learning-how-things-move-in-3d-from-internet-stereo-cvpr-2025-paper/fig-015.webp\", \"caption\": \"\", \"page\": 4, \"index\": 15, \"width\": 638, \"height\": 758}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-jin-stereo4d-learning-how-things-move-in-3d-from-internet-stereo-cvpr-2025-paper/fig-016.webp\", \"caption\": \"\", \"page\": 5, \"index\": 16, \"width\": 1840, \"height\": 886}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-jin-stereo4d-learning-how-things-move-in-3d-from-internet-stereo-cvpr-2025-paper/fig-017.webp\", \"caption\": \"\", \"page\": 5, \"index\": 17, \"width\": 1024, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-jin-stereo4d-learning-how-things-move-in-3d-from-internet-stereo-cvpr-2025-paper/fig-018.webp\", \"caption\": \"\", \"page\": 5, \"index\": 18, \"width\": 1024, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-jin-stereo4d-learning-how-things-move-in-3d-from-internet-stereo-cvpr-2025-paper/fig-019.webp\", \"caption\": \"\", \"page\": 5, \"index\": 19, \"width\": 1024, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-jin-stereo4d-learning-how-things-move-in-3d-from-internet-stereo-cvpr-2025-paper/fig-020.webp\", \"caption\": \"\", \"page\": 5, \"index\": 20, \"width\": 1024, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-jin-stereo4d-learning-how-things-move-in-3d-from-internet-stereo-cvpr-2025-paper/fig-021.webp\", \"caption\": \"\", \"page\": 5, \"index\": 21, \"width\": 1024, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-jin-stereo4d-learning-how-things-move-in-3d-from-internet-stereo-cvpr-2025-paper/fig-022.webp\", \"caption\": \"\", \"page\": 5, \"index\": 22, \"width\": 1024, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-jin-stereo4d-learning-how-things-move-in-3d-from-internet-stereo-cvpr-2025-paper/fig-023.webp\", \"caption\": \"\", \"page\": 5, \"index\": 23, \"width\": 1024, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-jin-stereo4d-learning-how-things-move-in-3d-from-internet-stereo-cvpr-2025-paper/fig-024.webp\", \"caption\": \"\", \"page\": 5, \"index\": 24, \"width\": 1024, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-jin-stereo4d-learning-how-things-move-in-3d-from-internet-stereo-cvpr-2025-paper/fig-025.webp\", \"caption\": \"\", \"page\": 6, \"index\": 25, \"width\": 512, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-jin-stereo4d-learning-how-things-move-in-3d-from-internet-stereo-cvpr-2025-paper/fig-026.webp\", \"caption\": \"\", \"page\": 6, \"index\": 26, \"width\": 512, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-jin-stereo4d-learning-how-things-move-in-3d-from-internet-stereo-cvpr-2025-paper/fig-027.webp\", \"caption\": \"\", \"page\": 6, \"index\": 27, \"width\": 1080, \"height\": 1080}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-jin-stereo4d-learning-how-things-move-in-3d-from-internet-stereo-cvpr-2025-paper/fig-028.webp\", \"caption\": \"\", \"page\": 6, \"index\": 28, \"width\": 1080, \"height\": 1080}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-jin-stereo4d-learning-how-things-move-in-3d-from-internet-stereo-cvpr-2025-paper/fig-029.webp\", \"caption\": \"\", \"page\": 7, \"index\": 29, \"width\": 1920, \"height\": 1080}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-jin-stereo4d-learning-how-things-move-in-3d-from-internet-stereo-cvpr-2025-paper/fig-030.webp\", \"caption\": \"\", \"page\": 7, \"index\": 30, \"width\": 512, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-jin-stereo4d-learning-how-things-move-in-3d-from-internet-stereo-cvpr-2025-paper/fig-031.webp\", \"caption\": \"\", \"page\": 7, \"index\": 31, \"width\": 1920, \"height\": 1080}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-jin-stereo4d-learning-how-things-move-in-3d-from-internet-stereo-cvpr-2025-paper/fig-032.webp\", \"caption\": \"\", \"page\": 7, \"index\": 32, \"width\": 1920, \"height\": 1080}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-jin-stereo4d-learning-how-things-move-in-3d-from-internet-stereo-cvpr-2025-paper/fig-033.webp\", \"caption\": \"\", \"page\": 7, \"index\": 33, \"width\": 1920, \"height\": 1080}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-jin-stereo4d-learning-how-things-move-in-3d-from-internet-stereo-cvpr-2025-paper/fig-034.webp\", \"caption\": \"\", \"page\": 7, \"index\": 34, \"width\": 512, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-jin-stereo4d-learning-how-things-move-in-3d-from-internet-stereo-cvpr-2025-paper/fig-035.webp\", \"caption\": \"\", \"page\": 7, \"index\": 35, \"width\": 512, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-jin-stereo4d-learning-how-things-move-in-3d-from-internet-stereo-cvpr-2025-paper/fig-036.webp\", \"caption\": \"\", \"page\": 7, \"index\": 36, \"width\": 512, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-jin-stereo4d-learning-how-things-move-in-3d-from-internet-stereo-cvpr-2025-paper/fig-037.webp\", \"caption\": \"\", \"page\": 7, \"index\": 37, \"width\": 512, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-jin-stereo4d-learning-how-things-move-in-3d-from-internet-stereo-cvpr-2025-paper/fig-038.webp\", \"caption\": \"\", \"page\": 7, \"index\": 38, \"width\": 1920, \"height\": 1080}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-jin-stereo4d-learning-how-things-move-in-3d-from-internet-stereo-cvpr-2025-paper/fig-039.webp\", \"caption\": \"\", \"page\": 7, \"index\": 39, \"width\": 1920, \"height\": 1080}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-jin-stereo4d-learning-how-things-move-in-3d-from-internet-stereo-cvpr-2025-paper/fig-040.webp\", \"caption\": \"\", \"page\": 7, \"index\": 40, \"width\": 512, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-jin-stereo4d-learning-how-things-move-in-3d-from-internet-stereo-cvpr-2025-paper/fig-041.webp\", \"caption\": \"\", \"page\": 7, \"index\": 41, \"width\": 512, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-jin-stereo4d-learning-how-things-move-in-3d-from-internet-stereo-cvpr-2025-paper/fig-042.webp\", \"caption\": \"\", \"page\": 7, \"index\": 42, \"width\": 512, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-jin-stereo4d-learning-how-things-move-in-3d-from-internet-stereo-cvpr-2025-paper/fig-043.webp\", \"caption\": \"\", \"page\": 7, \"index\": 43, \"width\": 512, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-jin-stereo4d-learning-how-things-move-in-3d-from-internet-stereo-cvpr-2025-paper/fig-044.webp\", \"caption\": \"\", \"page\": 7, \"index\": 44, \"width\": 512, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-jin-stereo4d-learning-how-things-move-in-3d-from-internet-stereo-cvpr-2025-paper/fig-045.webp\", \"caption\": \"\", \"page\": 7, \"index\": 45, \"width\": 512, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-jin-stereo4d-learning-how-things-move-in-3d-from-internet-stereo-cvpr-2025-paper/fig-046.webp\", \"caption\": \"\", \"page\": 7, \"index\": 46, \"width\": 512, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-jin-stereo4d-learning-how-things-move-in-3d-from-internet-stereo-cvpr-2025-paper/fig-047.webp\", \"caption\": \"\", \"page\": 7, \"index\": 47, \"width\": 512, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-jin-stereo4d-learning-how-things-move-in-3d-from-internet-stereo-cvpr-2025-paper/fig-048.webp\", \"caption\": \"\", \"page\": 7, \"index\": 48, \"width\": 512, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-jin-stereo4d-learning-how-things-move-in-3d-from-internet-stereo-cvpr-2025-paper/fig-049.webp\", \"caption\": \"\", \"page\": 7, \"index\": 49, \"width\": 512, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-jin-stereo4d-learning-how-things-move-in-3d-from-internet-stereo-cvpr-2025-paper/fig-050.webp\", \"caption\": \"\", \"page\": 7, \"index\": 50, \"width\": 512, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-jin-stereo4d-learning-how-things-move-in-3d-from-internet-stereo-cvpr-2025-paper/fig-051.webp\", \"caption\": \"\", \"page\": 7, \"index\": 51, \"width\": 512, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-jin-stereo4d-learning-how-things-move-in-3d-from-internet-stereo-cvpr-2025-paper/fig-052.webp\", \"caption\": \"\", \"page\": 7, \"index\": 52, \"width\": 512, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-jin-stereo4d-learning-how-things-move-in-3d-from-internet-stereo-cvpr-2025-paper/fig-053.webp\", \"caption\": \"\", \"page\": 7, \"index\": 53, \"width\": 512, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-jin-stereo4d-learning-how-things-move-in-3d-from-internet-stereo-cvpr-2025-paper/fig-054.webp\", \"caption\": \"\", \"page\": 7, \"index\": 54, \"width\": 512, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-jin-stereo4d-learning-how-things-move-in-3d-from-internet-stereo-cvpr-2025-paper/fig-055.webp\", \"caption\": \"\", \"page\": 7, \"index\": 55, \"width\": 512, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-jin-stereo4d-learning-how-things-move-in-3d-from-internet-stereo-cvpr-2025-paper/fig-056.webp\", \"caption\": \"\", \"page\": 8, \"index\": 56, \"width\": 467, \"height\": 263}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-jin-stereo4d-learning-how-things-move-in-3d-from-internet-stereo-cvpr-2025-paper/fig-057.webp\", \"caption\": \"\", \"page\": 8, \"index\": 57, \"width\": 467, \"height\": 263}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-jin-stereo4d-learning-how-things-move-in-3d-from-internet-stereo-cvpr-2025-paper/fig-058.webp\", \"caption\": \"\", \"page\": 8, \"index\": 58, \"width\": 758, \"height\": 426}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-jin-stereo4d-learning-how-things-move-in-3d-from-internet-stereo-cvpr-2025-paper/fig-059.webp\", \"caption\": \"\", \"page\": 8, \"index\": 59, \"width\": 467, \"height\": 263}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-jin-stereo4d-learning-how-things-move-in-3d-from-internet-stereo-cvpr-2025-paper/fig-060.webp\", \"caption\": \"\", \"page\": 8, \"index\": 60, \"width\": 758, \"height\": 426}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-jin-stereo4d-learning-how-things-move-in-3d-from-internet-stereo-cvpr-2025-paper/fig-061.webp\", \"caption\": \"\", \"page\": 8, \"index\": 61, \"width\": 758, \"height\": 426}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-jin-stereo4d-learning-how-things-move-in-3d-from-internet-stereo-cvpr-2025-paper/fig-062.webp\", \"caption\": \"\", \"page\": 8, \"index\": 62, \"width\": 758, \"height\": 426}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-jin-stereo4d-learning-how-things-move-in-3d-from-internet-stereo-cvpr-2025-paper/fig-063.webp\", \"caption\": \"\", \"page\": 8, \"index\": 63, \"width\": 762, \"height\": 426}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-jin-stereo4d-learning-how-things-move-in-3d-from-internet-stereo-cvpr-2025-paper/fig-064.webp\", \"caption\": \"\", \"page\": 8, \"index\": 64, \"width\": 467, \"height\": 263}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-jin-stereo4d-learning-how-things-move-in-3d-from-internet-stereo-cvpr-2025-paper/fig-065.webp\", \"caption\": \"\", \"page\": 8, \"index\": 65, \"width\": 743, \"height\": 418}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-jin-stereo4d-learning-how-things-move-in-3d-from-internet-stereo-cvpr-2025-paper/fig-066.webp\", \"caption\": \"\", \"page\": 8, \"index\": 66, \"width\": 467, \"height\": 263}]"
motivation: 恢复3D运动缺乏真值标注，难以进行大规模监督训练。
method: 融合相机位姿估计、立体深度估计与时间跟踪，从互联网立体视频挖掘高质量4D重建。
result: 生成大规模世界一致的伪度量3D点云与运动数据。
conclusion: 为动态3D场景理解提供大规模训练数据。
---

## Abstract
Learning to understand dynamic 3D scenes from imagery is crucial for applications ranging from robotics to scene reconstruction. Yet, unlike other problems where large-scale supervised training has enabled rapid progress, directly supervising methods for recovering 3D motion remains challenging due to the fundamental difficulty of obtaining ground truth annotations. We present a system for mining high-quality 4D reconstructions from internet stereoscopic, wide-angle videos. Our system fuses and filters the outputs of camera pose estimation, stereo depth estimation, and temporal tracking methods into high-quality dynamic 3D reconstructions. We use this method to generate large-scale data in the form of world-consistent, pseudo-metric 3D point clouds with long-term motion trajectories. We demonstrate the utility of this data by training a variant of DUSt3r to predict structure and 3D motion from real-world image pairs, showing that training on our reconstructed data enables generalization to diverse real-world scenes. Project page and data at https://stereo4d.github.io

---

## 论文详细总结（自动生成）

# Stereo4D：从互联网立体视频学习物体在3D中如何运动

## 1. 核心问题与研究动机

- **核心问题**：从图像中理解动态3D场景（即同时恢复几何与运动）是计算机视觉的基础问题，但直接监督3D运动恢复方法极其困难，根本原因在于**难以获取真实世界的3D运动真值标注**。
- **背景对比**：在静态3D重建、图像生成、大语言模型等领域，大规模高质量训练数据 + 可扩展架构已带来显著突破；然而动态3D场景的学习缺乏对应的“真实世界+3D运动轨迹”大规模数据集。
- **现有数据源的局限**：
  - **合成数据集**（如PointOdyssey、Kubric等）：与真实世界内容分布和运动模式存在域差距。
  - **传统动捕/多相机阵列**：精度高但难以规模化，场景多样性受限。
  - **自动驾驶数据集**（KITTI、Waymo）：场景局限于街道。
  - **小规模标注数据集**（TAPVid、Dycheck等）：主要用于评测而非训练。
- **本文洞察**：互联网上的**立体鱼眼视频（VR180）** 是尚未被利用的宝贵数据源——具有宽视场、标准化立体基线，适合挖掘真实世界的动态3D信息。
- **整体含义**：提出一套从互联网立体视频自动挖掘高质量4D重建的系统，并生成超过10万段视频片段的大规模数据集，为动态3D理解提供监督信号。

## 2. 方法论

### 2.1 核心思想

从VR180（宽角、立体）视频出发，融合**相机位姿估计、立体深度估计、2D时间跟踪**三类方法的输出，经反投影、优化与过滤，生成世界一致的**伪度量3D点云**及其**长期运动轨迹**。数据管线产出：每帧相机外参、立体标定、每帧视差图、3D点轨迹。

### 2.2 数据管线关键步骤

- **SfM（相机位姿估计）**：
  - 先用SLAM方法将视频切分为可跟踪的镜头（shots）。
  - 对每个镜头运行类似COLMAP的增量式SfM。
  - 立体标定初始化为基线6.3cm的校正立体对，但在BA中优化——实际发现立体对方向常显著偏离标称配置，优化标定对结果至关重要。
- **深度估计**：
  - 利用估计的立体标定生成校正立体对，用**RAFT**逐帧估计视差图。
  - 置信度检查：丢弃y方向光流>1像素（校正立体对应水平运动）和立体循环一致性误差>1像素的像素。
- **3D轨迹估计与优化**：
  - 用**BootsTAP**提取长程2D点轨迹（每10帧在512×512分辨率上均匀初始化128×128查询点，剪除重叠冗余轨迹）。
  - 结合相机位姿与视差图将2D轨迹反投影为3D运动轨迹。
  - 由于逐帧视差存在高频抖动，引入**逐帧沿相机射线的标量偏移δ_i**进行优化，目标函数由三项构成：
    - **静态损失 L_static**：鼓励点在世界空间中彼此靠近，抑制抖动。
    - **动态损失 L_dynamic**：用离散拉普拉斯算子沿相机射线最小化加速度，窗口W={1,3,5}。
    - **正则化损失 L_reg**：在视差空间中约束偏移量，反映测量本身来自视差；远处点容差更大（深度不确定性更高）。
  - 两项损失按运动幅度m加权：σ(m)=1/(1+exp(m−m₀))，m₀=20；m为轨迹在2D图像空间中拖尾长度的90百分位（用2D而非3D衡量，因远点3D噪声被放大）。
  - 用Adam优化100步，学习率0.05，λ_reg=10⁻⁴。
- **过滤策略**：
  - 语义过滤：丢弃落在“墙、建筑、道路、地面、人行道”等无纹理类别上的运动轨迹（DeepLabv3 + ADE20K）。
  - 视频过滤：剔除纯静态图像、交叉淡入淡出、含文字/标题的片段（通过多时间尺度SIFT匹配检测）。
  - 裁剪视频首尾避免标题序列。

### 2.3 DynaDUSt3R模型

- **基础架构**：基于DUSt3R（ViT编码器 + 交叉注意力Transformer解码器 + 点图头），预测两帧点云并对其到第一帧坐标系。
- **新增运动头**：与点图头并行，预测3D位移向量图（场景流），将每个输入帧的点位移到**中间查询时间 t_q ∈ [0,1]**。
- **设计动机**：
  - 支持预测两帧之间的完整运动轨迹，而不仅是端点。
  - 允许利用部分真值轨迹监督（并非所有轨迹都跨越t₀到t₁）。
- **时间嵌入**：用位置编码将t_q编码为128维向量，通过线性投影注入运动头。
- **训练目标**：
  - 沿用DUSt3R的置信度感知、尺度不变的3D回归损失（L_point）。
  - 增加运动后的位置欧氏距离损失（L_motion），鼓励学习正确位移。
  - 置信度损失权重α_m = α_p = 0.2。
- **训练细节**：以DUSt3R权重初始化，运动头用点图头权重初始化；微调49k迭代，batch size 64，学习率2.5e-5，Adam，权重衰减0.95；随机采样间隔≤60帧的帧对；同时使用60°和120° FoV视频。

## 3. 实验设计

### 3.1 数据集与Benchmark

- **训练数据**：
  - **Stereo4D**（本文构建）：>10万段视频片段，来自互联网VR180视频。
  - **PointOdyssey**（合成数据集）：含渲染的深度图与3D运动轨迹。
- **评测数据**：
  - **Stereo4D held-out测试集**。
  - **Aria Digital Twin (ADT)**：经TAPVid3D benchmark处理的含场景运动数据。
  - **Bonn**：用于深度/结构评测。
- **采样设置**：测试时随机采样间隔≤30帧的帧对（训练≤60帧）。

### 3.2 对比方法

- **3D运动预测**：DynaDUSt3R (PointOdyssey) vs. DynaDUSt3R (Stereo4D)。
- **3D结构预测**：DUSt3R、MonST3R、DynaDUSt3R (PointOdyssey)、DynaDUSt3R (Stereo4D)。

### 3.3 评价指标

- **3D运动**：3D端点误差（EPE↓）、运动误差<5cm/10cm的点比例（δ^3D_0.05、δ^3D_0.10 ↑）。
- **结构/深度**：绝对相对误差（Abs Rel↓）、δ<1.25内点比例（↑）。
- 预测点云尺度未知，统一用中位数尺度对齐。

## 4. 资源与算力

- 论文**未明确说明**所使用的GPU型号、数量或总训练时长。
- 仅提供了训练超参数：微调49k迭代、batch size 64、学习率2.5e-5、Adam优化器、权重衰减0.95。
- 数据管线方面，提到处理超过10万段视频片段，但未给出具体计算资源开销。
- **结论**：算力信息不透明，无法评估训练成本与可复现性所需资源。

## 5. 实验数量与充分性

- **主要实验组数**（正文）：
  1. 3D运动预测：在Stereo4D和ADT两个测试集上对比两种训练数据来源（合成vs真实）。
  2. 结构/深度预测：在Stereo4D和Bonn两个数据集上对比四种方法。
- **定性实验**：多个场景的可视化对比（图7-10），涵盖街景、人物运动等。
- **消融实验**：正文提及“补充材料中有关于轨迹优化和DynaDUSt3R设计的更多消融”，但正文未展开。
- **充分性评估**：
  - **优点**：跨域泛化测试（训练于Stereo4D，测试于ADT/Bonn）设计合理，能体现真实数据带来的泛化优势；合成vs真实的对比直接支撑核心论点。
  - **不足**：正文实验组数偏少，缺乏对数据管线各组件（如轨迹优化、过滤策略）的定量消融；未报告不同视频质量/场景类型下的分层结果；未与更多3D运动/场景流方法对比。

## 6. 主要结论与发现

- **真实数据优于合成数据**：DynaDUSt3R (Stereo4D) 在Stereo4D测试集上3D EPE从0.6191降至0.1110，δ^3D_0.05从11.61升至65.07；在ADT上EPE从0.3126降至0.1231，δ^3D_0.05从8.56升至51.98。
- **结构预测同样受益**：DynaDUSt3R (Stereo4D) 在Stereo4D测试集上Abs Rel=0.1032、δ<1.25=87.93，大幅优于DUSt3R（0.2696/67.77）和MonST3R（0.1939/72.56）；在Bonn上Abs Rel=0.0653、δ<1.25=96.02，同样领先。
- **定性发现**：PointOdyssey训练的模型会对静止物体（墙面、横幅）错误预测运动，而Stereo4D训练的模型能正确识别静止元素并更精确预测动态物体运动。
- **总体结论**：从互联网立体视频挖掘的真实世界4D数据能有效训练出泛化到多样真实场景的3D结构与运动预测模型。

## 7. 优点

- **数据范式创新**：首次系统性地将互联网VR180立体视频作为可扩展的4D真值挖掘来源，绕开了传统动捕和合成数据的瓶颈。
- **工程整合扎实**：将SfM、立体深度、2D跟踪等SOTA方法有机融合，并针对动态场景设计了专门的轨迹优化与过滤机制。
- **轨迹优化设计巧妙**：用逐帧沿射线偏移的轻量参数化 + 静态/动态/正则三项损失 + 运动幅度自适应加权，有效去除高频抖动，且正则化在视差空间处理远处不确定性。
- **模型设计合理**：DynaDUSt3R引入中间查询时间t_q，既支持完整轨迹预测，又允许利用部分真值监督，扩展性强。
- **跨域泛化验证**：在未见过的ADT和Bonn数据集上验证，证明真实数据带来的泛化优势，而非仅在自建测试集上过拟合。
- **数据规模可观**：>10万段视频片段，内容多样性好（通过词云展示）。

## 8. 不足与局限

- **数据质量依赖上游方法**：长程3D轨迹质量取决于光流和2D跟踪精度，远处背景区域和长时间遮挡的物体容易退化。
- **非生成式、仅两帧输入**：DynaDUSt3R是确定性模型，只处理两帧图像，无法处理长视频输入或对模糊运动内容进行生成式补全。
- **算力信息缺失**：未报告GPU型号、数量和训练时长，影响可复现性和成本评估。
- **消融实验不足**：正文缺乏对数据管线关键组件（轨迹优化、过滤策略、FoV选择等）的定量消融，难以判断各模块贡献。
- **评测范围有限**：仅对比了DUSt3R和MonST3R等少数方法，未与更多场景流/动态重建方法（如RAFT-3D等）比较。
- **潜在偏差风险**：数据来自互联网VR180视频，内容分布可能偏向特定拍摄风格和场景（旅游、活动记录等），对专业领域（医疗、工业）的覆盖未知。
- **伪度量而非真度量**：数据是“pseudo-metric”，依赖立体基线和标定优化，绝对尺度精度有限。
- **应用限制**：作为训练数据挖掘工具而非端到端产品，实际部署需要处理大规模视频下载、存储和计算成本。

（完）
