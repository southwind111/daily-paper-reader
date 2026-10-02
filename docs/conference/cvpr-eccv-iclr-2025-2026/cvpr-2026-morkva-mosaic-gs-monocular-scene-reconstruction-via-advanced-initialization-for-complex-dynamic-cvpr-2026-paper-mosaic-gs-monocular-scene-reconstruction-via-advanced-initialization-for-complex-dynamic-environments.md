---
title: "MOSAIC-GS: Monocular Scene Reconstruction via Advanced Initialization for Complex Dynamic Environments"
title_zh: MOSAIC-GS：面向复杂动态环境的高级初始化单目场景重建
authors: "Morkva, Svitlana, Patil, Vaishakh, Tonioni, Alessio, Oechsle, Michael, Wilder-Smith, Maximum, Hutter, Marco"
date: 2026
publication_date: 2026
publication_date_precision: year
publication_date_source: conference year only; exact release date unverified
publication_date_kind: unknown
pdf: "https://openaccess.thecvf.com/content/CVPR2026/papers/Morkva_MOSAIC-GS_Monocular_Scene_Reconstruction_via_Advanced_Initialization_for_Complex_Dynamic_CVPR_2026_paper.pdf"
tags: ["query:dr"]
score: 9.0
evidence: 利用几何线索与刚性约束从单目视频重建动态场景
tldr: 单目视频下的动态场景重建因缺乏多视角约束而高度病态，准确恢复物体几何与时间一致性尤为困难。本文提出MOSAIC-GS，一种全显式且计算高效的高保真动态场景重建方法，利用深度、光流、动态物体分割与点跟踪等几何线索，结合刚性运动约束在初始化阶段估计初步三维场景动态。在光度优化前恢复场景动态降低了对约束的依赖，实现了复杂动态环境下的高效重建。
source: CVPR-2026-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-morkva-mosaic-gs-monocular-scene-reconstruction-via-advanced-initialization-for-complex-dynamic-cvpr-2026-paper/fig-001.webp\", \"caption\": \"\", \"page\": 1, \"index\": 1, \"width\": 360, \"height\": 480}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-morkva-mosaic-gs-monocular-scene-reconstruction-via-advanced-initialization-for-complex-dynamic-cvpr-2026-paper/fig-002.webp\", \"caption\": \"\", \"page\": 1, \"index\": 2, \"width\": 360, \"height\": 480}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-morkva-mosaic-gs-monocular-scene-reconstruction-via-advanced-initialization-for-complex-dynamic-cvpr-2026-paper/fig-003.webp\", \"caption\": \"\", \"page\": 1, \"index\": 3, \"width\": 360, \"height\": 480}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-morkva-mosaic-gs-monocular-scene-reconstruction-via-advanced-initialization-for-complex-dynamic-cvpr-2026-paper/fig-004.webp\", \"caption\": \"\", \"page\": 1, \"index\": 4, \"width\": 360, \"height\": 480}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-morkva-mosaic-gs-monocular-scene-reconstruction-via-advanced-initialization-for-complex-dynamic-cvpr-2026-paper/fig-005.webp\", \"caption\": \"\", \"page\": 1, \"index\": 5, \"width\": 360, \"height\": 480}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-morkva-mosaic-gs-monocular-scene-reconstruction-via-advanced-initialization-for-complex-dynamic-cvpr-2026-paper/fig-006.webp\", \"caption\": \"\", \"page\": 1, \"index\": 6, \"width\": 360, \"height\": 480}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-morkva-mosaic-gs-monocular-scene-reconstruction-via-advanced-initialization-for-complex-dynamic-cvpr-2026-paper/fig-007.webp\", \"caption\": \"\", \"page\": 1, \"index\": 7, \"width\": 360, \"height\": 480}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-morkva-mosaic-gs-monocular-scene-reconstruction-via-advanced-initialization-for-complex-dynamic-cvpr-2026-paper/fig-008.webp\", \"caption\": \"\", \"page\": 1, \"index\": 8, \"width\": 360, \"height\": 480}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-morkva-mosaic-gs-monocular-scene-reconstruction-via-advanced-initialization-for-complex-dynamic-cvpr-2026-paper/fig-009.webp\", \"caption\": \"\", \"page\": 1, \"index\": 9, \"width\": 360, \"height\": 480}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-morkva-mosaic-gs-monocular-scene-reconstruction-via-advanced-initialization-for-complex-dynamic-cvpr-2026-paper/fig-010.webp\", \"caption\": \"\", \"page\": 1, \"index\": 10, \"width\": 360, \"height\": 480}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-morkva-mosaic-gs-monocular-scene-reconstruction-via-advanced-initialization-for-complex-dynamic-cvpr-2026-paper/fig-011.webp\", \"caption\": \"\", \"page\": 1, \"index\": 11, \"width\": 360, \"height\": 480}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-morkva-mosaic-gs-monocular-scene-reconstruction-via-advanced-initialization-for-complex-dynamic-cvpr-2026-paper/fig-012.webp\", \"caption\": \"\", \"page\": 1, \"index\": 12, \"width\": 360, \"height\": 480}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-morkva-mosaic-gs-monocular-scene-reconstruction-via-advanced-initialization-for-complex-dynamic-cvpr-2026-paper/fig-013.webp\", \"caption\": \"\", \"page\": 4, \"index\": 13, \"width\": 480, \"height\": 270}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-morkva-mosaic-gs-monocular-scene-reconstruction-via-advanced-initialization-for-complex-dynamic-cvpr-2026-paper/fig-014.webp\", \"caption\": \"\", \"page\": 4, \"index\": 14, \"width\": 480, \"height\": 270}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-morkva-mosaic-gs-monocular-scene-reconstruction-via-advanced-initialization-for-complex-dynamic-cvpr-2026-paper/fig-015.webp\", \"caption\": \"\", \"page\": 4, \"index\": 15, \"width\": 480, \"height\": 270}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-morkva-mosaic-gs-monocular-scene-reconstruction-via-advanced-initialization-for-complex-dynamic-cvpr-2026-paper/fig-016.webp\", \"caption\": \"\", \"page\": 4, \"index\": 16, \"width\": 480, \"height\": 270}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-morkva-mosaic-gs-monocular-scene-reconstruction-via-advanced-initialization-for-complex-dynamic-cvpr-2026-paper/fig-017.webp\", \"caption\": \"\", \"page\": 4, \"index\": 17, \"width\": 480, \"height\": 270}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-morkva-mosaic-gs-monocular-scene-reconstruction-via-advanced-initialization-for-complex-dynamic-cvpr-2026-paper/fig-018.webp\", \"caption\": \"\", \"page\": 4, \"index\": 18, \"width\": 480, \"height\": 270}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-morkva-mosaic-gs-monocular-scene-reconstruction-via-advanced-initialization-for-complex-dynamic-cvpr-2026-paper/fig-019.webp\", \"caption\": \"\", \"page\": 4, \"index\": 19, \"width\": 480, \"height\": 270}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-morkva-mosaic-gs-monocular-scene-reconstruction-via-advanced-initialization-for-complex-dynamic-cvpr-2026-paper/fig-020.webp\", \"caption\": \"\", \"page\": 4, \"index\": 20, \"width\": 480, \"height\": 270}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-morkva-mosaic-gs-monocular-scene-reconstruction-via-advanced-initialization-for-complex-dynamic-cvpr-2026-paper/fig-021.webp\", \"caption\": \"\", \"page\": 4, \"index\": 21, \"width\": 480, \"height\": 270}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-morkva-mosaic-gs-monocular-scene-reconstruction-via-advanced-initialization-for-complex-dynamic-cvpr-2026-paper/fig-022.webp\", \"caption\": \"\", \"page\": 4, \"index\": 22, \"width\": 480, \"height\": 270}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-morkva-mosaic-gs-monocular-scene-reconstruction-via-advanced-initialization-for-complex-dynamic-cvpr-2026-paper/fig-023.webp\", \"caption\": \"\", \"page\": 4, \"index\": 23, \"width\": 480, \"height\": 270}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-morkva-mosaic-gs-monocular-scene-reconstruction-via-advanced-initialization-for-complex-dynamic-cvpr-2026-paper/fig-024.webp\", \"caption\": \"\", \"page\": 4, \"index\": 24, \"width\": 480, \"height\": 270}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-morkva-mosaic-gs-monocular-scene-reconstruction-via-advanced-initialization-for-complex-dynamic-cvpr-2026-paper/fig-025.webp\", \"caption\": \"\", \"page\": 4, \"index\": 25, \"width\": 480, \"height\": 270}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-morkva-mosaic-gs-monocular-scene-reconstruction-via-advanced-initialization-for-complex-dynamic-cvpr-2026-paper/fig-026.webp\", \"caption\": \"\", \"page\": 4, \"index\": 26, \"width\": 480, \"height\": 270}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-morkva-mosaic-gs-monocular-scene-reconstruction-via-advanced-initialization-for-complex-dynamic-cvpr-2026-paper/fig-027.webp\", \"caption\": \"\", \"page\": 4, \"index\": 27, \"width\": 480, \"height\": 270}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-morkva-mosaic-gs-monocular-scene-reconstruction-via-advanced-initialization-for-complex-dynamic-cvpr-2026-paper/fig-028.webp\", \"caption\": \"\", \"page\": 4, \"index\": 28, \"width\": 480, \"height\": 270}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-morkva-mosaic-gs-monocular-scene-reconstruction-via-advanced-initialization-for-complex-dynamic-cvpr-2026-paper/fig-029.webp\", \"caption\": \"\", \"page\": 4, \"index\": 29, \"width\": 480, \"height\": 270}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-morkva-mosaic-gs-monocular-scene-reconstruction-via-advanced-initialization-for-complex-dynamic-cvpr-2026-paper/fig-030.webp\", \"caption\": \"\", \"page\": 7, \"index\": 30, \"width\": 360, \"height\": 480}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-morkva-mosaic-gs-monocular-scene-reconstruction-via-advanced-initialization-for-complex-dynamic-cvpr-2026-paper/fig-031.webp\", \"caption\": \"\", \"page\": 7, \"index\": 31, \"width\": 360, \"height\": 480}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-morkva-mosaic-gs-monocular-scene-reconstruction-via-advanced-initialization-for-complex-dynamic-cvpr-2026-paper/fig-032.webp\", \"caption\": \"\", \"page\": 7, \"index\": 32, \"width\": 360, \"height\": 480}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-morkva-mosaic-gs-monocular-scene-reconstruction-via-advanced-initialization-for-complex-dynamic-cvpr-2026-paper/fig-033.webp\", \"caption\": \"\", \"page\": 7, \"index\": 33, \"width\": 360, \"height\": 480}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-morkva-mosaic-gs-monocular-scene-reconstruction-via-advanced-initialization-for-complex-dynamic-cvpr-2026-paper/fig-034.webp\", \"caption\": \"\", \"page\": 7, \"index\": 34, \"width\": 297, \"height\": 423}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-morkva-mosaic-gs-monocular-scene-reconstruction-via-advanced-initialization-for-complex-dynamic-cvpr-2026-paper/fig-035.webp\", \"caption\": \"\", \"page\": 7, \"index\": 35, \"width\": 360, \"height\": 480}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-morkva-mosaic-gs-monocular-scene-reconstruction-via-advanced-initialization-for-complex-dynamic-cvpr-2026-paper/fig-036.webp\", \"caption\": \"\", \"page\": 7, \"index\": 36, \"width\": 360, \"height\": 480}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-morkva-mosaic-gs-monocular-scene-reconstruction-via-advanced-initialization-for-complex-dynamic-cvpr-2026-paper/fig-037.webp\", \"caption\": \"\", \"page\": 7, \"index\": 37, \"width\": 360, \"height\": 480}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-morkva-mosaic-gs-monocular-scene-reconstruction-via-advanced-initialization-for-complex-dynamic-cvpr-2026-paper/fig-038.webp\", \"caption\": \"\", \"page\": 7, \"index\": 38, \"width\": 360, \"height\": 480}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-morkva-mosaic-gs-monocular-scene-reconstruction-via-advanced-initialization-for-complex-dynamic-cvpr-2026-paper/fig-039.webp\", \"caption\": \"\", \"page\": 7, \"index\": 39, \"width\": 407, \"height\": 367}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-morkva-mosaic-gs-monocular-scene-reconstruction-via-advanced-initialization-for-complex-dynamic-cvpr-2026-paper/fig-040.webp\", \"caption\": \"\", \"page\": 7, \"index\": 40, \"width\": 467, \"height\": 297}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-morkva-mosaic-gs-monocular-scene-reconstruction-via-advanced-initialization-for-complex-dynamic-cvpr-2026-paper/fig-041.webp\", \"caption\": \"\", \"page\": 7, \"index\": 41, \"width\": 463, \"height\": 297}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-morkva-mosaic-gs-monocular-scene-reconstruction-via-advanced-initialization-for-complex-dynamic-cvpr-2026-paper/fig-042.webp\", \"caption\": \"\", \"page\": 7, \"index\": 42, \"width\": 465, \"height\": 297}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-morkva-mosaic-gs-monocular-scene-reconstruction-via-advanced-initialization-for-complex-dynamic-cvpr-2026-paper/fig-043.webp\", \"caption\": \"\", \"page\": 7, \"index\": 43, \"width\": 360, \"height\": 480}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-morkva-mosaic-gs-monocular-scene-reconstruction-via-advanced-initialization-for-complex-dynamic-cvpr-2026-paper/fig-044.webp\", \"caption\": \"\", \"page\": 7, \"index\": 44, \"width\": 407, \"height\": 362}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-morkva-mosaic-gs-monocular-scene-reconstruction-via-advanced-initialization-for-complex-dynamic-cvpr-2026-paper/fig-045.webp\", \"caption\": \"\", \"page\": 7, \"index\": 45, \"width\": 360, \"height\": 480}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-morkva-mosaic-gs-monocular-scene-reconstruction-via-advanced-initialization-for-complex-dynamic-cvpr-2026-paper/fig-046.webp\", \"caption\": \"\", \"page\": 7, \"index\": 46, \"width\": 407, \"height\": 358}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-morkva-mosaic-gs-monocular-scene-reconstruction-via-advanced-initialization-for-complex-dynamic-cvpr-2026-paper/fig-047.webp\", \"caption\": \"\", \"page\": 7, \"index\": 47, \"width\": 360, \"height\": 480}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-morkva-mosaic-gs-monocular-scene-reconstruction-via-advanced-initialization-for-complex-dynamic-cvpr-2026-paper/fig-048.webp\", \"caption\": \"\", \"page\": 7, \"index\": 48, \"width\": 360, \"height\": 480}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-morkva-mosaic-gs-monocular-scene-reconstruction-via-advanced-initialization-for-complex-dynamic-cvpr-2026-paper/fig-049.webp\", \"caption\": \"\", \"page\": 7, \"index\": 49, \"width\": 480, \"height\": 270}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-morkva-mosaic-gs-monocular-scene-reconstruction-via-advanced-initialization-for-complex-dynamic-cvpr-2026-paper/fig-050.webp\", \"caption\": \"\", \"page\": 7, \"index\": 50, \"width\": 480, \"height\": 270}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-morkva-mosaic-gs-monocular-scene-reconstruction-via-advanced-initialization-for-complex-dynamic-cvpr-2026-paper/fig-051.webp\", \"caption\": \"\", \"page\": 7, \"index\": 51, \"width\": 480, \"height\": 270}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-morkva-mosaic-gs-monocular-scene-reconstruction-via-advanced-initialization-for-complex-dynamic-cvpr-2026-paper/fig-052.webp\", \"caption\": \"\", \"page\": 7, \"index\": 52, \"width\": 480, \"height\": 270}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-morkva-mosaic-gs-monocular-scene-reconstruction-via-advanced-initialization-for-complex-dynamic-cvpr-2026-paper/fig-053.webp\", \"caption\": \"\", \"page\": 7, \"index\": 53, \"width\": 480, \"height\": 270}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-morkva-mosaic-gs-monocular-scene-reconstruction-via-advanced-initialization-for-complex-dynamic-cvpr-2026-paper/fig-054.webp\", \"caption\": \"\", \"page\": 7, \"index\": 54, \"width\": 480, \"height\": 270}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-morkva-mosaic-gs-monocular-scene-reconstruction-via-advanced-initialization-for-complex-dynamic-cvpr-2026-paper/fig-055.webp\", \"caption\": \"\", \"page\": 7, \"index\": 55, \"width\": 480, \"height\": 270}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-morkva-mosaic-gs-monocular-scene-reconstruction-via-advanced-initialization-for-complex-dynamic-cvpr-2026-paper/fig-056.webp\", \"caption\": \"\", \"page\": 7, \"index\": 56, \"width\": 480, \"height\": 270}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-morkva-mosaic-gs-monocular-scene-reconstruction-via-advanced-initialization-for-complex-dynamic-cvpr-2026-paper/fig-057.webp\", \"caption\": \"\", \"page\": 7, \"index\": 57, \"width\": 480, \"height\": 270}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-morkva-mosaic-gs-monocular-scene-reconstruction-via-advanced-initialization-for-complex-dynamic-cvpr-2026-paper/fig-058.webp\", \"caption\": \"\", \"page\": 7, \"index\": 58, \"width\": 480, \"height\": 270}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-morkva-mosaic-gs-monocular-scene-reconstruction-via-advanced-initialization-for-complex-dynamic-cvpr-2026-paper/fig-059.webp\", \"caption\": \"\", \"page\": 7, \"index\": 59, \"width\": 480, \"height\": 270}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-morkva-mosaic-gs-monocular-scene-reconstruction-via-advanced-initialization-for-complex-dynamic-cvpr-2026-paper/fig-060.webp\", \"caption\": \"\", \"page\": 7, \"index\": 60, \"width\": 480, \"height\": 270}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-morkva-mosaic-gs-monocular-scene-reconstruction-via-advanced-initialization-for-complex-dynamic-cvpr-2026-paper/fig-061.webp\", \"caption\": \"\", \"page\": 8, \"index\": 61, \"width\": 360, \"height\": 480}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-morkva-mosaic-gs-monocular-scene-reconstruction-via-advanced-initialization-for-complex-dynamic-cvpr-2026-paper/fig-062.webp\", \"caption\": \"\", \"page\": 8, \"index\": 62, \"width\": 360, \"height\": 480}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-morkva-mosaic-gs-monocular-scene-reconstruction-via-advanced-initialization-for-complex-dynamic-cvpr-2026-paper/fig-063.webp\", \"caption\": \"\", \"page\": 8, \"index\": 63, \"width\": 360, \"height\": 480}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-morkva-mosaic-gs-monocular-scene-reconstruction-via-advanced-initialization-for-complex-dynamic-cvpr-2026-paper/fig-064.webp\", \"caption\": \"\", \"page\": 8, \"index\": 64, \"width\": 2408, \"height\": 1224}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-morkva-mosaic-gs-monocular-scene-reconstruction-via-advanced-initialization-for-complex-dynamic-cvpr-2026-paper/fig-065.webp\", \"caption\": \"\", \"page\": 8, \"index\": 65, \"width\": 2408, \"height\": 1224}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-morkva-mosaic-gs-monocular-scene-reconstruction-via-advanced-initialization-for-complex-dynamic-cvpr-2026-paper/fig-066.webp\", \"caption\": \"\", \"page\": 8, \"index\": 66, \"width\": 2408, \"height\": 1224}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-morkva-mosaic-gs-monocular-scene-reconstruction-via-advanced-initialization-for-complex-dynamic-cvpr-2026-paper/fig-067.webp\", \"caption\": \"\", \"page\": 8, \"index\": 67, \"width\": 2408, \"height\": 1224}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-morkva-mosaic-gs-monocular-scene-reconstruction-via-advanced-initialization-for-complex-dynamic-cvpr-2026-paper/fig-068.webp\", \"caption\": \"\", \"page\": 8, \"index\": 68, \"width\": 2408, \"height\": 1224}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-morkva-mosaic-gs-monocular-scene-reconstruction-via-advanced-initialization-for-complex-dynamic-cvpr-2026-paper/fig-069.webp\", \"caption\": \"\", \"page\": 8, \"index\": 69, \"width\": 2408, \"height\": 1224}]"
motivation: 单目动态场景重建因缺乏多视角约束而高度病态，几何与时间一致性难以保证。
method: 提出全显式高斯泼溅方法MOSAIC-GS，融合深度、光流、分割与点跟踪线索并施加刚性运动约束。
result: 在光度优化前先估计场景动态，实现复杂动态环境的高保真高效重建。
conclusion: 表明多几何线索初始化可显著缓解单目动态重建的病态性。
---

