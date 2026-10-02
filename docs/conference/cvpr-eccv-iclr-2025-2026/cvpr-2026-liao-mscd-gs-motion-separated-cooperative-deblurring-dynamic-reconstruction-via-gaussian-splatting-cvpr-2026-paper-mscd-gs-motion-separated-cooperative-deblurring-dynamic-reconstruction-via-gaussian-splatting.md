---
title: "MSCD-GS: Motion-Separated Cooperative Deblurring Dynamic Reconstruction via Gaussian Splatting"
title_zh: MSCD-GS：基于高斯泼溅的运动分离协同去模糊动态重建
authors: "Liao, Yongjian, Zou, Xu, Chen, Wenjun, Li, Huixuan, Xie, Xiaoen, Li, Chunxi, Huang, Shixiang, Zhang, Gang, Zhou, Jiahuan, Zhong, Sheng, Yan, Luxin"
date: 2026
publication_date: 2026
publication_date_precision: year
publication_date_source: conference year only; exact release date unverified
publication_date_kind: unknown
pdf: "https://openaccess.thecvf.com/content/CVPR2026/papers/Liao_MSCD-GS_Motion-Separated_Cooperative_Deblurring_Dynamic_Reconstruction_via_Gaussian_Splatting_CVPR_2026_paper.pdf"
tags: ["query:dr"]
score: 9.0
evidence: 基于高斯泼溅的去模糊4D动态重建
tldr: 基于高斯泼溅的4D重建虽成果显著，但随意单目相机拍摄的动态图像因相机与物体在曝光期间运动而产生严重运动模糊，现有去模糊高斯模型难以应对真实动态场景。本文提出MSCD-GS，通过运动分离协同去模糊的4D高斯泼溅方法分离并联合优化相机与物体运动。实验表明其能有效处理运动模糊，提升重建质量与新视角合成效果。
source: CVPR-2026-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liao-mscd-gs-motion-separated-cooperative-deblurring-dynamic-reconstruction-via-gaussian-splatting-cvpr-2026-paper/fig-001.webp\", \"caption\": \"\", \"page\": 1, \"index\": 1, \"width\": 1280, \"height\": 720}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liao-mscd-gs-motion-separated-cooperative-deblurring-dynamic-reconstruction-via-gaussian-splatting-cvpr-2026-paper/fig-002.webp\", \"caption\": \"\", \"page\": 1, \"index\": 2, \"width\": 1280, \"height\": 720}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liao-mscd-gs-motion-separated-cooperative-deblurring-dynamic-reconstruction-via-gaussian-splatting-cvpr-2026-paper/fig-003.webp\", \"caption\": \"\", \"page\": 1, \"index\": 3, \"width\": 1280, \"height\": 720}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liao-mscd-gs-motion-separated-cooperative-deblurring-dynamic-reconstruction-via-gaussian-splatting-cvpr-2026-paper/fig-004.webp\", \"caption\": \"\", \"page\": 1, \"index\": 4, \"width\": 1280, \"height\": 720}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liao-mscd-gs-motion-separated-cooperative-deblurring-dynamic-reconstruction-via-gaussian-splatting-cvpr-2026-paper/fig-005.webp\", \"caption\": \"\", \"page\": 1, \"index\": 5, \"width\": 1280, \"height\": 720}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liao-mscd-gs-motion-separated-cooperative-deblurring-dynamic-reconstruction-via-gaussian-splatting-cvpr-2026-paper/fig-006.webp\", \"caption\": \"\", \"page\": 3, \"index\": 6, \"width\": 1280, \"height\": 720}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liao-mscd-gs-motion-separated-cooperative-deblurring-dynamic-reconstruction-via-gaussian-splatting-cvpr-2026-paper/fig-007.webp\", \"caption\": \"\", \"page\": 3, \"index\": 7, \"width\": 1280, \"height\": 720}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liao-mscd-gs-motion-separated-cooperative-deblurring-dynamic-reconstruction-via-gaussian-splatting-cvpr-2026-paper/fig-008.webp\", \"caption\": \"\", \"page\": 3, \"index\": 8, \"width\": 1280, \"height\": 720}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liao-mscd-gs-motion-separated-cooperative-deblurring-dynamic-reconstruction-via-gaussian-splatting-cvpr-2026-paper/fig-009.webp\", \"caption\": \"\", \"page\": 3, \"index\": 9, \"width\": 1280, \"height\": 720}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liao-mscd-gs-motion-separated-cooperative-deblurring-dynamic-reconstruction-via-gaussian-splatting-cvpr-2026-paper/fig-010.webp\", \"caption\": \"\", \"page\": 3, \"index\": 10, \"width\": 1280, \"height\": 720}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liao-mscd-gs-motion-separated-cooperative-deblurring-dynamic-reconstruction-via-gaussian-splatting-cvpr-2026-paper/fig-011.webp\", \"caption\": \"\", \"page\": 3, \"index\": 11, \"width\": 1280, \"height\": 720}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liao-mscd-gs-motion-separated-cooperative-deblurring-dynamic-reconstruction-via-gaussian-splatting-cvpr-2026-paper/fig-012.webp\", \"caption\": \"\", \"page\": 3, \"index\": 12, \"width\": 1280, \"height\": 720}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liao-mscd-gs-motion-separated-cooperative-deblurring-dynamic-reconstruction-via-gaussian-splatting-cvpr-2026-paper/fig-013.webp\", \"caption\": \"\", \"page\": 3, \"index\": 13, \"width\": 1280, \"height\": 720}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liao-mscd-gs-motion-separated-cooperative-deblurring-dynamic-reconstruction-via-gaussian-splatting-cvpr-2026-paper/fig-014.webp\", \"caption\": \"\", \"page\": 6, \"index\": 14, \"width\": 1280, \"height\": 720}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liao-mscd-gs-motion-separated-cooperative-deblurring-dynamic-reconstruction-via-gaussian-splatting-cvpr-2026-paper/fig-015.webp\", \"caption\": \"\", \"page\": 6, \"index\": 15, \"width\": 1280, \"height\": 720}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liao-mscd-gs-motion-separated-cooperative-deblurring-dynamic-reconstruction-via-gaussian-splatting-cvpr-2026-paper/fig-016.webp\", \"caption\": \"\", \"page\": 6, \"index\": 16, \"width\": 1280, \"height\": 720}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liao-mscd-gs-motion-separated-cooperative-deblurring-dynamic-reconstruction-via-gaussian-splatting-cvpr-2026-paper/fig-017.webp\", \"caption\": \"\", \"page\": 6, \"index\": 17, \"width\": 1280, \"height\": 720}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liao-mscd-gs-motion-separated-cooperative-deblurring-dynamic-reconstruction-via-gaussian-splatting-cvpr-2026-paper/fig-018.webp\", \"caption\": \"\", \"page\": 6, \"index\": 18, \"width\": 1280, \"height\": 720}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liao-mscd-gs-motion-separated-cooperative-deblurring-dynamic-reconstruction-via-gaussian-splatting-cvpr-2026-paper/fig-019.webp\", \"caption\": \"\", \"page\": 6, \"index\": 19, \"width\": 1280, \"height\": 720}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liao-mscd-gs-motion-separated-cooperative-deblurring-dynamic-reconstruction-via-gaussian-splatting-cvpr-2026-paper/fig-020.webp\", \"caption\": \"\", \"page\": 6, \"index\": 20, \"width\": 1280, \"height\": 720}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liao-mscd-gs-motion-separated-cooperative-deblurring-dynamic-reconstruction-via-gaussian-splatting-cvpr-2026-paper/fig-021.webp\", \"caption\": \"\", \"page\": 6, \"index\": 21, \"width\": 1280, \"height\": 720}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liao-mscd-gs-motion-separated-cooperative-deblurring-dynamic-reconstruction-via-gaussian-splatting-cvpr-2026-paper/fig-022.webp\", \"caption\": \"\", \"page\": 6, \"index\": 22, \"width\": 1280, \"height\": 720}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liao-mscd-gs-motion-separated-cooperative-deblurring-dynamic-reconstruction-via-gaussian-splatting-cvpr-2026-paper/fig-023.webp\", \"caption\": \"\", \"page\": 6, \"index\": 23, \"width\": 1280, \"height\": 720}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liao-mscd-gs-motion-separated-cooperative-deblurring-dynamic-reconstruction-via-gaussian-splatting-cvpr-2026-paper/fig-024.webp\", \"caption\": \"\", \"page\": 6, \"index\": 24, \"width\": 1280, \"height\": 720}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liao-mscd-gs-motion-separated-cooperative-deblurring-dynamic-reconstruction-via-gaussian-splatting-cvpr-2026-paper/fig-025.webp\", \"caption\": \"\", \"page\": 6, \"index\": 25, \"width\": 1280, \"height\": 720}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liao-mscd-gs-motion-separated-cooperative-deblurring-dynamic-reconstruction-via-gaussian-splatting-cvpr-2026-paper/fig-026.webp\", \"caption\": \"\", \"page\": 6, \"index\": 26, \"width\": 1280, \"height\": 720}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liao-mscd-gs-motion-separated-cooperative-deblurring-dynamic-reconstruction-via-gaussian-splatting-cvpr-2026-paper/fig-027.webp\", \"caption\": \"\", \"page\": 6, \"index\": 27, \"width\": 1280, \"height\": 720}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liao-mscd-gs-motion-separated-cooperative-deblurring-dynamic-reconstruction-via-gaussian-splatting-cvpr-2026-paper/fig-028.webp\", \"caption\": \"\", \"page\": 6, \"index\": 28, \"width\": 1280, \"height\": 720}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liao-mscd-gs-motion-separated-cooperative-deblurring-dynamic-reconstruction-via-gaussian-splatting-cvpr-2026-paper/fig-029.webp\", \"caption\": \"\", \"page\": 6, \"index\": 29, \"width\": 1280, \"height\": 720}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liao-mscd-gs-motion-separated-cooperative-deblurring-dynamic-reconstruction-via-gaussian-splatting-cvpr-2026-paper/fig-030.webp\", \"caption\": \"\", \"page\": 6, \"index\": 30, \"width\": 1280, \"height\": 720}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liao-mscd-gs-motion-separated-cooperative-deblurring-dynamic-reconstruction-via-gaussian-splatting-cvpr-2026-paper/fig-031.webp\", \"caption\": \"\", \"page\": 6, \"index\": 31, \"width\": 1280, \"height\": 720}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liao-mscd-gs-motion-separated-cooperative-deblurring-dynamic-reconstruction-via-gaussian-splatting-cvpr-2026-paper/fig-032.webp\", \"caption\": \"\", \"page\": 6, \"index\": 32, \"width\": 1280, \"height\": 720}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liao-mscd-gs-motion-separated-cooperative-deblurring-dynamic-reconstruction-via-gaussian-splatting-cvpr-2026-paper/fig-033.webp\", \"caption\": \"\", \"page\": 6, \"index\": 33, \"width\": 1280, \"height\": 720}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liao-mscd-gs-motion-separated-cooperative-deblurring-dynamic-reconstruction-via-gaussian-splatting-cvpr-2026-paper/fig-034.webp\", \"caption\": \"\", \"page\": 6, \"index\": 34, \"width\": 1280, \"height\": 720}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liao-mscd-gs-motion-separated-cooperative-deblurring-dynamic-reconstruction-via-gaussian-splatting-cvpr-2026-paper/fig-035.webp\", \"caption\": \"\", \"page\": 6, \"index\": 35, \"width\": 1280, \"height\": 720}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liao-mscd-gs-motion-separated-cooperative-deblurring-dynamic-reconstruction-via-gaussian-splatting-cvpr-2026-paper/fig-036.webp\", \"caption\": \"\", \"page\": 6, \"index\": 36, \"width\": 1280, \"height\": 720}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liao-mscd-gs-motion-separated-cooperative-deblurring-dynamic-reconstruction-via-gaussian-splatting-cvpr-2026-paper/fig-037.webp\", \"caption\": \"\", \"page\": 6, \"index\": 37, \"width\": 1280, \"height\": 720}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liao-mscd-gs-motion-separated-cooperative-deblurring-dynamic-reconstruction-via-gaussian-splatting-cvpr-2026-paper/fig-038.webp\", \"caption\": \"\", \"page\": 7, \"index\": 38, \"width\": 960, \"height\": 540}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liao-mscd-gs-motion-separated-cooperative-deblurring-dynamic-reconstruction-via-gaussian-splatting-cvpr-2026-paper/fig-039.webp\", \"caption\": \"\", \"page\": 7, \"index\": 39, \"width\": 960, \"height\": 540}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liao-mscd-gs-motion-separated-cooperative-deblurring-dynamic-reconstruction-via-gaussian-splatting-cvpr-2026-paper/fig-040.webp\", \"caption\": \"\", \"page\": 7, \"index\": 40, \"width\": 960, \"height\": 540}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liao-mscd-gs-motion-separated-cooperative-deblurring-dynamic-reconstruction-via-gaussian-splatting-cvpr-2026-paper/fig-041.webp\", \"caption\": \"\", \"page\": 7, \"index\": 41, \"width\": 960, \"height\": 540}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liao-mscd-gs-motion-separated-cooperative-deblurring-dynamic-reconstruction-via-gaussian-splatting-cvpr-2026-paper/fig-042.webp\", \"caption\": \"\", \"page\": 7, \"index\": 42, \"width\": 960, \"height\": 540}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liao-mscd-gs-motion-separated-cooperative-deblurring-dynamic-reconstruction-via-gaussian-splatting-cvpr-2026-paper/fig-043.webp\", \"caption\": \"\", \"page\": 7, \"index\": 43, \"width\": 960, \"height\": 540}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liao-mscd-gs-motion-separated-cooperative-deblurring-dynamic-reconstruction-via-gaussian-splatting-cvpr-2026-paper/fig-044.webp\", \"caption\": \"\", \"page\": 7, \"index\": 44, \"width\": 960, \"height\": 540}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liao-mscd-gs-motion-separated-cooperative-deblurring-dynamic-reconstruction-via-gaussian-splatting-cvpr-2026-paper/fig-045.webp\", \"caption\": \"\", \"page\": 7, \"index\": 45, \"width\": 960, \"height\": 540}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liao-mscd-gs-motion-separated-cooperative-deblurring-dynamic-reconstruction-via-gaussian-splatting-cvpr-2026-paper/fig-046.webp\", \"caption\": \"\", \"page\": 7, \"index\": 46, \"width\": 960, \"height\": 540}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liao-mscd-gs-motion-separated-cooperative-deblurring-dynamic-reconstruction-via-gaussian-splatting-cvpr-2026-paper/fig-047.webp\", \"caption\": \"\", \"page\": 7, \"index\": 47, \"width\": 960, \"height\": 540}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liao-mscd-gs-motion-separated-cooperative-deblurring-dynamic-reconstruction-via-gaussian-splatting-cvpr-2026-paper/fig-048.webp\", \"caption\": \"\", \"page\": 7, \"index\": 48, \"width\": 960, \"height\": 540}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liao-mscd-gs-motion-separated-cooperative-deblurring-dynamic-reconstruction-via-gaussian-splatting-cvpr-2026-paper/fig-049.webp\", \"caption\": \"\", \"page\": 7, \"index\": 49, \"width\": 960, \"height\": 540}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liao-mscd-gs-motion-separated-cooperative-deblurring-dynamic-reconstruction-via-gaussian-splatting-cvpr-2026-paper/fig-050.webp\", \"caption\": \"\", \"page\": 7, \"index\": 50, \"width\": 960, \"height\": 540}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liao-mscd-gs-motion-separated-cooperative-deblurring-dynamic-reconstruction-via-gaussian-splatting-cvpr-2026-paper/fig-051.webp\", \"caption\": \"\", \"page\": 7, \"index\": 51, \"width\": 960, \"height\": 540}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liao-mscd-gs-motion-separated-cooperative-deblurring-dynamic-reconstruction-via-gaussian-splatting-cvpr-2026-paper/fig-052.webp\", \"caption\": \"\", \"page\": 7, \"index\": 52, \"width\": 960, \"height\": 540}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liao-mscd-gs-motion-separated-cooperative-deblurring-dynamic-reconstruction-via-gaussian-splatting-cvpr-2026-paper/fig-053.webp\", \"caption\": \"\", \"page\": 7, \"index\": 53, \"width\": 960, \"height\": 540}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liao-mscd-gs-motion-separated-cooperative-deblurring-dynamic-reconstruction-via-gaussian-splatting-cvpr-2026-paper/fig-054.webp\", \"caption\": \"\", \"page\": 7, \"index\": 54, \"width\": 960, \"height\": 540}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liao-mscd-gs-motion-separated-cooperative-deblurring-dynamic-reconstruction-via-gaussian-splatting-cvpr-2026-paper/fig-055.webp\", \"caption\": \"\", \"page\": 7, \"index\": 55, \"width\": 960, \"height\": 540}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liao-mscd-gs-motion-separated-cooperative-deblurring-dynamic-reconstruction-via-gaussian-splatting-cvpr-2026-paper/fig-056.webp\", \"caption\": \"\", \"page\": 7, \"index\": 56, \"width\": 960, \"height\": 540}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liao-mscd-gs-motion-separated-cooperative-deblurring-dynamic-reconstruction-via-gaussian-splatting-cvpr-2026-paper/fig-057.webp\", \"caption\": \"\", \"page\": 7, \"index\": 57, \"width\": 960, \"height\": 540}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liao-mscd-gs-motion-separated-cooperative-deblurring-dynamic-reconstruction-via-gaussian-splatting-cvpr-2026-paper/fig-058.webp\", \"caption\": \"\", \"page\": 8, \"index\": 58, \"width\": 1280, \"height\": 720}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liao-mscd-gs-motion-separated-cooperative-deblurring-dynamic-reconstruction-via-gaussian-splatting-cvpr-2026-paper/fig-059.webp\", \"caption\": \"\", \"page\": 8, \"index\": 59, \"width\": 1280, \"height\": 720}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liao-mscd-gs-motion-separated-cooperative-deblurring-dynamic-reconstruction-via-gaussian-splatting-cvpr-2026-paper/fig-060.webp\", \"caption\": \"\", \"page\": 8, \"index\": 60, \"width\": 1280, \"height\": 720}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liao-mscd-gs-motion-separated-cooperative-deblurring-dynamic-reconstruction-via-gaussian-splatting-cvpr-2026-paper/fig-061.webp\", \"caption\": \"\", \"page\": 8, \"index\": 61, \"width\": 1280, \"height\": 720}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liao-mscd-gs-motion-separated-cooperative-deblurring-dynamic-reconstruction-via-gaussian-splatting-cvpr-2026-paper/fig-062.webp\", \"caption\": \"\", \"page\": 8, \"index\": 62, \"width\": 1280, \"height\": 720}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liao-mscd-gs-motion-separated-cooperative-deblurring-dynamic-reconstruction-via-gaussian-splatting-cvpr-2026-paper/fig-063.webp\", \"caption\": \"\", \"page\": 8, \"index\": 63, \"width\": 1280, \"height\": 720}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liao-mscd-gs-motion-separated-cooperative-deblurring-dynamic-reconstruction-via-gaussian-splatting-cvpr-2026-paper/fig-064.webp\", \"caption\": \"\", \"page\": 8, \"index\": 64, \"width\": 1280, \"height\": 720}]"
motivation: 随意单目相机拍摄的动态图像存在严重运动模糊，现有去模糊高斯模型难以处理真实动态场景。
method: 提出运动分离协同去模糊的4D高斯泼溅方法，分离并联合优化相机与物体运动。
result: 有效处理运动模糊，提升重建质量与新视角合成效果。
conclusion: 拓展了4D高斯泼溅在真实模糊动态场景中的适用性。
---

