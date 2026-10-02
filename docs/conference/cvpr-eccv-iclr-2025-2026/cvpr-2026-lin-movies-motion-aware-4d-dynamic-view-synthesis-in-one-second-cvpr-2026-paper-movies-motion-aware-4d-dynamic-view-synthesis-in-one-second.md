---
title: "MoVieS: Motion-Aware 4D Dynamic View Synthesis in One Second"
title_zh: MoVieS：一秒内完成运动感知的四维动态视图合成
authors: "Lin, Chenguo, Lin, Yuchen, Pan, Panwang, Yu, Yifan, Hu, Tao, Yan, Honglei, Fragkiadaki, Katerina, Mu, Yadong"
date: 2026
publication_date: 2026
publication_date_precision: year
publication_date_source: conference year only; exact release date unverified
publication_date_kind: unknown
pdf: "https://openaccess.thecvf.com/content/CVPR2026/papers/Lin_MoVieS_Motion-Aware_4D_Dynamic_View_Synthesis_in_One_Second_CVPR_2026_paper.pdf"
tags: ["query:dr"]
score: 9.0
evidence: 用运动感知高斯从单目视频重建四维动态场景
tldr: 从单目视频重建四维动态场景通常需要分任务建模，难以统一外观、几何与运动。本文提出MoVieS运动感知视图合成模型，用像素对齐的高斯基元表示动态三维场景，并显式监督其随时间变化的运动。该方法在约一秒内完成重建，首次在单一学习框架内统一重建、视图合成与三维点跟踪，并支持场景流估计与运动物体分割等零样本应用。
source: CVPR-2026-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-lin-movies-motion-aware-4d-dynamic-view-synthesis-in-one-second-cvpr-2026-paper/fig-001.webp\", \"caption\": \"\", \"page\": 2, \"index\": 1, \"width\": 528, \"height\": 304}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-lin-movies-motion-aware-4d-dynamic-view-synthesis-in-one-second-cvpr-2026-paper/fig-002.webp\", \"caption\": \"\", \"page\": 2, \"index\": 2, \"width\": 528, \"height\": 304}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-lin-movies-motion-aware-4d-dynamic-view-synthesis-in-one-second-cvpr-2026-paper/fig-003.webp\", \"caption\": \"\", \"page\": 2, \"index\": 3, \"width\": 528, \"height\": 304}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-lin-movies-motion-aware-4d-dynamic-view-synthesis-in-one-second-cvpr-2026-paper/fig-004.webp\", \"caption\": \"\", \"page\": 2, \"index\": 4, \"width\": 528, \"height\": 304}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-lin-movies-motion-aware-4d-dynamic-view-synthesis-in-one-second-cvpr-2026-paper/fig-005.webp\", \"caption\": \"\", \"page\": 2, \"index\": 5, \"width\": 528, \"height\": 304}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-lin-movies-motion-aware-4d-dynamic-view-synthesis-in-one-second-cvpr-2026-paper/fig-006.webp\", \"caption\": \"\", \"page\": 2, \"index\": 6, \"width\": 528, \"height\": 304}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-lin-movies-motion-aware-4d-dynamic-view-synthesis-in-one-second-cvpr-2026-paper/fig-007.webp\", \"caption\": \"\", \"page\": 2, \"index\": 7, \"width\": 528, \"height\": 304}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-lin-movies-motion-aware-4d-dynamic-view-synthesis-in-one-second-cvpr-2026-paper/fig-008.webp\", \"caption\": \"\", \"page\": 2, \"index\": 8, \"width\": 528, \"height\": 304}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-lin-movies-motion-aware-4d-dynamic-view-synthesis-in-one-second-cvpr-2026-paper/fig-009.webp\", \"caption\": \"\", \"page\": 2, \"index\": 9, \"width\": 528, \"height\": 304}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-lin-movies-motion-aware-4d-dynamic-view-synthesis-in-one-second-cvpr-2026-paper/fig-010.webp\", \"caption\": \"\", \"page\": 2, \"index\": 10, \"width\": 528, \"height\": 304}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-lin-movies-motion-aware-4d-dynamic-view-synthesis-in-one-second-cvpr-2026-paper/fig-011.webp\", \"caption\": \"\", \"page\": 2, \"index\": 11, \"width\": 1960, \"height\": 686}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-lin-movies-motion-aware-4d-dynamic-view-synthesis-in-one-second-cvpr-2026-paper/fig-012.webp\", \"caption\": \"\", \"page\": 2, \"index\": 12, \"width\": 528, \"height\": 304}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-lin-movies-motion-aware-4d-dynamic-view-synthesis-in-one-second-cvpr-2026-paper/fig-013.webp\", \"caption\": \"\", \"page\": 2, \"index\": 13, \"width\": 528, \"height\": 304}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-lin-movies-motion-aware-4d-dynamic-view-synthesis-in-one-second-cvpr-2026-paper/fig-014.webp\", \"caption\": \"\", \"page\": 2, \"index\": 14, \"width\": 528, \"height\": 304}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-lin-movies-motion-aware-4d-dynamic-view-synthesis-in-one-second-cvpr-2026-paper/fig-015.webp\", \"caption\": \"\", \"page\": 2, \"index\": 15, \"width\": 528, \"height\": 304}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-lin-movies-motion-aware-4d-dynamic-view-synthesis-in-one-second-cvpr-2026-paper/fig-016.webp\", \"caption\": \"\", \"page\": 2, \"index\": 16, \"width\": 528, \"height\": 304}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-lin-movies-motion-aware-4d-dynamic-view-synthesis-in-one-second-cvpr-2026-paper/fig-017.webp\", \"caption\": \"\", \"page\": 2, \"index\": 17, \"width\": 528, \"height\": 304}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-lin-movies-motion-aware-4d-dynamic-view-synthesis-in-one-second-cvpr-2026-paper/fig-018.webp\", \"caption\": \"\", \"page\": 2, \"index\": 18, \"width\": 528, \"height\": 304}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-lin-movies-motion-aware-4d-dynamic-view-synthesis-in-one-second-cvpr-2026-paper/fig-019.webp\", \"caption\": \"\", \"page\": 5, \"index\": 19, \"width\": 374, \"height\": 377}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-lin-movies-motion-aware-4d-dynamic-view-synthesis-in-one-second-cvpr-2026-paper/fig-020.webp\", \"caption\": \"\", \"page\": 5, \"index\": 20, \"width\": 377, \"height\": 377}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-lin-movies-motion-aware-4d-dynamic-view-synthesis-in-one-second-cvpr-2026-paper/fig-021.webp\", \"caption\": \"\", \"page\": 5, \"index\": 21, \"width\": 377, \"height\": 377}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-lin-movies-motion-aware-4d-dynamic-view-synthesis-in-one-second-cvpr-2026-paper/fig-022.webp\", \"caption\": \"\", \"page\": 5, \"index\": 22, \"width\": 375, \"height\": 377}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-lin-movies-motion-aware-4d-dynamic-view-synthesis-in-one-second-cvpr-2026-paper/fig-023.webp\", \"caption\": \"\", \"page\": 5, \"index\": 23, \"width\": 375, \"height\": 376}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-lin-movies-motion-aware-4d-dynamic-view-synthesis-in-one-second-cvpr-2026-paper/fig-024.webp\", \"caption\": \"\", \"page\": 5, \"index\": 24, \"width\": 374, \"height\": 376}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-lin-movies-motion-aware-4d-dynamic-view-synthesis-in-one-second-cvpr-2026-paper/fig-025.webp\", \"caption\": \"\", \"page\": 5, \"index\": 25, \"width\": 377, \"height\": 378}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-lin-movies-motion-aware-4d-dynamic-view-synthesis-in-one-second-cvpr-2026-paper/fig-026.webp\", \"caption\": \"\", \"page\": 5, \"index\": 26, \"width\": 375, \"height\": 377}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-lin-movies-motion-aware-4d-dynamic-view-synthesis-in-one-second-cvpr-2026-paper/fig-027.webp\", \"caption\": \"\", \"page\": 5, \"index\": 27, \"width\": 374, \"height\": 376}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-lin-movies-motion-aware-4d-dynamic-view-synthesis-in-one-second-cvpr-2026-paper/fig-028.webp\", \"caption\": \"\", \"page\": 5, \"index\": 28, \"width\": 375, \"height\": 376}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-lin-movies-motion-aware-4d-dynamic-view-synthesis-in-one-second-cvpr-2026-paper/fig-029.webp\", \"caption\": \"\", \"page\": 5, \"index\": 29, \"width\": 377, \"height\": 376}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-lin-movies-motion-aware-4d-dynamic-view-synthesis-in-one-second-cvpr-2026-paper/fig-030.webp\", \"caption\": \"\", \"page\": 5, \"index\": 30, \"width\": 377, \"height\": 377}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-lin-movies-motion-aware-4d-dynamic-view-synthesis-in-one-second-cvpr-2026-paper/fig-031.webp\", \"caption\": \"\", \"page\": 5, \"index\": 31, \"width\": 377, \"height\": 378}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-lin-movies-motion-aware-4d-dynamic-view-synthesis-in-one-second-cvpr-2026-paper/fig-032.webp\", \"caption\": \"\", \"page\": 5, \"index\": 32, \"width\": 376, \"height\": 377}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-lin-movies-motion-aware-4d-dynamic-view-synthesis-in-one-second-cvpr-2026-paper/fig-033.webp\", \"caption\": \"\", \"page\": 5, \"index\": 33, \"width\": 374, \"height\": 377}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-lin-movies-motion-aware-4d-dynamic-view-synthesis-in-one-second-cvpr-2026-paper/fig-034.webp\", \"caption\": \"\", \"page\": 5, \"index\": 34, \"width\": 377, \"height\": 377}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-lin-movies-motion-aware-4d-dynamic-view-synthesis-in-one-second-cvpr-2026-paper/fig-035.webp\", \"caption\": \"\", \"page\": 5, \"index\": 35, \"width\": 374, \"height\": 376}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-lin-movies-motion-aware-4d-dynamic-view-synthesis-in-one-second-cvpr-2026-paper/fig-036.webp\", \"caption\": \"\", \"page\": 5, \"index\": 36, \"width\": 374, \"height\": 376}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-lin-movies-motion-aware-4d-dynamic-view-synthesis-in-one-second-cvpr-2026-paper/fig-037.webp\", \"caption\": \"\", \"page\": 7, \"index\": 37, \"width\": 436, \"height\": 436}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-lin-movies-motion-aware-4d-dynamic-view-synthesis-in-one-second-cvpr-2026-paper/fig-038.webp\", \"caption\": \"\", \"page\": 7, \"index\": 38, \"width\": 436, \"height\": 434}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-lin-movies-motion-aware-4d-dynamic-view-synthesis-in-one-second-cvpr-2026-paper/fig-039.webp\", \"caption\": \"\", \"page\": 7, \"index\": 39, \"width\": 436, \"height\": 438}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-lin-movies-motion-aware-4d-dynamic-view-synthesis-in-one-second-cvpr-2026-paper/fig-040.webp\", \"caption\": \"\", \"page\": 7, \"index\": 40, \"width\": 436, \"height\": 438}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-lin-movies-motion-aware-4d-dynamic-view-synthesis-in-one-second-cvpr-2026-paper/fig-041.webp\", \"caption\": \"\", \"page\": 7, \"index\": 41, \"width\": 438, \"height\": 436}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-lin-movies-motion-aware-4d-dynamic-view-synthesis-in-one-second-cvpr-2026-paper/fig-042.webp\", \"caption\": \"\", \"page\": 7, \"index\": 42, \"width\": 440, \"height\": 438}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-lin-movies-motion-aware-4d-dynamic-view-synthesis-in-one-second-cvpr-2026-paper/fig-043.webp\", \"caption\": \"\", \"page\": 7, \"index\": 43, \"width\": 442, \"height\": 436}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-lin-movies-motion-aware-4d-dynamic-view-synthesis-in-one-second-cvpr-2026-paper/fig-044.webp\", \"caption\": \"\", \"page\": 7, \"index\": 44, \"width\": 438, \"height\": 436}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-lin-movies-motion-aware-4d-dynamic-view-synthesis-in-one-second-cvpr-2026-paper/fig-045.webp\", \"caption\": \"\", \"page\": 7, \"index\": 45, \"width\": 440, \"height\": 440}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-lin-movies-motion-aware-4d-dynamic-view-synthesis-in-one-second-cvpr-2026-paper/fig-046.webp\", \"caption\": \"\", \"page\": 7, \"index\": 46, \"width\": 438, \"height\": 440}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-lin-movies-motion-aware-4d-dynamic-view-synthesis-in-one-second-cvpr-2026-paper/fig-047.webp\", \"caption\": \"\", \"page\": 7, \"index\": 47, \"width\": 438, \"height\": 440}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-lin-movies-motion-aware-4d-dynamic-view-synthesis-in-one-second-cvpr-2026-paper/fig-048.webp\", \"caption\": \"\", \"page\": 7, \"index\": 48, \"width\": 436, \"height\": 430}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-lin-movies-motion-aware-4d-dynamic-view-synthesis-in-one-second-cvpr-2026-paper/fig-049.webp\", \"caption\": \"\", \"page\": 8, \"index\": 49, \"width\": 444, \"height\": 451}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-lin-movies-motion-aware-4d-dynamic-view-synthesis-in-one-second-cvpr-2026-paper/fig-050.webp\", \"caption\": \"\", \"page\": 8, \"index\": 50, \"width\": 440, \"height\": 451}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-lin-movies-motion-aware-4d-dynamic-view-synthesis-in-one-second-cvpr-2026-paper/fig-051.webp\", \"caption\": \"\", \"page\": 8, \"index\": 51, \"width\": 444, \"height\": 452}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-lin-movies-motion-aware-4d-dynamic-view-synthesis-in-one-second-cvpr-2026-paper/fig-052.webp\", \"caption\": \"\", \"page\": 8, \"index\": 52, \"width\": 445, \"height\": 451}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-lin-movies-motion-aware-4d-dynamic-view-synthesis-in-one-second-cvpr-2026-paper/fig-053.webp\", \"caption\": \"\", \"page\": 8, \"index\": 53, \"width\": 444, \"height\": 455}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-lin-movies-motion-aware-4d-dynamic-view-synthesis-in-one-second-cvpr-2026-paper/fig-054.webp\", \"caption\": \"\", \"page\": 8, \"index\": 54, \"width\": 441, \"height\": 455}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-lin-movies-motion-aware-4d-dynamic-view-synthesis-in-one-second-cvpr-2026-paper/fig-055.webp\", \"caption\": \"\", \"page\": 8, \"index\": 55, \"width\": 445, \"height\": 455}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-lin-movies-motion-aware-4d-dynamic-view-synthesis-in-one-second-cvpr-2026-paper/fig-056.webp\", \"caption\": \"\", \"page\": 8, \"index\": 56, \"width\": 435, \"height\": 446}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-lin-movies-motion-aware-4d-dynamic-view-synthesis-in-one-second-cvpr-2026-paper/fig-057.webp\", \"caption\": \"\", \"page\": 8, \"index\": 57, \"width\": 530, \"height\": 526}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-lin-movies-motion-aware-4d-dynamic-view-synthesis-in-one-second-cvpr-2026-paper/fig-058.webp\", \"caption\": \"\", \"page\": 8, \"index\": 58, \"width\": 532, \"height\": 525}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-lin-movies-motion-aware-4d-dynamic-view-synthesis-in-one-second-cvpr-2026-paper/fig-059.webp\", \"caption\": \"\", \"page\": 8, \"index\": 59, \"width\": 530, \"height\": 532}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-lin-movies-motion-aware-4d-dynamic-view-synthesis-in-one-second-cvpr-2026-paper/fig-060.webp\", \"caption\": \"\", \"page\": 8, \"index\": 60, \"width\": 444, \"height\": 452}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-lin-movies-motion-aware-4d-dynamic-view-synthesis-in-one-second-cvpr-2026-paper/fig-061.webp\", \"caption\": \"\", \"page\": 8, \"index\": 61, \"width\": 440, \"height\": 452}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-lin-movies-motion-aware-4d-dynamic-view-synthesis-in-one-second-cvpr-2026-paper/fig-062.webp\", \"caption\": \"\", \"page\": 8, \"index\": 62, \"width\": 441, \"height\": 452}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-lin-movies-motion-aware-4d-dynamic-view-synthesis-in-one-second-cvpr-2026-paper/fig-063.webp\", \"caption\": \"\", \"page\": 8, \"index\": 63, \"width\": 441, \"height\": 452}]"
motivation: 从单目视频重建四维动态场景难以统一建模外观、几何与运动，且依赖任务特定监督。
method: 用像素对齐高斯基元表示动态场景并显式监督其时变运动，在单一学习框架内统一重建、视图合成与三维点跟踪。
result: 约一秒内即可从单目视频重建四维动态场景，并支持场景流估计等零样本应用。
conclusion: 首次统一了动态重建、视图合成与点跟踪，推动了四维动态场景建模。
---

