---
title: "Mesh4D: 4D Mesh Reconstruction and Tracking from Monocular Video"
title_zh: Mesh4D：单目视频的4D网格重建与跟踪
authors: "Jiang, Zeren, Zheng, Chuanxia, Laina, Iro, Larlus, Diane, Vedaldi, Andrea"
date: 2026
publication_date: 2026
publication_date_precision: year
publication_date_source: conference year only; exact release date unverified
publication_date_kind: unknown
pdf: "https://openaccess.thecvf.com/content/CVPR2026/papers/Jiang_Mesh4D_4D_Mesh_Reconstruction_and_Tracking_from_Monocular_Video_CVPR_2026_paper.pdf"
tags: ["query:dr"]
score: 10.0
evidence: 单目4D网格重建与动态运动跟踪
tldr: 针对单目视频中动态物体完整3D形状与运动重建困难、形变表示不稳定的问题，本文提出前馈模型Mesh4D。它用紧凑隐空间编码整段动画序列，训练时以骨架结构提供形变先验，推理时无需骨架，并结合时空注意力与隐扩散模型。实验表明该方法能稳定重建物体形状与运动，为单目4D网格重建与跟踪提供统一框架。
source: CVPR-2026-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiang-mesh4d-4d-mesh-reconstruction-and-tracking-from-monocular-video-cvpr-2026-paper/fig-001.webp\", \"caption\": \"\", \"page\": 1, \"index\": 1, \"width\": 3840, \"height\": 2304}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiang-mesh4d-4d-mesh-reconstruction-and-tracking-from-monocular-video-cvpr-2026-paper/fig-002.webp\", \"caption\": \"\", \"page\": 1, \"index\": 2, \"width\": 2560, \"height\": 1536}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiang-mesh4d-4d-mesh-reconstruction-and-tracking-from-monocular-video-cvpr-2026-paper/fig-003.webp\", \"caption\": \"\", \"page\": 1, \"index\": 3, \"width\": 512, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiang-mesh4d-4d-mesh-reconstruction-and-tracking-from-monocular-video-cvpr-2026-paper/fig-004.webp\", \"caption\": \"\", \"page\": 1, \"index\": 4, \"width\": 512, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiang-mesh4d-4d-mesh-reconstruction-and-tracking-from-monocular-video-cvpr-2026-paper/fig-005.webp\", \"caption\": \"\", \"page\": 1, \"index\": 5, \"width\": 512, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiang-mesh4d-4d-mesh-reconstruction-and-tracking-from-monocular-video-cvpr-2026-paper/fig-006.webp\", \"caption\": \"\", \"page\": 1, \"index\": 6, \"width\": 512, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiang-mesh4d-4d-mesh-reconstruction-and-tracking-from-monocular-video-cvpr-2026-paper/fig-007.webp\", \"caption\": \"\", \"page\": 1, \"index\": 7, \"width\": 512, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiang-mesh4d-4d-mesh-reconstruction-and-tracking-from-monocular-video-cvpr-2026-paper/fig-008.webp\", \"caption\": \"\", \"page\": 1, \"index\": 8, \"width\": 512, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiang-mesh4d-4d-mesh-reconstruction-and-tracking-from-monocular-video-cvpr-2026-paper/fig-009.webp\", \"caption\": \"\", \"page\": 1, \"index\": 9, \"width\": 512, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiang-mesh4d-4d-mesh-reconstruction-and-tracking-from-monocular-video-cvpr-2026-paper/fig-010.webp\", \"caption\": \"\", \"page\": 1, \"index\": 10, \"width\": 1092, \"height\": 369}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiang-mesh4d-4d-mesh-reconstruction-and-tracking-from-monocular-video-cvpr-2026-paper/fig-011.webp\", \"caption\": \"\", \"page\": 1, \"index\": 11, \"width\": 1092, \"height\": 369}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiang-mesh4d-4d-mesh-reconstruction-and-tracking-from-monocular-video-cvpr-2026-paper/fig-012.webp\", \"caption\": \"\", \"page\": 1, \"index\": 12, \"width\": 512, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiang-mesh4d-4d-mesh-reconstruction-and-tracking-from-monocular-video-cvpr-2026-paper/fig-013.webp\", \"caption\": \"\", \"page\": 1, \"index\": 13, \"width\": 512, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiang-mesh4d-4d-mesh-reconstruction-and-tracking-from-monocular-video-cvpr-2026-paper/fig-014.webp\", \"caption\": \"\", \"page\": 1, \"index\": 14, \"width\": 1092, \"height\": 369}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiang-mesh4d-4d-mesh-reconstruction-and-tracking-from-monocular-video-cvpr-2026-paper/fig-015.webp\", \"caption\": \"\", \"page\": 4, \"index\": 15, \"width\": 512, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiang-mesh4d-4d-mesh-reconstruction-and-tracking-from-monocular-video-cvpr-2026-paper/fig-016.webp\", \"caption\": \"\", \"page\": 4, \"index\": 16, \"width\": 512, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiang-mesh4d-4d-mesh-reconstruction-and-tracking-from-monocular-video-cvpr-2026-paper/fig-017.webp\", \"caption\": \"\", \"page\": 4, \"index\": 17, \"width\": 512, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiang-mesh4d-4d-mesh-reconstruction-and-tracking-from-monocular-video-cvpr-2026-paper/fig-018.webp\", \"caption\": \"\", \"page\": 4, \"index\": 18, \"width\": 512, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiang-mesh4d-4d-mesh-reconstruction-and-tracking-from-monocular-video-cvpr-2026-paper/fig-019.webp\", \"caption\": \"\", \"page\": 4, \"index\": 19, \"width\": 512, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiang-mesh4d-4d-mesh-reconstruction-and-tracking-from-monocular-video-cvpr-2026-paper/fig-020.webp\", \"caption\": \"\", \"page\": 4, \"index\": 20, \"width\": 512, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiang-mesh4d-4d-mesh-reconstruction-and-tracking-from-monocular-video-cvpr-2026-paper/fig-021.webp\", \"caption\": \"\", \"page\": 4, \"index\": 21, \"width\": 1222, \"height\": 954}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiang-mesh4d-4d-mesh-reconstruction-and-tracking-from-monocular-video-cvpr-2026-paper/fig-022.webp\", \"caption\": \"\", \"page\": 4, \"index\": 22, \"width\": 2444, \"height\": 1908}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiang-mesh4d-4d-mesh-reconstruction-and-tracking-from-monocular-video-cvpr-2026-paper/fig-023.webp\", \"caption\": \"\", \"page\": 4, \"index\": 23, \"width\": 1222, \"height\": 954}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiang-mesh4d-4d-mesh-reconstruction-and-tracking-from-monocular-video-cvpr-2026-paper/fig-024.webp\", \"caption\": \"\", \"page\": 4, \"index\": 24, \"width\": 1920, \"height\": 1080}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiang-mesh4d-4d-mesh-reconstruction-and-tracking-from-monocular-video-cvpr-2026-paper/fig-025.webp\", \"caption\": \"\", \"page\": 4, \"index\": 25, \"width\": 960, \"height\": 540}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiang-mesh4d-4d-mesh-reconstruction-and-tracking-from-monocular-video-cvpr-2026-paper/fig-026.webp\", \"caption\": \"\", \"page\": 4, \"index\": 26, \"width\": 960, \"height\": 540}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiang-mesh4d-4d-mesh-reconstruction-and-tracking-from-monocular-video-cvpr-2026-paper/fig-027.webp\", \"caption\": \"\", \"page\": 4, \"index\": 27, \"width\": 960, \"height\": 540}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiang-mesh4d-4d-mesh-reconstruction-and-tracking-from-monocular-video-cvpr-2026-paper/fig-028.webp\", \"caption\": \"\", \"page\": 4, \"index\": 28, \"width\": 1222, \"height\": 954}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiang-mesh4d-4d-mesh-reconstruction-and-tracking-from-monocular-video-cvpr-2026-paper/fig-029.webp\", \"caption\": \"\", \"page\": 4, \"index\": 29, \"width\": 1222, \"height\": 954}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiang-mesh4d-4d-mesh-reconstruction-and-tracking-from-monocular-video-cvpr-2026-paper/fig-030.webp\", \"caption\": \"\", \"page\": 6, \"index\": 30, \"width\": 1222, \"height\": 954}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiang-mesh4d-4d-mesh-reconstruction-and-tracking-from-monocular-video-cvpr-2026-paper/fig-031.webp\", \"caption\": \"\", \"page\": 7, \"index\": 31, \"width\": 1024, \"height\": 1024}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiang-mesh4d-4d-mesh-reconstruction-and-tracking-from-monocular-video-cvpr-2026-paper/fig-032.webp\", \"caption\": \"\", \"page\": 7, \"index\": 32, \"width\": 1024, \"height\": 1024}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiang-mesh4d-4d-mesh-reconstruction-and-tracking-from-monocular-video-cvpr-2026-paper/fig-033.webp\", \"caption\": \"\", \"page\": 7, \"index\": 33, \"width\": 1024, \"height\": 1024}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiang-mesh4d-4d-mesh-reconstruction-and-tracking-from-monocular-video-cvpr-2026-paper/fig-034.webp\", \"caption\": \"\", \"page\": 7, \"index\": 34, \"width\": 1024, \"height\": 1024}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiang-mesh4d-4d-mesh-reconstruction-and-tracking-from-monocular-video-cvpr-2026-paper/fig-035.webp\", \"caption\": \"\", \"page\": 7, \"index\": 35, \"width\": 1024, \"height\": 1024}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiang-mesh4d-4d-mesh-reconstruction-and-tracking-from-monocular-video-cvpr-2026-paper/fig-036.webp\", \"caption\": \"\", \"page\": 7, \"index\": 36, \"width\": 1024, \"height\": 1024}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiang-mesh4d-4d-mesh-reconstruction-and-tracking-from-monocular-video-cvpr-2026-paper/fig-037.webp\", \"caption\": \"\", \"page\": 7, \"index\": 37, \"width\": 1024, \"height\": 1024}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiang-mesh4d-4d-mesh-reconstruction-and-tracking-from-monocular-video-cvpr-2026-paper/fig-038.webp\", \"caption\": \"\", \"page\": 7, \"index\": 38, \"width\": 1024, \"height\": 1024}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiang-mesh4d-4d-mesh-reconstruction-and-tracking-from-monocular-video-cvpr-2026-paper/fig-039.webp\", \"caption\": \"\", \"page\": 7, \"index\": 39, \"width\": 1024, \"height\": 1024}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiang-mesh4d-4d-mesh-reconstruction-and-tracking-from-monocular-video-cvpr-2026-paper/fig-040.webp\", \"caption\": \"\", \"page\": 7, \"index\": 40, \"width\": 1024, \"height\": 1024}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiang-mesh4d-4d-mesh-reconstruction-and-tracking-from-monocular-video-cvpr-2026-paper/fig-041.webp\", \"caption\": \"\", \"page\": 7, \"index\": 41, \"width\": 1024, \"height\": 1024}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiang-mesh4d-4d-mesh-reconstruction-and-tracking-from-monocular-video-cvpr-2026-paper/fig-042.webp\", \"caption\": \"\", \"page\": 7, \"index\": 42, \"width\": 1024, \"height\": 1024}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiang-mesh4d-4d-mesh-reconstruction-and-tracking-from-monocular-video-cvpr-2026-paper/fig-043.webp\", \"caption\": \"\", \"page\": 7, \"index\": 43, \"width\": 1024, \"height\": 1024}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiang-mesh4d-4d-mesh-reconstruction-and-tracking-from-monocular-video-cvpr-2026-paper/fig-044.webp\", \"caption\": \"\", \"page\": 7, \"index\": 44, \"width\": 1024, \"height\": 1024}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiang-mesh4d-4d-mesh-reconstruction-and-tracking-from-monocular-video-cvpr-2026-paper/fig-045.webp\", \"caption\": \"\", \"page\": 7, \"index\": 45, \"width\": 1024, \"height\": 1024}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiang-mesh4d-4d-mesh-reconstruction-and-tracking-from-monocular-video-cvpr-2026-paper/fig-046.webp\", \"caption\": \"\", \"page\": 7, \"index\": 46, \"width\": 1024, \"height\": 1024}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiang-mesh4d-4d-mesh-reconstruction-and-tracking-from-monocular-video-cvpr-2026-paper/fig-047.webp\", \"caption\": \"\", \"page\": 7, \"index\": 47, \"width\": 1024, \"height\": 1024}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiang-mesh4d-4d-mesh-reconstruction-and-tracking-from-monocular-video-cvpr-2026-paper/fig-048.webp\", \"caption\": \"\", \"page\": 7, \"index\": 48, \"width\": 512, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiang-mesh4d-4d-mesh-reconstruction-and-tracking-from-monocular-video-cvpr-2026-paper/fig-049.webp\", \"caption\": \"\", \"page\": 7, \"index\": 49, \"width\": 512, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiang-mesh4d-4d-mesh-reconstruction-and-tracking-from-monocular-video-cvpr-2026-paper/fig-050.webp\", \"caption\": \"\", \"page\": 7, \"index\": 50, \"width\": 512, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiang-mesh4d-4d-mesh-reconstruction-and-tracking-from-monocular-video-cvpr-2026-paper/fig-051.webp\", \"caption\": \"\", \"page\": 7, \"index\": 51, \"width\": 512, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiang-mesh4d-4d-mesh-reconstruction-and-tracking-from-monocular-video-cvpr-2026-paper/fig-052.webp\", \"caption\": \"\", \"page\": 7, \"index\": 52, \"width\": 512, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiang-mesh4d-4d-mesh-reconstruction-and-tracking-from-monocular-video-cvpr-2026-paper/fig-053.webp\", \"caption\": \"\", \"page\": 7, \"index\": 53, \"width\": 512, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiang-mesh4d-4d-mesh-reconstruction-and-tracking-from-monocular-video-cvpr-2026-paper/fig-054.webp\", \"caption\": \"\", \"page\": 7, \"index\": 54, \"width\": 1024, \"height\": 1024}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiang-mesh4d-4d-mesh-reconstruction-and-tracking-from-monocular-video-cvpr-2026-paper/fig-055.webp\", \"caption\": \"\", \"page\": 7, \"index\": 55, \"width\": 512, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiang-mesh4d-4d-mesh-reconstruction-and-tracking-from-monocular-video-cvpr-2026-paper/fig-056.webp\", \"caption\": \"\", \"page\": 7, \"index\": 56, \"width\": 512, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiang-mesh4d-4d-mesh-reconstruction-and-tracking-from-monocular-video-cvpr-2026-paper/fig-057.webp\", \"caption\": \"\", \"page\": 7, \"index\": 57, \"width\": 512, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiang-mesh4d-4d-mesh-reconstruction-and-tracking-from-monocular-video-cvpr-2026-paper/fig-058.webp\", \"caption\": \"\", \"page\": 7, \"index\": 58, \"width\": 512, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiang-mesh4d-4d-mesh-reconstruction-and-tracking-from-monocular-video-cvpr-2026-paper/fig-059.webp\", \"caption\": \"\", \"page\": 7, \"index\": 59, \"width\": 512, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiang-mesh4d-4d-mesh-reconstruction-and-tracking-from-monocular-video-cvpr-2026-paper/fig-060.webp\", \"caption\": \"\", \"page\": 7, \"index\": 60, \"width\": 512, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiang-mesh4d-4d-mesh-reconstruction-and-tracking-from-monocular-video-cvpr-2026-paper/fig-061.webp\", \"caption\": \"\", \"page\": 7, \"index\": 61, \"width\": 512, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiang-mesh4d-4d-mesh-reconstruction-and-tracking-from-monocular-video-cvpr-2026-paper/fig-062.webp\", \"caption\": \"\", \"page\": 7, \"index\": 62, \"width\": 512, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiang-mesh4d-4d-mesh-reconstruction-and-tracking-from-monocular-video-cvpr-2026-paper/fig-063.webp\", \"caption\": \"\", \"page\": 7, \"index\": 63, \"width\": 512, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiang-mesh4d-4d-mesh-reconstruction-and-tracking-from-monocular-video-cvpr-2026-paper/fig-064.webp\", \"caption\": \"\", \"page\": 7, \"index\": 64, \"width\": 512, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiang-mesh4d-4d-mesh-reconstruction-and-tracking-from-monocular-video-cvpr-2026-paper/fig-065.webp\", \"caption\": \"\", \"page\": 7, \"index\": 65, \"width\": 1024, \"height\": 1024}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiang-mesh4d-4d-mesh-reconstruction-and-tracking-from-monocular-video-cvpr-2026-paper/fig-066.webp\", \"caption\": \"\", \"page\": 7, \"index\": 66, \"width\": 512, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiang-mesh4d-4d-mesh-reconstruction-and-tracking-from-monocular-video-cvpr-2026-paper/fig-067.webp\", \"caption\": \"\", \"page\": 7, \"index\": 67, \"width\": 512, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiang-mesh4d-4d-mesh-reconstruction-and-tracking-from-monocular-video-cvpr-2026-paper/fig-068.webp\", \"caption\": \"\", \"page\": 7, \"index\": 68, \"width\": 512, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiang-mesh4d-4d-mesh-reconstruction-and-tracking-from-monocular-video-cvpr-2026-paper/fig-069.webp\", \"caption\": \"\", \"page\": 7, \"index\": 69, \"width\": 512, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiang-mesh4d-4d-mesh-reconstruction-and-tracking-from-monocular-video-cvpr-2026-paper/fig-070.webp\", \"caption\": \"\", \"page\": 7, \"index\": 70, \"width\": 512, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiang-mesh4d-4d-mesh-reconstruction-and-tracking-from-monocular-video-cvpr-2026-paper/fig-071.webp\", \"caption\": \"\", \"page\": 7, \"index\": 71, \"width\": 512, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiang-mesh4d-4d-mesh-reconstruction-and-tracking-from-monocular-video-cvpr-2026-paper/fig-072.webp\", \"caption\": \"\", \"page\": 7, \"index\": 72, \"width\": 512, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiang-mesh4d-4d-mesh-reconstruction-and-tracking-from-monocular-video-cvpr-2026-paper/fig-073.webp\", \"caption\": \"\", \"page\": 7, \"index\": 73, \"width\": 512, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiang-mesh4d-4d-mesh-reconstruction-and-tracking-from-monocular-video-cvpr-2026-paper/fig-074.webp\", \"caption\": \"\", \"page\": 7, \"index\": 74, \"width\": 1024, \"height\": 1024}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiang-mesh4d-4d-mesh-reconstruction-and-tracking-from-monocular-video-cvpr-2026-paper/fig-075.webp\", \"caption\": \"\", \"page\": 7, \"index\": 75, \"width\": 1024, \"height\": 1024}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiang-mesh4d-4d-mesh-reconstruction-and-tracking-from-monocular-video-cvpr-2026-paper/fig-076.webp\", \"caption\": \"\", \"page\": 7, \"index\": 76, \"width\": 1024, \"height\": 1024}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiang-mesh4d-4d-mesh-reconstruction-and-tracking-from-monocular-video-cvpr-2026-paper/fig-077.webp\", \"caption\": \"\", \"page\": 7, \"index\": 77, \"width\": 1024, \"height\": 1024}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiang-mesh4d-4d-mesh-reconstruction-and-tracking-from-monocular-video-cvpr-2026-paper/fig-078.webp\", \"caption\": \"\", \"page\": 7, \"index\": 78, \"width\": 1024, \"height\": 1024}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiang-mesh4d-4d-mesh-reconstruction-and-tracking-from-monocular-video-cvpr-2026-paper/fig-079.webp\", \"caption\": \"\", \"page\": 8, \"index\": 79, \"width\": 1024, \"height\": 1024}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiang-mesh4d-4d-mesh-reconstruction-and-tracking-from-monocular-video-cvpr-2026-paper/fig-080.webp\", \"caption\": \"\", \"page\": 8, \"index\": 80, \"width\": 1024, \"height\": 1024}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiang-mesh4d-4d-mesh-reconstruction-and-tracking-from-monocular-video-cvpr-2026-paper/fig-081.webp\", \"caption\": \"\", \"page\": 8, \"index\": 81, \"width\": 512, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiang-mesh4d-4d-mesh-reconstruction-and-tracking-from-monocular-video-cvpr-2026-paper/fig-082.webp\", \"caption\": \"\", \"page\": 8, \"index\": 82, \"width\": 512, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiang-mesh4d-4d-mesh-reconstruction-and-tracking-from-monocular-video-cvpr-2026-paper/fig-083.webp\", \"caption\": \"\", \"page\": 8, \"index\": 83, \"width\": 512, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiang-mesh4d-4d-mesh-reconstruction-and-tracking-from-monocular-video-cvpr-2026-paper/fig-084.webp\", \"caption\": \"\", \"page\": 8, \"index\": 84, \"width\": 512, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiang-mesh4d-4d-mesh-reconstruction-and-tracking-from-monocular-video-cvpr-2026-paper/fig-085.webp\", \"caption\": \"\", \"page\": 8, \"index\": 85, \"width\": 512, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiang-mesh4d-4d-mesh-reconstruction-and-tracking-from-monocular-video-cvpr-2026-paper/fig-086.webp\", \"caption\": \"\", \"page\": 8, \"index\": 86, \"width\": 512, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiang-mesh4d-4d-mesh-reconstruction-and-tracking-from-monocular-video-cvpr-2026-paper/fig-087.webp\", \"caption\": \"\", \"page\": 8, \"index\": 87, \"width\": 1024, \"height\": 1024}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiang-mesh4d-4d-mesh-reconstruction-and-tracking-from-monocular-video-cvpr-2026-paper/fig-088.webp\", \"caption\": \"\", \"page\": 8, \"index\": 88, \"width\": 1024, \"height\": 1024}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiang-mesh4d-4d-mesh-reconstruction-and-tracking-from-monocular-video-cvpr-2026-paper/fig-089.webp\", \"caption\": \"\", \"page\": 8, \"index\": 89, \"width\": 1024, \"height\": 1024}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiang-mesh4d-4d-mesh-reconstruction-and-tracking-from-monocular-video-cvpr-2026-paper/fig-090.webp\", \"caption\": \"\", \"page\": 8, \"index\": 90, \"width\": 1024, \"height\": 1024}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiang-mesh4d-4d-mesh-reconstruction-and-tracking-from-monocular-video-cvpr-2026-paper/fig-091.webp\", \"caption\": \"\", \"page\": 8, \"index\": 91, \"width\": 1024, \"height\": 1024}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiang-mesh4d-4d-mesh-reconstruction-and-tracking-from-monocular-video-cvpr-2026-paper/fig-092.webp\", \"caption\": \"\", \"page\": 8, \"index\": 92, \"width\": 1024, \"height\": 1024}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiang-mesh4d-4d-mesh-reconstruction-and-tracking-from-monocular-video-cvpr-2026-paper/fig-093.webp\", \"caption\": \"\", \"page\": 8, \"index\": 93, \"width\": 1024, \"height\": 1024}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiang-mesh4d-4d-mesh-reconstruction-and-tracking-from-monocular-video-cvpr-2026-paper/fig-094.webp\", \"caption\": \"\", \"page\": 8, \"index\": 94, \"width\": 1024, \"height\": 1024}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiang-mesh4d-4d-mesh-reconstruction-and-tracking-from-monocular-video-cvpr-2026-paper/fig-095.webp\", \"caption\": \"\", \"page\": 8, \"index\": 95, \"width\": 1024, \"height\": 1024}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiang-mesh4d-4d-mesh-reconstruction-and-tracking-from-monocular-video-cvpr-2026-paper/fig-096.webp\", \"caption\": \"\", \"page\": 8, \"index\": 96, \"width\": 512, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiang-mesh4d-4d-mesh-reconstruction-and-tracking-from-monocular-video-cvpr-2026-paper/fig-097.webp\", \"caption\": \"\", \"page\": 8, \"index\": 97, \"width\": 512, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiang-mesh4d-4d-mesh-reconstruction-and-tracking-from-monocular-video-cvpr-2026-paper/fig-098.webp\", \"caption\": \"\", \"page\": 8, \"index\": 98, \"width\": 512, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiang-mesh4d-4d-mesh-reconstruction-and-tracking-from-monocular-video-cvpr-2026-paper/fig-099.webp\", \"caption\": \"\", \"page\": 8, \"index\": 99, \"width\": 512, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiang-mesh4d-4d-mesh-reconstruction-and-tracking-from-monocular-video-cvpr-2026-paper/fig-100.webp\", \"caption\": \"\", \"page\": 8, \"index\": 100, \"width\": 512, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiang-mesh4d-4d-mesh-reconstruction-and-tracking-from-monocular-video-cvpr-2026-paper/fig-101.webp\", \"caption\": \"\", \"page\": 8, \"index\": 101, \"width\": 512, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiang-mesh4d-4d-mesh-reconstruction-and-tracking-from-monocular-video-cvpr-2026-paper/fig-102.webp\", \"caption\": \"\", \"page\": 8, \"index\": 102, \"width\": 1024, \"height\": 1024}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiang-mesh4d-4d-mesh-reconstruction-and-tracking-from-monocular-video-cvpr-2026-paper/fig-103.webp\", \"caption\": \"\", \"page\": 8, \"index\": 103, \"width\": 512, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiang-mesh4d-4d-mesh-reconstruction-and-tracking-from-monocular-video-cvpr-2026-paper/fig-104.webp\", \"caption\": \"\", \"page\": 8, \"index\": 104, \"width\": 512, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiang-mesh4d-4d-mesh-reconstruction-and-tracking-from-monocular-video-cvpr-2026-paper/fig-105.webp\", \"caption\": \"\", \"page\": 8, \"index\": 105, \"width\": 1024, \"height\": 1024}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiang-mesh4d-4d-mesh-reconstruction-and-tracking-from-monocular-video-cvpr-2026-paper/fig-106.webp\", \"caption\": \"\", \"page\": 8, \"index\": 106, \"width\": 1024, \"height\": 1024}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiang-mesh4d-4d-mesh-reconstruction-and-tracking-from-monocular-video-cvpr-2026-paper/fig-107.webp\", \"caption\": \"\", \"page\": 8, \"index\": 107, \"width\": 1024, \"height\": 1024}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiang-mesh4d-4d-mesh-reconstruction-and-tracking-from-monocular-video-cvpr-2026-paper/fig-108.webp\", \"caption\": \"\", \"page\": 8, \"index\": 108, \"width\": 1024, \"height\": 1024}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiang-mesh4d-4d-mesh-reconstruction-and-tracking-from-monocular-video-cvpr-2026-paper/fig-109.webp\", \"caption\": \"\", \"page\": 8, \"index\": 109, \"width\": 1024, \"height\": 1024}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiang-mesh4d-4d-mesh-reconstruction-and-tracking-from-monocular-video-cvpr-2026-paper/fig-110.webp\", \"caption\": \"\", \"page\": 8, \"index\": 110, \"width\": 1024, \"height\": 1024}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiang-mesh4d-4d-mesh-reconstruction-and-tracking-from-monocular-video-cvpr-2026-paper/fig-111.webp\", \"caption\": \"\", \"page\": 8, \"index\": 111, \"width\": 1024, \"height\": 1024}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiang-mesh4d-4d-mesh-reconstruction-and-tracking-from-monocular-video-cvpr-2026-paper/fig-112.webp\", \"caption\": \"\", \"page\": 8, \"index\": 112, \"width\": 1024, \"height\": 1024}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiang-mesh4d-4d-mesh-reconstruction-and-tracking-from-monocular-video-cvpr-2026-paper/fig-113.webp\", \"caption\": \"\", \"page\": 8, \"index\": 113, \"width\": 1024, \"height\": 1024}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiang-mesh4d-4d-mesh-reconstruction-and-tracking-from-monocular-video-cvpr-2026-paper/fig-114.webp\", \"caption\": \"\", \"page\": 8, \"index\": 114, \"width\": 1024, \"height\": 1024}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiang-mesh4d-4d-mesh-reconstruction-and-tracking-from-monocular-video-cvpr-2026-paper/fig-115.webp\", \"caption\": \"\", \"page\": 8, \"index\": 115, \"width\": 1024, \"height\": 1024}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiang-mesh4d-4d-mesh-reconstruction-and-tracking-from-monocular-video-cvpr-2026-paper/fig-116.webp\", \"caption\": \"\", \"page\": 8, \"index\": 116, \"width\": 1024, \"height\": 1024}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiang-mesh4d-4d-mesh-reconstruction-and-tracking-from-monocular-video-cvpr-2026-paper/fig-117.webp\", \"caption\": \"\", \"page\": 8, \"index\": 117, \"width\": 1024, \"height\": 1024}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiang-mesh4d-4d-mesh-reconstruction-and-tracking-from-monocular-video-cvpr-2026-paper/fig-118.webp\", \"caption\": \"\", \"page\": 8, \"index\": 118, \"width\": 1024, \"height\": 1024}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiang-mesh4d-4d-mesh-reconstruction-and-tracking-from-monocular-video-cvpr-2026-paper/fig-119.webp\", \"caption\": \"\", \"page\": 8, \"index\": 119, \"width\": 1024, \"height\": 1024}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiang-mesh4d-4d-mesh-reconstruction-and-tracking-from-monocular-video-cvpr-2026-paper/fig-120.webp\", \"caption\": \"\", \"page\": 8, \"index\": 120, \"width\": 1024, \"height\": 1024}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiang-mesh4d-4d-mesh-reconstruction-and-tracking-from-monocular-video-cvpr-2026-paper/fig-121.webp\", \"caption\": \"\", \"page\": 8, \"index\": 121, \"width\": 1024, \"height\": 1024}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiang-mesh4d-4d-mesh-reconstruction-and-tracking-from-monocular-video-cvpr-2026-paper/fig-122.webp\", \"caption\": \"\", \"page\": 8, \"index\": 122, \"width\": 1024, \"height\": 1024}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiang-mesh4d-4d-mesh-reconstruction-and-tracking-from-monocular-video-cvpr-2026-paper/fig-123.webp\", \"caption\": \"\", \"page\": 8, \"index\": 123, \"width\": 1024, \"height\": 1024}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiang-mesh4d-4d-mesh-reconstruction-and-tracking-from-monocular-video-cvpr-2026-paper/fig-124.webp\", \"caption\": \"\", \"page\": 8, \"index\": 124, \"width\": 1024, \"height\": 1024}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiang-mesh4d-4d-mesh-reconstruction-and-tracking-from-monocular-video-cvpr-2026-paper/fig-125.webp\", \"caption\": \"\", \"page\": 8, \"index\": 125, \"width\": 512, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiang-mesh4d-4d-mesh-reconstruction-and-tracking-from-monocular-video-cvpr-2026-paper/fig-126.webp\", \"caption\": \"\", \"page\": 8, \"index\": 126, \"width\": 512, \"height\": 512}]"
motivation: 从单目视频重建动态物体的完整3D形状与运动具有挑战，且缺乏稳定的形变表示。
method: 提出前馈模型Mesh4D，用编码整段动画序列的紧凑隐空间表示形变场，训练时由骨架结构引导，并基于该表示训练隐扩散模型。
result: 模型在推理时无需骨架信息即可重建物体完整形状与运动，时空注意力带来更稳定的形变表示。
conclusion: 该工作将4D网格重建与跟踪统一为隐空间建模，为单目动态物体重建提供可扩展方案。
---