## Abstract
We present MOSAIC-GS, a novel, fully explicit, and computationally efficient approach for high-fidelity dynamic scene reconstruction from monocular videos using Gaussian Splatting.Monocular reconstruction is inherently ill-posed due to the lack of sufficient multiview constraints, making accurate recovery of object geometry and temporal coherence particularly challenging. To address this, we leverage multiple geometric cues, such as depth, optical flow, dynamic object segmentation, and point tracking. Combined with rigidity-based motion constraints, these cues allow us to estimate preliminary 3D scene dynamics during an initialization stage.Recovering scene dynamics prior to the photometric optimization reduces reliance on motion inference from visual appearance alone, which is often ambiguous in monocular settings.To enable compact representations, fast training, and real-time rendering while supporting non-rigid deformations, the scene is decomposed into static and dynamic components. Each Gaussian in the dynamic part of the scene is assigned a trajectory represented as time-dependent Poly-Fourier curve for parameter-efficient motion encoding.We demonstrate that MOSAIC-GS achieves substantially faster optimization and rendering compared to existing methods,while maintaining reconstruction quality on par with state-of-the-art approaches across standard monocular dynamic scene benchmarks.

---

## 论文详细总结（自动生成）

# MOSAIC-GS 论文详细总结

## 1. 核心问题与整体含义（研究动机与背景）