## Abstract
We present MoVieS, a Motion-aware View Synthesis model that reconstructs 4D dynamic scenes from monocular videos in one second. It represents dynamic 3D scenes with pixel-aligned Gaussian primitives and explicitly supervises their time-varying motions. This allows, for the first time, the unified modeling of appearance, geometry and motion from monocular videos, and enables reconstruction, view synthesis and 3D point tracking within a single learning-based framework. By bridging view synthesis with geometry reconstruction, MoVieS enables large-scale training on diverse datasets with minimal dependence on task-specific supervision. As a result, it also naturally supports a wide range of zero-shot applications, such as scene flow estimation and moving object segmentation. Extensive experiments validate the effectiveness and efficiency of MoVieS across multiple tasks, achieving competitive performance while offering several orders of magnitude speedups.

---

## 论文详细总结（自动生成）

# MoVieS 论文结构化总结

## 1. 核心问题与整体含义

- **研究动机**：人类能自然地从动态 3D 世界的连续观测中解读几何与运动。现有 3D 任务（单目深度估计、场景重建、新视角合成、点跟踪）多被**孤立处理**，且大部分视角合成/重建工作聚焦于**静态场景**，需要昂贵的**逐场景优化**，无法利用大规模先验知识。
- **核心痛点**：真实世界本质上是动态且多样的，而现有动态重建方法普遍存在以下问题：
  - 仅支持两帧输入、输出稀疏点云（DUSt3R 系列扩展）；
  - 依赖多阶段流水线、迭代优化与外部监督（光流、点跟踪），速度慢；
  - 难以统一建模外观、几何与运动，缺乏跨任务泛化能力。