## Abstract
We propose Mesh4D, a feed-forward model for monocular 4D mesh reconstruction. Given a monocular video of a dynamic object, our model reconstructs the object's complete 3D shape and motion, represented as a deformation field. Our key contribution is a compact latent space that encodes the entire animation sequence. This latent space is learned by an autoencoder that, during training, is guided by the skeletal structure of the training objects, providing strong priors on plausible deformations. Crucially, skeletal information is not required at inference time. The encoder employs spatio-temporal attention, yielding a more stable representation of the object's overall deformation. Building on this representation, we train a latent diffusion model that, conditioned on the input video and the mesh reconstructed from the first frame, predicts the full animation in one shot. We evaluate Mesh4D on reconstruction and novel view synthesis benchmarks, outperforming prior methods in recovering accurate 3D shape and deformation.

---

## 论文详细总结（自动生成）

# Mesh4D 论文中文总结

## 1. 核心问题与整体含义

- **研究背景**：单目视频中的 4D 形状重建旨在从一段单目 RGB 视频中恢复动态物体的完整 3D 形状与运动，在视觉、图形学和机器人领域有广泛应用，例如自动创建 3D 动画。
- **核心困难**：
  - 单目视频仅包含有限的 3D 形状与运动信息，必须推断大量不可见区域。
  - 传统基于优化的 analysis-by-synthesis 方法只能重建可见部分，且易受遮挡和歧义影响，结果噪声较大。
  - 已有前馈方法多只处理两帧或逐帧重建，无法建模整段视频中的完整 4D 结构。
  - 现有 3D 生成/扩散方法虽能提供 3D 先验，但部分工作更关注“看起来合理”的新视角合成，而非准确的几何与跟踪。