## Abstract
Although 4D reconstruction based on Gaussian Splatting has achieved many impressive results, reconstructing real-world images captured by a casual monocular camera remains a significant challenge. In dynamic scenes, as the camera and objects move during the exposure time, these input images inevitably contain a considerable amount of motion blur, which severely compromises the quality of reconstruction and new viewpoint synthesis. The existing deblurring 3D Gaussian models still cannot handle motion blur issues in real dynamic scenes. To address these challenges, we propose MSCD-GS--a novel method for motion-separated collaborative deblurring 4D reconstruction via Gaussian Splatting, capable of effectively handling motion-blurred inputs. Specifically, due to the distinct motion characteristics of static and dynamic Gaussians, we perform separate motion models for dynamic scene reconstruction. To predict Gaussian changes over exposure time, we designed motion-aware networks for static and dynamic Gaussians, thereby synthesizing virtual blurred images. Finally, we utilize the results from the deblurring network and the synthesized images to supervise 4D reconstruction collaboratively. Extensive experiments demonstrate that MSCD-GS can effectively reconstruct high-quality dynamic scenes from blurred image inputs, with performance surpassing existing methods.

---

## 论文详细总结（自动生成）

# MSCD-GS 论文总结

## 1. 核心问题与整体含义（研究动机与背景）