- **整体含义**：论文提出 **MoVieS**（**Mo**tion-aware **Vie**w **S**ynthesis），首次在**单一学习框架**内，从单目视频中**统一建模外观、几何与运动**，并在**约 1 秒**内完成 4D 动态场景重建，支持重建、视角合成与 3D 点跟踪，并自然衍生出零样本应用。

---

## 2. 方法论

### 2.1 核心思想
- 用**可渲染、可形变的 3D 粒子**表示动态场景，称为 **Dynamic Splatter Pixel（动态泼溅像素）**；
- 将动态场景**解耦**为：一组**静态高斯基元** + 对应每个基元的**时变形变场**；
- 借助 3D 高斯泼溅（3DGS）可微渲染，把**新视角合成（NVS）作为代理任务**，反过来促进几何与运动的学习。

### 2.2 关键技术细节

- **动态泼溅像素表示**
  - 每个像素对应一个高斯基元 $g := \{x, a\}$，其中 $x \in \mathbb{R}^3$ 为规范空间（第一帧相机坐标系）位置，$a \in \mathbb{R}^{11}$ 包含旋转四元数 $q$、尺度 $s$、不透明度 $\alpha$、颜色 $c_{rgb}$。
  - 引入时间相关形变场 $m(t) := \{\Delta x(t), \Delta a(t)\}$，形变规则为：
    $$x \leftarrow x + \Delta x(t), \quad a \leftarrow a + \Delta a(t)$$