- **整体含义**：论文提出 Mesh4D，将 4D 网格重建与跟踪统一为一个前馈生成问题：从单目视频一次性预测完整 3D 网格及其随时间的形变场，避免逐场景优化，并提升几何、运动与外观一致性。

## 2. 方法论

### 2.1 核心思想

- **问题形式化**：给定视频 \( I=\{I_t\}_{t=1}^T \)，目标是输出第一帧的 3D 网格 \( M_1=(V_1,F_1) \) 以及从第 1 帧到第 t 帧的稠密形变场 \( T_{1\to t} \)，从而得到变形网格 \( M_t=(V_1+T_{1\to t}(V_1),F_1) \)。
- **总体框架**：
  1. 使用预训练图像到 3D 生成器从第一帧重建 canonical mesh \( M_1 \)。
  2. 使用新的形变 VAE 将整段动画序列编码为紧凑隐变量 \( z_d \)。
  3. 训练隐扩散模型，以输入视频和 canonical mesh 为条件，一次性预测完整动画的形变隐变量。
- **关键特点**：推理时不需要骨架信息；骨架仅在训练 VAE 时作为“特权信息”提供形变先验。

### 2.2 静态 3D 重建骨干

- 基于预训练 Hunyuan3D 2.1 的 latent 3D 重建模型。
- 其 VAE 将网格编码为 VecSet 隐变量 \( z_s \)：从网格采样点云和法线，经神经网络得到隐编码；解码器通过 SDF 和 Marching Cubes 恢复网格。
- 通过 flow matching 训练条件扩散生成器，从图像采样 \( z_s \sim p(z_s|I) \)。
- 该骨干仅用于从第一帧 \( I_1 \) 重建静态参考网格 \( M_1 \)。