- **研究背景**：基于高斯泼溅（Gaussian Splatting）的 4D 重建已在动态场景建模与实时渲染上取得显著成果，但在"随手拍摄的单目相机"这一真实场景下仍面临巨大挑战。
- **核心问题**：在动态场景中，曝光时间内相机与物体同时运动，导致输入图像不可避免地包含大量**运动模糊**，严重损害重建质量与新视角合成效果。运动模糊可细分为：
  - **相机运动模糊**：曝光期间相机位姿变化所致；
  - **物体运动模糊**：物体与相机运动交织所致，处理难度更大。
- **现有方法的不足**：
  - 面向相机运动模糊的 NeRF/3DGS 方法（通过曝光时间内生成虚拟帧合成模糊图）仅适用于静态背景，无法解决物体运动模糊；
  - BARD-GS、Deblur4DGS 等 4D 去模糊方法虽能同时处理两类模糊并保持实时渲染，但**高度依赖大量先验数据**（深度图、轨迹、光流等）；
  - 基于深度网络的图像去模糊方法（如 NAFNet）缺乏 3D 空间感知，仅凭单帧恢复细节，效果有限，且**其去模糊能力决定重建性能的下限**（见表 1）；
  - 直接将去模糊模型与 4DGS 简单拼接不可行，因为去模糊结果不一致。