- **特征骨干**
  - 使用预训练图像编码器（DINOv2）逐帧提取特征，经 patchify + 位置编码；
  - 相机信息以**两种互补方式**注入：① **Plücker 嵌入**（像素对齐，空间相加）；② **相机 token**（线性层编码后拼接到 token 序列）；
  - 时间戳 $t_i \in [0,1]$ 经**正弦位置编码**生成时间 token；
  - 采用 VGGT 的**几何预训练注意力块**，实现跨帧 token 交互。

- **三个并行预测头（DPT 风格）**
  - **深度头（Depth Head）**：由 VGGT 初始化，预测每帧深度，为高斯构建提供空间定位；
  - **泼溅头（Splatter Head）**：从头训练，预测每个像素的高斯外观属性，并加入**RGB 直通捷径**（来自输入图像到最后一层卷积）保留高频细节；
  - **运动头（Motion Head）**：通过 **AdaLN** 注入查询时间 $t_q$，预测每个像素向 $t_q$ 的 3D 位移 $\Delta x$ 与属性形变 $\Delta a$。

- **训练目标**
  $$\mathcal{L} := \lambda_d \mathcal{L}_{depth} + \lambda_r \mathcal{L}_{rendering} + \lambda_m \mathcal{L}_{motion}$$
  - **深度损失**：预测深度与 GT 的 MSE + 空间梯度 L1；
  - **渲染损失**：MSE + LPIPS（$\lambda_{LPIPS}=0.5$）；
  - **运动损失**：点级 L1（稀疏性）+ **分布损失**（保持帧内相对距离结构），权重 $\lambda_m=10, \lambda_{pt}=1, \lambda_{dist}=10$；
  - 场景按平均欧氏距离做**尺度归一化**（同 VGGT），不使用置信度加权。