### 2.3 形变 VAE

- **输入**：网格序列 \( \{M_t\}_{t=1}^T \)，以及训练时可用的法线 \( n \)、蒙皮权重 \( w \)、骨骼 \( b \)。
- **编码器**：
  - 从 \( M_1 \) 采样点云，并通过重心坐标追踪这些点在每一帧的对应位置，构造跨时间对应的点云序列 \( \{P_t\} \)。
  - 将第 1 帧与第 t 帧的点坐标、法线拼接并投影为点特征 \( h_t \)。
  - **骨架注入**：
    - 使用蒙皮权重构造自注意力偏置/掩码，使同属一个骨骼的点更容易互相注意。
    - 将骨骼头尾位置编码为骨骼特征，通过带蒙皮权重掩码的 cross-attention 注入点特征。
  - **时空注意力**：
    - 使用 Farthest Point Sampling 对点进行下采样，降低计算量。
    - 采用空间注意力、时间注意力、全局注意力交替的 Transformer 结构，并加入 RoPE 时间位置编码。
    - 经过 8 层注意力后，预测每帧形变隐分布的均值和方差，采样得到 \( z_d \)。
- **解码器**：
  - 将 \( z_d \) 投影后，经过 16 层时空注意力块。
  - 以 canonical 顶点 \( V_1 \) 作为 query，通过 cross-attention 输出每个顶点在各时刻的形变 \( T_{1\to t}(V_1) \)。