- **研究背景**：NeRF 与 3D Gaussian Splatting（3DGS）在静态场景重建上已实现高保真、照片级渲染，但二者本质上局限于静态场景，难以适用于机器人、自动驾驶、数字孪生、VR/AR 等动态环境。
- **核心问题**：从**单目视频**中重建动态三维场景是高度病态（ill-posed）的问题——缺乏足够的多视角约束，导致物体几何与时间一致性难以准确恢复；同时相机视野受限（机器人/嵌入式设备常见窄视角或立体视角），进一步加剧困难。
- **现有方法的痛点**：
  - 训练时间长、显存与存储开销大、渲染慢；
  - 复杂运动区域易出现明显伪影；
  - 许多方法优先追求视觉真实感而牺牲物理一致性，在未见视角下产生畸变；
  - 主流的两类动态高斯方案——**逐帧形变建模**（内存密集、难以扩展到长序列）与**连续运动建模**（紧凑但对快速/复杂运动捕捉不足）——各有局限。
- **论文的核心洞察**：在光度优化过程中**纯粹依赖视觉外观推断场景动态既低效也不可靠**；高质量的初始化（几何+物理先验）对重建保真度与收敛速度有决定性影响。因此作者主张：**在光度优化之前先恢复场景动态**。
- **整体含义**：MOSAIC-GS 是一个**全显式、计算高效**的单目动态场景重建框架，目标是在保持与 SOTA 相当的重建质量的同时，大幅降低训练与渲染成本，并附带实现动态场景分割与编辑等零成本下游应用。