---

## 3. 实验设计

### 3.1 数据集与 Benchmark

| 任务 | 数据集 | 指标 |
|---|---|---|
| 静态 NVS | RealEstate10K | PSNR / SSIM / LPIPS |
| 动态 NVS | DyCheck（带共视掩码 mPSNR/mSSIM/mLPIPS）、NVIDIA 动态场景数据集 | PSNR / SSIM / LPIPS |
| 3D 点跟踪 | TAPVid-3D 基准（Aria Digital Twin、DriveTrack、Panoptic Studio） | EPE3D、δ0.05 3D、δ0.10 3D |
| 野外鲁棒性 | DAVIS（相机位姿由 MegaSaM 估计） | 定性 |

### 3.2 训练数据集（8 个异构来源）
RealEstate10K（70K 静态）、TartanAir、MatrixCity、PointOdyssey、DynamicReplica、Spring、VKITTI2、Stereo4D（98K 真实动态），覆盖动态/深度/跟踪标注的不同组合。

### 3.3 对比方法
- **静态前馈**：DepthSplat、GS-LRM（作者重实现）；
- **动态优化式**：Splatter-a-Video、Shape-of-Motion、MoSca；
- **点跟踪**：BootsTAPIR†、CoTracker3†（2D 跟踪 + 深度反投影）、SpatialTracker（原生 3D）；
- 所有方法均提供**相同相机参数**以保证公平。