- **训练目标**：
  - 最小化预测形变与真实顶点位移之间的 L2 损失，并加入 KL 正则项：
    \[
    L_{VAE}=\sum_t \|(V_t-V_1)-D_t^d(V_1;z_d)\|_2^2+\lambda L_{KL}
    \]
  - 实际中为效率只对随机子集顶点计算损失。

### 2.4 形变扩散模型

- 目标是学习 \( z_d \sim p(z_d|M_1,I) \)。
- 在 HY3D 2.1 的 shape diffusion 模型基础上扩展：
  - 增加时间嵌入与空间嵌入。
  - 空间嵌入来自 \( M_1 \) 上 FPS 采样点的位置，用于增强空间一致性。
  - 每个 DiT block 增加额外注意力层，融合视频时序线索和 canonical 形状信息。
  - 视频特征由 DINO-Giant 逐帧提取，并由对应 latent token 进行 cross-attention。
  - 还使用 canonical mesh 的 shape feature \( z_s \) 作为细节条件。
- 训练目标与静态 shape diffusion 的 flow matching 目标一致。

## 3. 实验设计

### 3.1 数据集与 Benchmark

- **训练数据**：
  - 从 Diffusion4D 筛选过的 Objaverse-1.0 版本出发。
  - 过滤运动过小或形变过大的对象，提取骨架、蒙皮权重和对应顶点序列。
  - 过滤顶点数或骨骼数过多的对象，保留约 9k 个实例。
  - 每个实例渲染为正面视频，最多 100 帧。
