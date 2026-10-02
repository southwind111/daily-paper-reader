---
title: "SLAM3R: Real-Time Dense Scene Reconstruction from Monocular RGB Videos"
title_zh: SLAM3R：基于单目RGB视频的实时稠密场景重建
authors: "Liu, Yuzheng, Dong, Siyan, Wang, Shuzhe, Yin, Yingda, Yang, Yanchao, Fan, Qingnan, Chen, Baoquan"
date: 2025
publication_date: 2025
publication_date_precision: year
publication_date_source: conference year only; exact release date unverified
publication_date_kind: unknown
pdf: "https://openaccess.thecvf.com/content/CVPR2025/papers/Liu_SLAM3R_Real-Time_Dense_Scene_Reconstruction_from_Monocular_RGB_Videos_CVPR_2025_paper.pdf"
tags: ["query:dr"]
score: 5.0
evidence: 基于前馈网络从单目RGB视频实时稠密重建三维场景
tldr: 实时高质量稠密三维重建是重要但困难的任务，传统方法依赖位姿优化。本文提出SLAM3R系统，通过前馈神经网络无缝整合局部重建与全局坐标配准，先用滑动窗口将输入视频转为重叠片段，再直接从RGB图像回归三维点图并渐进对齐与形变，从而构建全局一致的场景重建。方法无需显式求解相机参数，在多个数据集上实现实时高质量的稠密重建效果，为实时场景重建提供了新思路。
source: CVPR-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-liu-slam3r-real-time-dense-scene-reconstruction-from-monocular-rgb-videos-cvpr-2025-paper/fig-001.webp\", \"caption\": \"\", \"page\": 1, \"index\": 1, \"width\": 1900, \"height\": 1706}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-liu-slam3r-real-time-dense-scene-reconstruction-from-monocular-rgb-videos-cvpr-2025-paper/fig-002.webp\", \"caption\": \"\", \"page\": 4, \"index\": 2, \"width\": 2844, \"height\": 792}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-liu-slam3r-real-time-dense-scene-reconstruction-from-monocular-rgb-videos-cvpr-2025-paper/fig-003.webp\", \"caption\": \"\", \"page\": 4, \"index\": 3, \"width\": 1404, \"height\": 1002}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-liu-slam3r-real-time-dense-scene-reconstruction-from-monocular-rgb-videos-cvpr-2025-paper/fig-004.webp\", \"caption\": \"\", \"page\": 6, \"index\": 4, \"width\": 2867, \"height\": 895}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-liu-slam3r-real-time-dense-scene-reconstruction-from-monocular-rgb-videos-cvpr-2025-paper/fig-005.webp\", \"caption\": \"\", \"page\": 7, \"index\": 5, \"width\": 2876, \"height\": 1364}]"
motivation: 传统基于位姿优化的方法难以实时高质量地稠密重建场景。
method: 提出端到端系统SLAM3R，用滑窗将视频转为重叠片段，以前馈网络直接回归三维点图并渐进对齐融合。
result: 无需显式求解相机参数即可生成全局一致的稠密重建，跨数据集实现实时高质量效果。
conclusion: 为实时稠密场景重建提供了无需位姿优化的新途径。
---

## Abstract
In this paper, we introduce SLAM3R, a novel and effective system for real-time, high-quality, dense 3D reconstruction using RGB videos. SLAM3R provides an end-to-end solution by seamlessly integrating local 3D reconstruction and global coordinate registration through feed-forward neural networks. Given an input video, the system first converts it into overlapping clips using a sliding window mechanism. Unlike traditional pose optimization-based methods, SLAM3R directly regresses 3D pointmaps from RGB images in each window and progressively aligns and deforms these local pointmaps to create a globally consistent scene reconstruction - all without explicitly solving any camera parameters. Experiments across datasets consistently show that SLAM3R achieves state-of-the-art reconstruction accuracy and completeness while maintaining real-time performance at 20+ FPS. Code available at: https://github.com/PKU-VCL-3DV/SLAM3R.

---

## 论文详细总结（自动生成）

# SLAM3R 论文中文总结

## 1. 核心问题与整体含义
- **研究动机**：稠密三维场景重建是计算机视觉长期难题。传统方法多依赖 SfM/SLAM 估计相机参数，再用 MVS 或神经隐式/3DGS 表示补全细节，通常需要离线处理，难以实时应用。
- **背景痛点**：现有稠密 SLAM 方法难以同时满足三个关键指标：重建精度、完整性、运行效率。单目稠密 SLAM 如 NICER-SLAM 速度常低于 1 FPS；DUSt3R 双视图实时，但多视图需全局优化，效率受限；Spann3R 增量式扩展到视频，但存在明显累积漂移。
- **核心问题**：如何仅用单目 RGB 视频，在无需显式求解相机参数的前提下，实现实时、高质量、稠密的全局一致三维场景重建。
- **整体含义**：SLAM3R 将问题重新定义为“隐式相机定位 + 稠密场景建图”，通过端到端前馈网络直接回归三维点图并增量配准到全局坐标，在 20+ FPS 下兼顾重建质量与效率。

## 2. 方法论
### 2.1 核心思想
- 采用**两层级联框架**：
  - **Image-to-Points（I2P）**：从滑动窗口视频片段中恢复局部稠密三维点图。
  - **Local-to-World（L2W）**：将局部点图增量配准到统一全局坐标系。
- 全程**不显式求解相机内外参**，而是直接预测统一坐标系下的三维点图和置信度。
- 滑动窗口默认步长为 1，确保每帧至少一次作为关键帧。

### 2.2 I2P：窗口内局部重建
- 将视频切成长度为 L 的窗口，默认选窗口中间帧为关键帧，其余为支持帧。
- 网络基于多分支 ViT：
  - 共享图像编码器独立并行编码各帧。
  - **关键帧解码器 Dkey**：关键帧 token