- **整体含义**：本文提出 MSCD-GS，将去模糊模型与 4DGS **高效协同融合**，在不依赖大量先验数据的条件下，从运动模糊输入实现高质量 4D 动态重建。

## 2. 方法论

### 2.1 核心思想
- 依据静态与动态高斯**运动特性不同**，对二者分别建模运动轨迹，并设计轻量级**运动感知网络（MLP）**预测其在曝光时间内的变化，从而合成虚拟模糊图像，并与去模糊网络结果**协同监督** 4D 重建。

### 2.2 关键技术细节与流程

- **运动模糊建模**：模糊图像 B 视为曝光时间 [τs, τe] 内 N 张虚拟清晰图像 I(Pτ) 的积分，并离散化为 N 个时间戳的均值。
- **3DGS 预备**：每个高斯由中心 μ、协方差 Σ（由缩放 S 与旋转 R 构成）、不透明度 o、颜色 c 定义；经投影与 α-blending 渲染像素颜色。

- **静态/动态高斯分离**：
  - 用 BootsTAPIR 逐像素跟踪运动，得到每帧 2D 动态掩码 MD；
  - 将"2D 投影中心落入动态掩码范围内 **且** 运动距离处于**前 1.5%**"的高斯判为动态高斯 GD，其余为静态高斯 GS；
  - 将输入序列划分为 N 个子集，逐子集渐进重建，最后按时间顺序拼接成完整 4D 场景。