- **测试数据**：
  - 选取 50 个与训练集不重叠的动画 3D 资产。
  - 要求具有显著物体运动、高质量纹理。
  - 每个序列渲染 4 个固定视角视频，方位角为 \(0^\circ,90^\circ,180^\circ,270^\circ\)。
  - 一个视角作为输入，其余三个用于新视角合成评估。
- **Benchmark 特点**：论文提出新 benchmark，重点评估 3D 形状与运动重建质量，而不仅是渲染视频的视觉质量。

### 3.2 对比方法

- Hunyuan3D 2.1（HY3D）：逐帧图像到 3D 重建，使用共享噪声改善时序一致性。
- L4GM：前馈 4D Gaussian 重建方法。
- GVFD：基于 Gaussian Variation Field 的视频到 4D 生成方法。
- 对于 L4GM 和 GVFD，取不透明度大于 0.01 的 Gaussian 中心作为点云进行几何评估。
- 使用 Coherent Point Drift 对齐第一帧网格的尺度和刚体变换；表中 Aligned 表示将对齐后的 canonical shape 输入形变扩散模型。

### 3.3 评价指标

- **几何重建**：Volumetric IoU、Point-to-Surface 距离、Chamfer 距离。
- **跟踪**：\( \pi^2 \)-Corr，即预测网格与 GT 网格上第一帧最近邻对应点之间的欧氏距离。
- **新视角合成**：PSNR、SSIM、LPIPS、CLIP 相似度、FVD 时序一致性。