## 2. 方法论

### 2.1 核心思想
- 输入为单目视频，配合相机内参 K、外参 [R|t]ₜ、逐帧深度图 Dₜ（来自传感器或单目深度估计模型如 Depth Anything）。
- 将场景**解耦为静态分量 G_s 与动态分量 G_d**，动态高斯用**时间相关的 Poly-Fourier 曲线**编码轨迹，实现参数高效的紧凑运动表示。
- 关键创新在于**四阶段高级预处理管线**，为光度优化提供包含运动信息的丰富初始化（而非常规方法仅初始化高斯位置与颜色）。

### 2.2 关键技术细节

**（1）动态区域检测**
- 用 RAFT 计算相邻帧的稠密光流，结合已知内外参构造基础矩阵 F，计算 **Sampson 极线误差** e_epi(x)：
  - 分子为 (x'ᵀFx)²，分母为 (Fx)₁²+(Fx)₂²+(Fᵀx')₁²+(Fᵀx')₂²；
  - 误差超过阈值 τ_epi 的像素被视为无法由相机运动解释，即动态区域。
- 选择 Sampson 误差而非完整 3D 重投影误差，是因为后者对噪声深度图敏感、不可靠。

**（2）动态实例的分割与跟踪**
- 使用提示式分割与跟踪模型 **SAM2**：先由上一步检测结果提取动态区域边界框作为提示；若已有已跟踪实例，则先减去其掩码以避免重复跟踪。
- 低置信度掩码（p_conf < τ_mask）被过滤；高置信度掩码加入跟踪器并按固定间隔前向传播，降低重复跟踪开销。
- 处理完全部帧后，再执行**反向传播（backtracking）**，把物体掩码扩展到其早期仍处于静止状态的帧。

**（3）场景流估计与刚性约束精化**
- 沿用点跟踪思路（BootsTAPIR / CoTracker），在动态区域内随机采样 **N_p = 10,000** 个查询点，跨全部 T 帧跟踪，得到轨迹 {p_iᵗ}。
- 依据与分割掩码 M_jᵗ 的多数重叠，把轨迹分配给动态物体 j，得到逐物体 3D 点集 {P^j}；主要属于静态背景的轨迹被丢弃（分割+跟踪的结合可缓解遮挡与掩码不完美带来的歧义）。
- 用深度图、内参、外参将 2D 轨迹**提升为 3D 场景流**。
- 对每个动态物体，用 **Kabsch 算法 + RANSAC** 估计最优刚体变换 (R_jᵗ, t_jᵗ)，精化位置：P_i^{t+1} := R_jᵗ P_iᵗ + t_jᵗ，并更新可见性；先前向再反向处理，对不可见点用最近的前后可见帧插值填补。

**（4）静态与动态区域的初始化**
- 用 **Poly-Fourier 曲线**（基函数 φ(t) = [1, t, t², sin(ωt), cos(ωt)]ᵀ）对每条轨迹求解线性方程组 **Ax = y**，解出系数 x（多项式系数 a₀,a₁,a₂,… 与傅里叶系数 b₁,c₁,…）。
- **与先前工作的关键差异**：Poly-Fourier 系数不是在光度优化中学习，而是**直接由精化后的场景流求解得到**，作为动态高斯形变参数的初始化。
- 颜色从对应像素 RGB 帧提取；尺度通过 RGB 图的 **Laplacian of Gaussian (LoG) 范数**并结合深度图估计；静态区域采用 Meuleman 等人的采样策略，仅在时间上间隔的部分训练帧上采样，以兼顾覆盖度并避免平坦区域过采样。

**（5）光度优化**
- 场景表示为 G = G_s ∪ G_d。静态高斯参数为均值 μ、旋转四元数 q、尺度 s、不透明度 α、球谐颜色系数 c。
- 动态高斯额外存储时间相关形变参数，位置偏移：
  - Δμ(t) = Σ_{k=1}^{d_p} a_k t^k + Σ_{k=1}^{d_F} [b_k cos(kωt) + c_k sin(kωt)]，μ(t) = μ₀ + Δμ(t)。
- **旋转建模的改进**：不像 Gaussian Flow 那样直接把时变偏移加到基础四元数上，而是把 Poly-Fourier 输出加单位四元数后归一化为单位四元数 Δq(t)，最终旋转 q(t) = Δq(t) ⊗ q₀（四元数乘法）。该设计保证旋转参数化一致，避免非法四元数更新带来的伪影。
- **不建模时变颜色形变**，以提升紧凑性并防止模型用"人工颜色变化"来补偿运动估计误差。
- 损失函数：L = (1−λ_ssim)L_L1 + λ_ssim L_SSIM + λ_depth L_depth；其中深度损失用 **Pearson 相关损失**实现，以应对时序深度尺度不一致，保持相对几何并具有尺度不变性。

## 3. 实验设计

### 3.1 数据集 / 场景
- **iPhone DyCheck**：7 个随意拍摄的动态场景，每场景最多 500 帧，含 RGB、相机内外参、噪声 LiDAR 深度、真值共可见性掩码，以及 1–2 个静态相机用于新视角评测。
- **NVIDIA Dynamic Scene（原始版，Yoon 等）**：7 个动态序列、12 个静态相机；通过从连续相机各取一帧模拟单目输入，得到 12 个时空稀疏帧，以第一相机图像作为参考视角。
- **NVIDIA Dynamic Scene（Gaussian Marbles 变体）**：7 个场景、每场景 100–200 帧、4 个静态相机，一台作单目输入、其余作评测视角。
- 论文特别指出：先前工作（如 MoSca）常忽视两个 NVIDIA 版本的差异，导致比较不一致；本文在两版上分别报告结果。

### 3.2 Benchmark 与评价指标
- 指标：**PSNR ↑** 与 **LPIPS ↓**（论文强调 LPIPS 更贴合视觉质量）。

### 3.3 对比方法
- **Dynamic Gaussians（Dyn. Gaussians）**、**4D Gaussians**、**Gaussian Marbles**、**Gaussian Flow**、**Shape of Motion**、**MoSca**（当前 SOTA）；
- NVIDIA 原始数据集上还对比了 **Casual-FVS、MonoNeRF、CTNeRF、RoDynRF**；
- Marbles 变体上对比 **Gaussian Flow** 与 **Gaussian Marbles**。
- 公平性处理：MOSAIC-GS 不含相机位姿精化阶段，为公平比较采用 MoSca 提取的精化位姿；在 Marbles 变体上，由于原数据集无可靠共可见性掩码，作者由深度图和相机参数解析生成掩码，并将所有先前方法在该协议下**重新评测**。

### 3.4 消融实验
在 DyCheck 上考察 5 个因素：(1) 动态高斯均值形变系数初始化；(2) 刚体变换场景流精化；(3) 静/动场景解耦；(4) 傅里叶编码阶数（32 默认、24、16）；(5) 深度监督。

## 4. 资源与算力

- **GPU 型号与数量**：文中明确说明所有方法（包括本文）在**单张 NVIDIA RTX 4090 GPU** 上基准测试。
- **训练时长（DyCheck 平均）**：
  - 本文 MOSAIC-GS：**10.5 分钟**（含预处理），其中光度优化约 **5 分钟**；
  - Gaussian Flow：23 分钟；MoSca：50 分钟；Gaussian Marbles：5–9 小时。
- **渲染速度**：本文 **180 FPS**；Gaussian Marbles ~200 FPS；Gaussian Flow 52 FPS；MoSca 38 FPS。
- **NVIDIA Marbles 变体**：本文 7 分钟，Gaussian Flow 18 分钟，Gaussian Marbles 3.5–8 小时。
- **未明确说明的部分**：论文未报告显存占用、预处理阶段与光度优化阶段的详细拆分耗时、总 GPU 小时数或碳排放等信息，也未说明除基准测试外的其他算力配置。

## 5. 实验数量与充分性

- **实验规模**：
  - **3 个数据集/版本**（DyCheck、NVIDIA 原始、NVIDIA Marbles 变体）上的定量评测；
  - **7 个对比方法**（DyCheck 表格中含 6 个基线 + 本文共 7 行）；
  - **1 组包含 8 行配置的消融实验**（完整模型 + 7 种变体）；
  - 多组定性对比（DyCheck 与 NVIDIA 原始数据集）；
  - 附加应用展示（场景分割、物体移除、颜色/运动编辑，见图 7）。
- **充分性评价**：
  - 覆盖了主流单目动态重建基准，且对 NVIDIA 数据集的两个版本做了区分，这在同类工作中较为严谨；
  - 消融实验覆盖了方法的所有关键组件，且报告了质量与时间两个维度，信息量较足。
- **客观与公平性**：
  - 优点：主动指出并纠正先前工作的比较偏差（两个 NVIDIA 版本混淆）；在 Marbles 变体上**重新评测所有基线**并统一采用共可见性掩码评测；采用 MoSca 的精化位姿以消除位姿优化的不公平优势。
  - 潜在问题：**未做多随机种子的重复实验或方差报告**；LPIPS 上胜出但 PSNR 落后于 MoSca，作者以"感知质量优于像素保真"作解释，这一解释虽有定性图支持，但缺乏主观用户研究佐证；依赖外部模型（RAFT、SAM2、BootsTAPIR、深度模型）的输出，可能引入与基线不同的先验强度差异。

## 6. 主要结论与发现

- **质量**：
  - DyCheck 平均 **PSNR 18.4 / LPIPS 0.255**，PSNR 仅次于 MoSca（19.32），但 **LPIPS 取得该数据集新的 SOTA**（优于 MoSca 的 0.264）；
  - NVIDIA 原始数据集：**PSNR 26.26（第二，仅次于 MoSca 26.72）/ LPIPS 0.060（最佳）**；
  - NVIDIA Marbles 变体（共可见性协议）：**PSNR 23.79 / LPIPS 0.069，全面 SOTA**，训练时间仅为 Gaussian Marbles 的极小部分。
- **效率**：训练时间约为 MoSca 的 1/5、Gaussian Flow 的 1/2，渲染速度约为 MoSca 的 4.7 倍。
- **消融结论**：
  - **场景解耦贡献最大**：去除后 mPSNR 从 18.40 骤降到 14.65，mLPIPS 从 0.255 恶化到 0.456，且光度优化时间从 5.06 分钟升至 8.26 分钟（所有高斯都要存形变参数）；
  - **形变初始化**次之关键：去除后 mPSNR 降至 16.99；
  - 场景流精化（18.11）与深度监督（18.13）均有正向增益；
  - 傅里叶阶数影响相对较小（24 阶 18.37、16 阶 18.29），高阶更能刻画 Wheel 等快速运动场景的细节，但 >32 阶会牺牲紧凑性。
- **附加发现**：预处理阶段的掩码 ID 时域精化可避免简单 3D 重投影造成的身份跳变，使**时序一致的分割与编辑成为重建的"副产品"，无需额外计算开销**。

## 7. 优点（亮点）

- **方法论层面**：
  - 提出"**先初始化动态、再做光度优化**"的范式转变，将病态的单目运动推断问题转化为由多源几何/物理线索驱动的初始化问题，思路清晰且动机充分；
  - 多线索融合（光流 + Sampson 极线误差 + SAM2 分割跟踪 + 点跟踪 + 深度）形成鲁棒且完整的动态实例识别与跟踪管线，并加入**反向传播