---

## 4. 资源与算力

- **训练硬件**：**32 × H20 GPU**；
- **训练时长**：约 **5 天**；
- **优化配置**：AdamW + 余弦学习率 + 线性 warm-up；
- **效率技术**：gsplat 渲染后端、DeepSpeed、梯度检查点、梯度累积、bf16 混合精度；
- **训练策略**：采用**课程学习**，分三阶段——① 静态场景预训练 → ② 变视角动态场景 → ③ 高分辨率微调；
- **新嵌入初始化**：相机/时间嵌入**零初始化**以稳定训练。

---

## 5. 实验数量与充分性

### 5.1 实验组数概览
- **主实验 3 大类**：静态 NVS、动态 NVS、3D 点跟踪；
- **消融实验 4 组**：
  1. **相机条件**（4 种设置：无 / Plücker / 相机 token / 组合）；
  2. **运动监督**（4 种设置：无 / 逐点 L1 / 分布损失 / 组合）；
  3. **运动与 NVS 协同**（3 种设置：NVS 无运动 / 运动无 NVS / 联合）；
  4. **VGGT 初始化**（VGGT 初始化 vs 从头训练，定量 + 定性）；
- **零样本应用 2 项**：场景流估计、运动物体分割；
- **定性对比**：Figure 3（NVS）、Figure 4（运动可视化）、Figure 5（零样本应用）。

### 5.2 充分性与公平性评估
- **优点**：多数据集、多任务、多基线、多消融，覆盖较为完整；对相机参数做了统一处理；DyCheck 使用共视掩码计算指标；对 2D 跟踪基线统一用深度模型反投影，保证公平。
- **可商榷之处**：部分数据集（如 DyCheck、NVIDIA）仅使用小规模子集；部分结论（如零样本应用）主要以**定性可视化**呈现，缺少定量评测；VGGT 初始化对比分辨率降至 224×224，与主实验设置不完全一致。

---

## 6. 主要结论与发现

- **统一建模可行且高效**：单一模型可在 **0.93 秒/场景**内完成动态场景重建，相较优化式方法（10–45 分钟）实现**数个数量级加速**；
- **动态 NVS 表现优异**：DyCheck 上 mPSNR 18.46（vs MoSca 18.24）、mSSIM 58.87（vs 55.14）；NVIDIA 数据集上 PSNR 19.16（略低于 MoSca 的 21.45），但 MoSca 存在过拟合、伪影严重的问题；
- **静态场景自适应**：静态输入时预测运动自然收敛至零（< 1e-3），说明模型能**隐式区分静态/动态区域**；
- **3D 点跟踪优势明显**：EPE3D 显著低于所有基线（如 Aria Digital Twin 0.2153 vs 0.5413），δ 指标