### 3.4 主要实验结果

- **几何与跟踪**：
  - Mesh4D 在 IoU、P2S、Chamfer、\( \pi^2 \)-Corr 上均优于 HY3D、L4GM、GVFD。
  - Ours：IoU 0.3731，P2S 0.0287，Chamfer 0.0273，\( \pi^2 \)-Corr 0.0384。
  - Ours (Aligned)：IoU 0.3949，P2S 0.0261，Chamfer 0.0243，\( \pi^2 \)-Corr 0.0338。
- **新视角合成**：
  - Mesh4D 在 PSNR、SSIM、LPIPS、FVD 上最优。
  - Ours：PSNR 19.67，SSIM 0.9018，LPIPS 0.1087，FVD 601.9。
  - Ours (Aligned)：PSNR 19.88，SSIM 0.9030，LPIPS 0.1052，FVD 572.7。
  - CLIP 分数略低于 HY3D，原因是 Mesh4D 只从第一帧生成纹理，而 HY3D 每帧重新生成纹理。
- **消融实验**：
  - 去掉时间与全局注意力：IoU 0.6328，P2S 0.0153，Chamfer 0.0113，\( \pi^2 \)-Corr 0.0160。
  - 去掉骨架信息：IoU 0.6704，P2S 0.0148，Chamfer 0.0107，\( \pi^2 \)-Corr 0.0138。
  - 完整模型：IoU 0.7039，P2S 0.0144，Chamfer 0.0099，\( \pi^2 \)-Corr 0.0117。
  - 定性结果：去掉骨架会导致刚体变换错误，如“扭曲的棍子”；去掉时间与全局注意力会导致抖动和脚部附近误差增大。