- **静态高斯运动模型**：假设子集时间极短、运动为线性，位置建模为 μS(ti) = μS(ts) + (ti/τd)·d，其余参数同 3DGS。

- **动态高斯运动模型**（非线性，涉及相机与物体运动）：
  - **位置**：使用 Catmull-Rom 样条，以子集起止点 (μs, μe) 为端点、相邻点 (μ−1, μ+1) 为控制点插值；
  - **旋转**：用 Slerp（四元数球面线性插值）建模 RD(ti)；
  - **不透明度**：采用**双高斯衰减模型** oD(x, ti) = σ(ti)·o·G(x)，σ 由两个高斯原语的时间 μ0、μ1 及中间时刻 td 控制，刻画物体出现/消失的持续性。

- **运动感知去模糊网络**：
  - **静态高斯去模糊**：MLP FS 预测 N 张虚拟清晰图对应的旋转 ΔR 与平移 ΔT，得到 μS(ti) = μS(t)·ΔRi + ΔTi；
  - **动态高斯去模糊**：轻量 MLP FD，包含正弦嵌入器、三个分支编码器（位置/尺度/几何状态）与残差主干，逐高斯预测位移 ΔμD、各向异性尺度 ΔS、旋转 ΔRD，并组合得到 RD(ti) 与 S(ti)。