δ 指标（δ0.05、δ0.10）同样大幅领先，表明模型不仅能降低平均误差，还能在**困难点、快速运动点**上保持较高的命中率；在 DriveTrack、Panoptic Studio 上均保持一致的领先趋势，说明该优势来自**统一的几何—运动表征**，而非针对单一数据集调参。
- **消融结论清晰**：
  - **相机条件**：Plücker 嵌入与相机 token **联合使用**最优，单独使用任一方式均有下降，说明二者提供的空间/全局信息互补；
  - **运动监督**：逐点 L1 与分布损失**联合**效果最佳，分布损失单独使用也能带来可观提升，验证了"保持帧内相对结构"这一先验的有效性；
  - **运动与 NVS 协同**：联合训练 > 仅 NVS > 仅运动，证明**新视角合成作为代理任务**能反哺几何与运动学习，二者互相受益而非此消彼长；
  - **VGGT 初始化**：相比从头训练，几何预训练注意力块带来了更好的深度精度与更快的收敛，且在运动预测上也有正向迁移。
- **零样本能力**：在未显式监督的任务上（场景流估计、运动物体分割），模型能直接输出合理的运动场与动态区域掩码，说明其学到的形变场具有**任务无关的物理一致性**。
- **野外泛化**：在 DAVIS 上配合外部位姿估计器（MegaSaM）仍能生成时序稳定的 4D 重建，说明模型对相机参数噪声与真实场景复杂性具有一定鲁棒性。

---

## 7. 局限与批判性讨论

- **对相机位姿的依赖**：动态 NVS 与点跟踪任务中，模型仍需输入相机参数（或由外部方法估计）。在野外场景中，位姿误差会直接传播到高斯定位与运动预测，缺乏联合优化位姿的机制。
- **动态表示的物理约束不足**：形变场为**逐像素独立预测**，未显式建模刚体/关节约束，长序列或大运动下可能出现"非物理"漂移（尽管分布损失部分缓解了该问题）。
- **评测规模有限**：DyCheck、NVIDIA 等动态基准仅使用小子集，且部分对比方法为作者重实现，绝对数值的可比性需谨慎对待；零样本应用缺少定量指标，说服力弱于主实验。
- **计算成本与可及性**：训练需要 32×H20、约 5 天，复现门槛较高；尽管推理只需约 1 秒/场景，但训练侧的资源需求限制了社区跟进与公平比较。
- **代理任务的偏差**：以 NVS 作为核心代理目标，可能使几何/运动向"渲染友好"而非"度量准确"方向优化，点跟踪的高精度或许部分来自深度归一化与训练数据分布的巧合。
- **静态/动态判别**：模型"隐式"将静态输入的运动收敛至零，但论文未深入分析其在**长时间静态背景 + 局部运动**场景下是否会误判，也缺少对失败案例的系统剖析。

---

## 8. 总体评价与启示

- **方法论价值**：MoVieS 的核心贡献不在于某一项指标刷新，而在于给出了一种**"外观—几何—运动"统一的可微表征范式**：用可渲染的 3D 粒子承载几何与外观，用形变场承载运动，用 NVS 作为统一监督信号。这一思路可自然扩展到 4D 生成、动态资产重建等方向。
- **工程价值**：把此前需要逐场景优化、耗时数十分钟的动态重建压缩到**前馈、约 1 秒**，配合课程学习与几何预训练初始化，展示了大规模异构数据（8 个来源、约 168K 序列）联合训练在动态 3D 任务上的可行性。
- **实验设计评价**：任务覆盖（静态 NVS、动态 NVS、3D 跟踪）+ 四组消融 + 零样本应用，结构完整、逻辑闭环；消融设计针对性强，能有效归因各组件贡献。主要短板在于部分基准规模偏小、零样本评测偏定性、以及训练资源带来的复现壁垒。
- **后续研究方向**：① 位姿与几何/运动的**联合优化**；② 引入刚体/关节等**结构化运动先验**；③ 扩展到更长视频与更大场景；④ 建立更标准化、更大规模的动态 4D 评测基准。

---

（完）