## 4. 资源与算力

- **论文正文未明确说明**使用的 GPU 型号、GPU 数量、训练总时长、显存消耗或具体计算资源。
- 文中提到训练数据规模约 9k 个 Objaverse 实例、每个实例最多 100 帧，并基于预训练 Hunyuan3D 2.1 和 DINO-Giant 等大模型，但未给出训练硬件与时间细节。
- 因此，无法从论文文本中判断其训练成本、推理速度和实际部署资源需求。

## 5. 实验数量与充分性

- **实验组数概览**：
  - 主几何与跟踪对比实验：1 组，覆盖 3 个基线方法和 2 个本文变体。
  - 新视角合成对比实验：1 组，覆盖 3 个基线方法和 2 个本文变体。
  - 消融实验：2 个主要变体，分别去掉骨架信息和去掉时间/全局注意力，另有完整模型对比。
  - 定性实验：几何重建对比、NVS 对比、消融可视化。
- **充分性**：
  - 在自建 Objaverse 子集 benchmark 上，实验覆盖了几何、跟踪、NVS 和时序一致性，指标较全面。
  - 消融实验验证了骨架信息和时空注意力的有效性。
  - 但实验主要集中在合成 3D 动画资产，未在真实单目视频上系统评估。
  - 基线数量有限，且部分基线本身并非专门为完整 4D 网格重建与稠密跟踪设计。
  - 3D-GS 类方法不直接定义内外表面，因此 volumetric IoU 不适用；HY3D 和 L4GM 也不直接支持跟踪评估，导致部分指标不可比。
- **公平性**：
  - 论文使用 CPD 对齐尺度和刚体变换，并区分“Ours”和“Ours (Aligned)”，一定程度上控制了 canonical mesh 对齐差异。
  - 但不同方法的表示不同，几何评估方式存在天然差异，公平性仍受限于任务设定和指标适配。

## 6. 主要结论与发现

- Mesh4D 能够从单目 RGB 视频前馈式重建完整 3D 网格及其形变，并实现顶点级跟踪。
- 将整段动画序列编码到紧凑隐空间，比逐帧或双帧建模更稳定、更准确。
- 训练时引入骨架、蒙皮权重和骨骼信息，可显著提升形变隐空间质量；推理时无需骨架。
- 时空注意力和全局注意力有助于捕捉长期时空相关性，减少抖动并提升时序一致性。
- 基于该隐空间的 latent diffusion 模型能够一次性预测完整动画，条件于输入视频和第一帧重建网格。
- 在 Objaverse 子集 benchmark 上，Mesh4D 在几何重建、跟踪和新视角合成的大部分指标上达到 state-of-the-art。

## 7. 优点

- **统一框架**：将 4D 网格重建与跟踪统一为形变场隐空间建模，显式建模物体运动，有利于纹理一致性和时序一致性。
- **前馈高效**：推理时无需逐场景优化，相比 V2M4 等需要后优化的方法更高效、更灵活。
- **骨架特权信息**：训练时利用骨架和蒙皮权重提供强形变先验，但推理时不需要骨架，兼顾先验学习与部署便利。
- **时空注意力设计**：编码器联合建模空间、时间和全局注意力，能够捕捉点轨迹的长期相关性，提升形变表示稳定性。
- **基于强预训练 3D 先验**：建立在 Hunyuan3D 2.1 等大规模 3D 生成模型之上，增强了对多样物体的泛化和不可见区域补全能力。
- **新 benchmark**：强调 3D 形状与运动重建质量，而非仅关注 2D 渲染质量，更贴近 4D 重建的核心目标。
- **消融清晰**：通过定量和定性消融明确验证了骨架信息和时空注意力的贡献。

## 8. 不足与局限

- **依赖高质量 canonical mesh**：方法建立在预训练图像到 3D 生成器之上，若第一帧重建的 canonical mesh 不准确，会直接影响后续 4D 重建。
- **训练依赖骨架**：虽然推理时不需要骨架，但训练 VAE 需要骨架、蒙皮权重和骨骼信息，限制了可训练数据范围。
- **无法表示拓扑变化**：形变场基于固定网格顶点和面，不能处理物体拓扑结构随时间变化的情况。
- **非常非刚体对象困难**：论文自述难以重建非常非刚性的物体。
- **纹理限制**：纹理仅从第一帧生成，导致 CLIP 相似度低于逐帧生成纹理的 HY3D。
- **实验覆盖有限**：
  - 主要在 Objaverse 合成动画资产上评估，未充分验证真实世界单目视频。
  - 测试集为 50 个序列，规模相对有限。
  - 对比方法数量有限，且部分指标因表示差异无法完全公平比较。
- **算力信息缺失**：未报告 GPU 型号、数量、训练时长等资源消耗，难以评估可复现性和实际成本。
- **推理效率未量化**：虽然强调前馈和无需逐场景优化，但未给出具体推理时间或吞吐量。
- **潜在偏差风险**：训练和测试均来自 Objaverse 类合成 3D 资产，可能对真实场景中的光照、遮挡、运动模糊、非刚性形变等存在域偏差。

（完）