- **虚拟图像合成**：将同一采样时刻的静态与动态高斯合并渲染成虚拟清晰图像 I(ti)，再按曝光时间内 N 张的平均合成虚拟模糊图 B̂(t)。

- **优化策略（两阶段协同）**：
  - 先用 NAFNet 去模糊结果 Bd 监督训练 4D 高斯（L′render = Σ|Bd(ti) − I(ti)|₁），得到高质量初始模型；
  - 再引入真实模糊图 B 进行协同约束：**Lrender = λ·L′render + (1−λ)·Σ|B(t) − B̂(t)|₁**，其中 λ 为平衡超参；
  - 该设计既防止对先验清晰图过拟合，又同时对齐真实模糊观测。

## 3. 实验设计

- **数据集 / 场景**：
  - **Stereo Blur 数据集**：6 个严重运动模糊场景，每场景 48 张图，原始分辨率 1280×720，由 ZED 双目相机采集（使用左视图按通用协议合成模糊帧）；
  - **真实世界模糊数据集（BARD-GS 提出）**：7 个场景，分辨率 960×540，用两台曝光时间不同的 GoPro 相机采集（1/24 s 模糊、1/240 s 清晰）。
- **Benchmark / 评价指标**：去模糊与 4D 重建用 PSNR↑、SSIM↑、LPIPS↓；同时测量渲染帧率 FPS 与训练时长。
- **对比方法**：
  - 静态去模糊重建：Deblurring-3DGS、BAD-GS；
  - 动态重建：4D Gaussians、E-D3DGS、SoM、SplineGS；
  - 动态重建 + 去模糊网络：E-D3DGS+NAFNet、SoM+NAFNet；
  - 动态去模糊重建：DyBluRF、BARD-GS、Deblur4DGS；
  - 另设 NAFNet 作为下界、清晰图输入作为上界（MSCD-GS*）。

## 4. 资源与算力

- 论文明确说明实验在**单张 NVIDIA A100 40GB GPU** 上进行。
- 训练时长在表格中给出（如 MSCD-GS 为 0.72 h，明显低于 Deblur4DGS 的 6.10 h、BARD-GS 的 4.62 h 等）。
- 计算在华中科技大学 HPC 平台完成。
- **未明确说明**：具体 GPU 数量、总训练轮数、总能耗等细节；仅从表格可推断单卡设置与各方法的相对训练时长。

## 5. 实验数量与充分性

- **主实验**：在 2 个真实数据集上分别评估去模糊 4D 重建（表 2）与新视角合成（表 3），与约 11 个基线方法对比。
- **消融实验**：
  - 模块消融（表 4）：去模糊网络 DN、静态高斯去模糊 SGD、动态高斯去模糊 DGD 的 7 种组合；
  - 虚拟视角数量消融（表 5）：N = 2、3、4、6、10 共 5 种设置。
- **定性对比**：图 3（去模糊 4D 重建）、图 4（新视角合成）、图 5（模块消融定性）、图 6（局限性）。
- **充分性评价**：
  - **较充分**：覆盖两个数据集、去模糊与 NVS 两类任务、模块与超参两组消融，并同时报告精度、速度、训练时间，对比维度全面。
  - **客观/公平性**：由于现有 4D 方法无法直接处理模糊图，作者统一用预训练 NAFNet 辅助各基线重建，提供了相对公平的比较；同时设置下界（NAFNet）与上界（清晰图输入）以界定性能区间。
  - **可改进处**：消融实验仅在 Stereo Blur 的单个场景（Man）上进行，代表性有限；数据集规模较小（6 与 7 个场景）。

## 6. 主要结论与发现

- MSCD-GS 能有效从运动模糊输入重建高质量动态场景，去模糊与新视角合成**均达到 SOTA**：
  - Stereo Blur 去模糊：PSNR 33.21、SSIM 0.957、LPIPS 0.043；NVS：PSNR 29.49；
  - 真实世界数据集 NVS：PSNR 28.13。
- 在同类动态去模糊重建方法中，MSCD-GS **渲染帧率最高（121 FPS）、训练时间最短（0.72 h）**。
- 协同正则约束（λ 平衡去模糊先验与运动合成模糊）能避免过拟合到先验清晰图，显著提升重建质量。
- 结论：MSCD-GS 拓展了 4D 高斯泼溅在真实模糊动态场景中的适用性，且**对先验数据依赖更少、更实用**。

## 7. 优点

- **运动分离建模**：依据静态/动态高斯的运动特性差异分别建模（线性运动 vs. 样条+Slerp+双高斯衰减），更贴合物理成像机制。
- **轻量运动感知网络**：两个 MLP 分别预测静态刚性运动与动态逐高斯非刚性变形，兼顾表达力与效率。
- **协同去模糊约束**：巧妙结合去模糊模型输出与运动合成模糊图进行联合监督，既利用去模糊先验又防止过拟合，是本文的关键创新。
- **高效率与实用性**：不依赖深度、轨迹、光流等大量先验，训练时间与渲染帧率均优于同类方法。
- **实验对比完备**：同时报告精度、速度与训练成本，并给出性能下界/上界，对比公平性较好。

## 8. 不足与局限

- **无法重建"缺失内容"**：小而快的运动物体在曝光中可能出现重影甚至完全消失，由于 4D 重建依赖图像监督，这类缺失部分无法被恢复（图 6 中人物腿部消失）。作者提出未来可引入扩散模型生成缺失内容。
- **依赖去模糊网络的下限**：MSCD-GS 以预训练 NAFNet 为基础，去模糊网络的能力仍会影响重建性能上限（表 1 显示其构成下界）。
- **启发式分类阈值**：静态/动态高斯分类依赖"运动距离前 1.5%"等经验阈值，可能对场景敏感，论文未深入讨论阈值鲁棒性。
- **实验覆盖有限**：数据集仅两个、场景数量较少（6 与 7 个）；消融实验仅在单个场景上进行，泛化性验证略显不足。
- **超参与采样设置**：虚拟帧数 N=3、平衡系数 λ=0.4 等设置对结果的影响虽有消融，但最优性论证相对有限。

（完）
