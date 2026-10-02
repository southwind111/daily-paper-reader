---
title: "4DGS360: 360° Gaussian Reconstruction of Dynamic Objects from a Single Video"
title_zh: 4DGS360：从单段视频对动态物体进行360度高斯重建
authors: "Jae Won Jang, Yeonjin Chang, Wonsik Shin, Juhwan Cho, Nojun Kwak"
date: 2026
publication_date: 2026
publication_date_precision: year
publication_date_source: conference year only; exact release date unverified
publication_date_kind: unknown
pdf: "https://media.eventhosts.cc/Conferences/ECCV2026/pdfs/7789.pdf"
tags: ["query:dr"]
score: 9.0
evidence: 从单段视频对动态物体进行360度四维高斯重建
tldr: 现有方法依赖二维先验，初始点易过拟合各训练视角的可见表面，难以重建一致的360度动态几何。本文提出免扩散的4DGS360框架，采用三维原生初始化缓解遮挡区域几何歧义，并提出AnchorTAP3D三维跟踪器，以置信二维轨迹点为锚点强化三维轨迹、抑制漂移。实验表明该初始化结合优化可在遮挡区域保持几何一致，实现连贯的360度四维动态物体重建。
source: ECCV-2026-Accepted-Program
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-a971f1116ac1b4514b410ee0/fig-001.webp\", \"caption\": \"\", \"page\": 2, \"index\": 1, \"width\": 720, \"height\": 960}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-a971f1116ac1b4514b410ee0/fig-002.webp\", \"caption\": \"\", \"page\": 2, \"index\": 2, \"width\": 720, \"height\": 960}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-a971f1116ac1b4514b410ee0/fig-003.webp\", \"caption\": \"\", \"page\": 2, \"index\": 3, \"width\": 720, \"height\": 960}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-a971f1116ac1b4514b410ee0/fig-004.webp\", \"caption\": \"\", \"page\": 2, \"index\": 4, \"width\": 720, \"height\": 960}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-a971f1116ac1b4514b410ee0/fig-005.webp\", \"caption\": \"\", \"page\": 2, \"index\": 5, \"width\": 720, \"height\": 960}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-a971f1116ac1b4514b410ee0/fig-006.webp\", \"caption\": \"\", \"page\": 2, \"index\": 6, \"width\": 720, \"height\": 960}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-a971f1116ac1b4514b410ee0/fig-007.webp\", \"caption\": \"\", \"page\": 2, \"index\": 7, \"width\": 720, \"height\": 960}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-a971f1116ac1b4514b410ee0/fig-008.webp\", \"caption\": \"\", \"page\": 2, \"index\": 8, \"width\": 414, \"height\": 581}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-a971f1116ac1b4514b410ee0/fig-009.webp\", \"caption\": \"\", \"page\": 2, \"index\": 9, \"width\": 370, \"height\": 487}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-a971f1116ac1b4514b410ee0/fig-010.webp\", \"caption\": \"\", \"page\": 2, \"index\": 10, \"width\": 498, \"height\": 269}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-a971f1116ac1b4514b410ee0/fig-011.webp\", \"caption\": \"\", \"page\": 2, \"index\": 11, \"width\": 436, \"height\": 365}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-a971f1116ac1b4514b410ee0/fig-012.webp\", \"caption\": \"\", \"page\": 2, \"index\": 12, \"width\": 447, \"height\": 343}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-a971f1116ac1b4514b410ee0/fig-013.webp\", \"caption\": \"\", \"page\": 2, \"index\": 13, \"width\": 391, \"height\": 326}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-a971f1116ac1b4514b410ee0/fig-014.webp\", \"caption\": \"\", \"page\": 2, \"index\": 14, \"width\": 859, \"height\": 653}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-a971f1116ac1b4514b410ee0/fig-015.webp\", \"caption\": \"\", \"page\": 2, \"index\": 15, \"width\": 720, \"height\": 960}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-a971f1116ac1b4514b410ee0/fig-016.webp\", \"caption\": \"\", \"page\": 2, \"index\": 16, \"width\": 360, \"height\": 480}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-a971f1116ac1b4514b410ee0/fig-017.webp\", \"caption\": \"\", \"page\": 2, \"index\": 17, \"width\": 360, \"height\": 480}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-a971f1116ac1b4514b410ee0/fig-018.webp\", \"caption\": \"\", \"page\": 2, \"index\": 18, \"width\": 360, \"height\": 480}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-a971f1116ac1b4514b410ee0/fig-019.webp\", \"caption\": \"\", \"page\": 2, \"index\": 19, \"width\": 360, \"height\": 480}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-a971f1116ac1b4514b410ee0/fig-020.webp\", \"caption\": \"\", \"page\": 2, \"index\": 20, \"width\": 360, \"height\": 480}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-a971f1116ac1b4514b410ee0/fig-021.webp\", \"caption\": \"\", \"page\": 2, \"index\": 21, \"width\": 720, \"height\": 960}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-a971f1116ac1b4514b410ee0/fig-022.webp\", \"caption\": \"\", \"page\": 2, \"index\": 22, \"width\": 720, \"height\": 960}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-a971f1116ac1b4514b410ee0/fig-023.webp\", \"caption\": \"\", \"page\": 2, \"index\": 23, \"width\": 720, \"height\": 960}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-a971f1116ac1b4514b410ee0/fig-024.webp\", \"caption\": \"\", \"page\": 2, \"index\": 24, \"width\": 720, \"height\": 960}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-a971f1116ac1b4514b410ee0/fig-025.webp\", \"caption\": \"\", \"page\": 2, \"index\": 25, \"width\": 720, \"height\": 960}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-a971f1116ac1b4514b410ee0/fig-026.webp\", \"caption\": \"\", \"page\": 5, \"index\": 26, \"width\": 372, \"height\": 371}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-a971f1116ac1b4514b410ee0/fig-027.webp\", \"caption\": \"\", \"page\": 5, \"index\": 27, \"width\": 379, \"height\": 369}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-a971f1116ac1b4514b410ee0/fig-028.webp\", \"caption\": \"\", \"page\": 5, \"index\": 28, \"width\": 362, \"height\": 351}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-a971f1116ac1b4514b410ee0/fig-029.webp\", \"caption\": \"\", \"page\": 5, \"index\": 29, \"width\": 362, \"height\": 350}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-a971f1116ac1b4514b410ee0/fig-030.webp\", \"caption\": \"\", \"page\": 5, \"index\": 30, \"width\": 360, \"height\": 480}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-a971f1116ac1b4514b410ee0/fig-031.webp\", \"caption\": \"\", \"page\": 7, \"index\": 31, \"width\": 720, \"height\": 960}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-a971f1116ac1b4514b410ee0/fig-032.webp\", \"caption\": \"\", \"page\": 7, \"index\": 32, \"width\": 720, \"height\": 960}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-a971f1116ac1b4514b410ee0/fig-033.webp\", \"caption\": \"\", \"page\": 7, \"index\": 33, \"width\": 720, \"height\": 960}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-a971f1116ac1b4514b410ee0/fig-034.webp\", \"caption\": \"\", \"page\": 7, \"index\": 34, \"width\": 720, \"height\": 960}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-a971f1116ac1b4514b410ee0/fig-035.webp\", \"caption\": \"\", \"page\": 11, \"index\": 35, \"width\": 360, \"height\": 480}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-a971f1116ac1b4514b410ee0/fig-036.webp\", \"caption\": \"\", \"page\": 11, \"index\": 36, \"width\": 720, \"height\": 960}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-a971f1116ac1b4514b410ee0/fig-037.webp\", \"caption\": \"\", \"page\": 11, \"index\": 37, \"width\": 720, \"height\": 960}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-a971f1116ac1b4514b410ee0/fig-038.webp\", \"caption\": \"\", \"page\": 11, \"index\": 38, \"width\": 720, \"height\": 960}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-a971f1116ac1b4514b410ee0/fig-039.webp\", \"caption\": \"\", \"page\": 11, \"index\": 39, \"width\": 368, \"height\": 831}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-a971f1116ac1b4514b410ee0/fig-040.webp\", \"caption\": \"\", \"page\": 11, \"index\": 40, \"width\": 370, \"height\": 833}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-a971f1116ac1b4514b410ee0/fig-041.webp\", \"caption\": \"\", \"page\": 11, \"index\": 41, \"width\": 360, \"height\": 480}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-a971f1116ac1b4514b410ee0/fig-042.webp\", \"caption\": \"\", \"page\": 11, \"index\": 42, \"width\": 330, \"height\": 365}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-a971f1116ac1b4514b410ee0/fig-043.webp\", \"caption\": \"\", \"page\": 11, \"index\": 43, \"width\": 684, \"height\": 680}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-a971f1116ac1b4514b410ee0/fig-044.webp\", \"caption\": \"\", \"page\": 11, \"index\": 44, \"width\": 360, \"height\": 480}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-a971f1116ac1b4514b410ee0/fig-045.webp\", \"caption\": \"\", \"page\": 11, \"index\": 45, \"width\": 498, \"height\": 626}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-a971f1116ac1b4514b410ee0/fig-046.webp\", \"caption\": \"\", \"page\": 11, \"index\": 46, \"width\": 360, \"height\": 480}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-a971f1116ac1b4514b410ee0/fig-047.webp\", \"caption\": \"\", \"page\": 11, \"index\": 47, \"width\": 394, \"height\": 450}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-a971f1116ac1b4514b410ee0/fig-048.webp\", \"caption\": \"\", \"page\": 11, \"index\": 48, \"width\": 360, \"height\": 480}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-a971f1116ac1b4514b410ee0/fig-049.webp\", \"caption\": \"\", \"page\": 11, \"index\": 49, \"width\": 360, \"height\": 480}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-a971f1116ac1b4514b410ee0/fig-050.webp\", \"caption\": \"\", \"page\": 11, \"index\": 50, \"width\": 352, \"height\": 452}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-a971f1116ac1b4514b410ee0/fig-051.webp\", \"caption\": \"\", \"page\": 11, \"index\": 51, \"width\": 360, \"height\": 480}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-a971f1116ac1b4514b410ee0/fig-052.webp\", \"caption\": \"\", \"page\": 11, \"index\": 52, \"width\": 360, \"height\": 480}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-a971f1116ac1b4514b410ee0/fig-053.webp\", \"caption\": \"\", \"page\": 11, \"index\": 53, \"width\": 720, \"height\": 960}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-a971f1116ac1b4514b410ee0/fig-054.webp\", \"caption\": \"\", \"page\": 11, \"index\": 54, \"width\": 720, \"height\": 960}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-a971f1116ac1b4514b410ee0/fig-055.webp\", \"caption\": \"\", \"page\": 11, \"index\": 55, \"width\": 467, \"height\": 960}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-a971f1116ac1b4514b410ee0/fig-056.webp\", \"caption\": \"\", \"page\": 11, \"index\": 56, \"width\": 467, \"height\": 960}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-a971f1116ac1b4514b410ee0/fig-057.webp\", \"caption\": \"\", \"page\": 11, \"index\": 57, \"width\": 360, \"height\": 480}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-a971f1116ac1b4514b410ee0/fig-058.webp\", \"caption\": \"\", \"page\": 11, \"index\": 58, \"width\": 668, \"height\": 648}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-a971f1116ac1b4514b410ee0/fig-059.webp\", \"caption\": \"\", \"page\": 11, \"index\": 59, \"width\": 768, \"height\": 498}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-a971f1116ac1b4514b410ee0/fig-060.webp\", \"caption\": \"\", \"page\": 11, \"index\": 60, \"width\": 663, \"height\": 560}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-a971f1116ac1b4514b410ee0/fig-061.webp\", \"caption\": \"\", \"page\": 11, \"index\": 61, \"width\": 360, \"height\": 480}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-a971f1116ac1b4514b410ee0/fig-062.webp\", \"caption\": \"\", \"page\": 11, \"index\": 62, \"width\": 360, \"height\": 480}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-a971f1116ac1b4514b410ee0/fig-063.webp\", \"caption\": \"\", \"page\": 11, \"index\": 63, \"width\": 360, \"height\": 480}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-a971f1116ac1b4514b410ee0/fig-064.webp\", \"caption\": \"\", \"page\": 11, \"index\": 64, \"width\": 360, \"height\": 480}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-a971f1116ac1b4514b410ee0/fig-065.webp\", \"caption\": \"\", \"page\": 11, \"index\": 65, \"width\": 360, \"height\": 480}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-a971f1116ac1b4514b410ee0/fig-066.webp\", \"caption\": \"\", \"page\": 11, \"index\": 66, \"width\": 358, \"height\": 480}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-a971f1116ac1b4514b410ee0/fig-067.webp\", \"caption\": \"\", \"page\": 11, \"index\": 67, \"width\": 1920, \"height\": 1080}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-a971f1116ac1b4514b410ee0/fig-068.webp\", \"caption\": \"\", \"page\": 11, \"index\": 68, \"width\": 360, \"height\": 480}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-a971f1116ac1b4514b410ee0/fig-069.webp\", \"caption\": \"\", \"page\": 11, \"index\": 69, \"width\": 1920, \"height\": 1080}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-a971f1116ac1b4514b410ee0/fig-070.webp\", \"caption\": \"\", \"page\": 11, \"index\": 70, \"width\": 1920, \"height\": 1080}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-a971f1116ac1b4514b410ee0/fig-071.webp\", \"caption\": \"\", \"page\": 11, \"index\": 71, \"width\": 1920, \"height\": 1080}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-a971f1116ac1b4514b410ee0/fig-072.webp\", \"caption\": \"\", \"page\": 11, \"index\": 72, \"width\": 1920, \"height\": 1080}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-a971f1116ac1b4514b410ee0/fig-073.webp\", \"caption\": \"\", \"page\": 11, \"index\": 73, \"width\": 1920, \"height\": 1080}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-a971f1116ac1b4514b410ee0/fig-074.webp\", \"caption\": \"\", \"page\": 11, \"index\": 74, \"width\": 1920, \"height\": 1080}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-a971f1116ac1b4514b410ee0/fig-075.webp\", \"caption\": \"\", \"page\": 11, \"index\": 75, \"width\": 1920, \"height\": 1080}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-a971f1116ac1b4514b410ee0/fig-076.webp\", \"caption\": \"\", \"page\": 11, \"index\": 76, \"width\": 960, \"height\": 540}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-a971f1116ac1b4514b410ee0/fig-077.webp\", \"caption\": \"\", \"page\": 11, \"index\": 77, \"width\": 1920, \"height\": 1080}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-a971f1116ac1b4514b410ee0/fig-078.webp\", \"caption\": \"\", \"page\": 11, \"index\": 78, \"width\": 960, \"height\": 540}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-a971f1116ac1b4514b410ee0/fig-079.webp\", \"caption\": \"\", \"page\": 11, \"index\": 79, \"width\": 1920, \"height\": 1080}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-a971f1116ac1b4514b410ee0/fig-080.webp\", \"caption\": \"\", \"page\": 11, \"index\": 80, \"width\": 1920, \"height\": 1080}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-a971f1116ac1b4514b410ee0/fig-081.webp\", \"caption\": \"\", \"page\": 11, \"index\": 81, \"width\": 1920, \"height\": 1080}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-a971f1116ac1b4514b410ee0/fig-082.webp\", \"caption\": \"\", \"page\": 11, \"index\": 82, \"width\": 1920, \"height\": 1080}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-a971f1116ac1b4514b410ee0/fig-083.webp\", \"caption\": \"\", \"page\": 12, \"index\": 83, \"width\": 360, \"height\": 480}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-a971f1116ac1b4514b410ee0/fig-084.webp\", \"caption\": \"\", \"page\": 12, \"index\": 84, \"width\": 360, \"height\": 480}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-a971f1116ac1b4514b410ee0/fig-085.webp\", \"caption\": \"\", \"page\": 12, \"index\": 85, \"width\": 360, \"height\": 480}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-a971f1116ac1b4514b410ee0/fig-086.webp\", \"caption\": \"\", \"page\": 12, \"index\": 86, \"width\": 360, \"height\": 480}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-a971f1116ac1b4514b410ee0/fig-087.webp\", \"caption\": \"\", \"page\": 12, \"index\": 87, \"width\": 360, \"height\": 480}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-a971f1116ac1b4514b410ee0/fig-088.webp\", \"caption\": \"\", \"page\": 12, \"index\": 88, \"width\": 360, \"height\": 480}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-a971f1116ac1b4514b410ee0/fig-089.webp\", \"caption\": \"\", \"page\": 12, \"index\": 89, \"width\": 360, \"height\": 480}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-a971f1116ac1b4514b410ee0/fig-090.webp\", \"caption\": \"\", \"page\": 12, \"index\": 90, \"width\": 360, \"height\": 480}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-a971f1116ac1b4514b410ee0/fig-091.webp\", \"caption\": \"\", \"page\": 13, \"index\": 91, \"width\": 960, \"height\": 540}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-a971f1116ac1b4514b410ee0/fig-092.webp\", \"caption\": \"\", \"page\": 13, \"index\": 92, \"width\": 1920, \"height\": 1080}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-a971f1116ac1b4514b410ee0/fig-093.webp\", \"caption\": \"\", \"page\": 13, \"index\": 93, \"width\": 1920, \"height\": 1080}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-a971f1116ac1b4514b410ee0/fig-094.webp\", \"caption\": \"\", \"page\": 13, \"index\": 94, \"width\": 360, \"height\": 480}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-a971f1116ac1b4514b410ee0/fig-095.webp\", \"caption\": \"\", \"page\": 14, \"index\": 95, \"width\": 360, \"height\": 480}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-a971f1116ac1b4514b410ee0/fig-096.webp\", \"caption\": \"\", \"page\": 14, \"index\": 96, \"width\": 360, \"height\": 480}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-a971f1116ac1b4514b410ee0/fig-097.webp\", \"caption\": \"\", \"page\": 14, \"index\": 97, \"width\": 360, \"height\": 480}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-a971f1116ac1b4514b410ee0/fig-098.webp\", \"caption\": \"\", \"page\": 14, \"index\": 98, \"width\": 360, \"height\": 480}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-a971f1116ac1b4514b410ee0/fig-099.webp\", \"caption\": \"\", \"page\": 14, \"index\": 99, \"width\": 720, \"height\": 960}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-a971f1116ac1b4514b410ee0/fig-100.webp\", \"caption\": \"\", \"page\": 14, \"index\": 100, \"width\": 720, \"height\": 960}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-a971f1116ac1b4514b410ee0/fig-101.webp\", \"caption\": \"\", \"page\": 14, \"index\": 101, \"width\": 720, \"height\": 960}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-a971f1116ac1b4514b410ee0/fig-102.webp\", \"caption\": \"\", \"page\": 14, \"index\": 102, \"width\": 720, \"height\": 960}]"
motivation: 现有方法依赖二维先验，初始点易过拟合可见表面，难以重建一致的360度动态几何。
method: 提出免扩散的4DGS360，采用三维原生初始化与AnchorTAP3D三维跟踪器，利用置信二维轨迹点作为锚点抑制漂移。
result: 在遮挡区域保持几何一致，实现连贯的360度四维重建。
conclusion: 为单目视频下动态物体的全视角重建提供了可靠初始化与优化方案。
---

## Abstract
We introduce 4DGS360, a di!usion-free framework for 360→dynamic object reconstruction from casual monocular video. Existingmethods often fail to reconstruct consistent 360→ geometry, as their heavyreliance on 2D-native priors causes initial points to overfit to visible sur-face in each training view. 4DGS360 addresses this challenge through anadvanced 3D-native initialization that mitigates the geometric ambigu-ity of occluded regions. Our proposed 3D tracker, AnchorTAP3D, pro-duces reinforced 3D point trajectories by leveraging confident 2D trackpoints as anchors, suppressing drift and providing reliable initializationthat preserves geometry in occluded regions. This initialization, com-bined with optimization, yields coherent 360→ 4D reconstructions. Wefurther present iPhone360, a new benchmark where test cameras areplaced up to 135→ apart from training views, enabling 360→ evaluationthat existing datasets cannot provide. Experiments show that 4DGS360achieves state-of-the-art performance on the iPhone360, iPhone, andDAVIS datasets, both qualitatively and quantitatively. Project websiteat https://jaewon040.github.io/4dgs360/

---

## 论文详细总结（自动生成）

# 4DGS360 论文深度总结

## 1. 核心问题与整体含义

- **研究背景**：动态 3D 重建是计算机视觉的核心议题，在视频内容创作、VR/MR/AR 空间计算、3D 全息媒体等场景需求旺盛。其中，从"随手拍摄的单目视频"（casual monocular video）中重建，是最贴近真实采集条件、但也是高度病态（ill-posed）的设定——每帧仅有单一视角，缺少多视图立体线索。
- **核心痛点**：现有方法（如 MoSca、HiMoR）依赖预训练 2D 点跟踪模型建立跨帧对应关系，再结合深度图将 2D 轨迹"提升"（lift）到 3D 以初始化高斯点。然而深度图只能提供当前帧**可见表面**的深度，导致被遮挡轨迹点的 3D 位置存在歧义，初始几何在每个时间步都**过拟合于可见表面**。
- **后果**：这种不完整的初始几何在后续优化中无法被恢复，即使某些区域在其他帧中可见，模型仍无法重建，最终在极端新视角（如偏离训练视角 > 90°）下出现几何崩坏。
- **整体含义**：论文主张通过**3D 原生的、遮挡感知的初始化**来打破"2D 先验依赖 → 几何过拟合"的恶性循环，从而实现真正一致的 360° 动态物体重建；同时指出并弥补了现有数据集无法评估 360° 重建的空白。

## 2. 方法论

### 2.1 核心思想
- 提出免扩散（diffusion-free）框架 **4DGS360**，关键在于用 **AnchorTAP3D**（Anchor-guided Tracking Any Point in 3D）提供可靠的、几何一致的 3D 轨迹初始化，进而释放后续优化（尤其是 ARAP 正则）的全部潜力。

### 2.2 动态高斯表示（预备知识）
- 场景由一组规范空间（canonical space）中的各向异性 3D 高斯 $G(\mu, \Sigma, \vartheta, c)$ 表示，通过时间相关变换 $T_t=[R_t|t_t]\in SE(3)$ 变形：
  - $G_t = G(R_t\mu_0 + t_t,\ R_t\Sigma_0 R_t^\top,\ \vartheta, c)$
- 变形场沿用 **HiMoR** 的层级结构：以节点树编码运动，每个高斯由其 K 近邻叶节点运动插值得到 $T_t=\sum w_k M_k$；每个节点运动又由父节点共享的运动基线性组合 $M_t=\sum_m v_m B_{m,t}$。高层节点捕捉全局平滑运动，深层节点细化局部形变。
- 渲染采用深度排序的 alpha 混合，实现可微光栅化。

### 2.3 AnchorTAP3D（关键技术细节）
以置信 2D 轨迹点作为**锚点**来条件化 3D 跟踪器，无需额外训练，流程如下：

1. **2D 跟踪**：2D 跟踪器 $P_{2D}$ 对查询点 $p_t$ 预测目标帧对应点与置信度：$(p_{t'}, c_{t'}) = P_{2D}(p_t, I)$。
2. **提升到 3D**：用目标帧深度图与相机参数反投影：$x^{2D}_{t'} = \pi^{-1}_{t'}(p_{t'}, D_{t'}, \varepsilon_{t'})$。
3. **置信掩码过滤**：仅保留 $c_{t'}>\varsigma$ 的点作为可信锚点，剔除被遮挡的低置信点。
4. **滑窗锚点集合**：在长度 $L=16$（相邻窗重叠 8 帧）的时序窗口内，收集高置信 2D 轨迹提升得到的 3D 锚点集合 $\mathcal{X}^A_{w(t,t')}$。
5. **锚点条件化 3D 跟踪**：$(x^{\text{Anchor}}_{t'}, v_{t'}) = P_{3D}(p_t, I, D, \omega, \mathcal{X}^A_{w(t,t')})$。
- **效果**：与仅传播单一查询点的传统 3D 跟踪器不同，多锚点提供时空约束，抑制误差漂移，且锚点对深度/标定噪声相对不敏感，长期稳定性更强。

### 2.4 初始化流程
- 从 T 个查询时刻的 3D 轨迹中随机采样 N 条轨迹定义高斯基元；将高斯可见数最多的帧设为规范帧。
- 按时间速度对轨迹做 **k-means** 聚类为 B 组，簇内用 **Procrustes 对齐**估计帧间刚体变换，得到初始运动基 $\{B_i\}$。
- 节点初始化采用加权随机采样（权重结合运动幅度与空间密度），兼顾高动态区域与空间覆盖。
- **关键差异**：以往方法因无法推断遮挡点的 3D 位置而丢弃不可见点；AnchorTAP3D 能推断遮挡区域的合理 3D 位置，使运动基能完整捕捉全局物体动力学。

### 2.5 优化方法
- **刚性正则（广义 ARAP）**：对同一局部刚性簇内的节点对 $(i,j)$，约束任意帧 $t,t'$ 间的成对距离一致性与相对局部变换一致性：
  - $\mathcal{L}_{arap} = w_1\sum\|\|x^t_i-x^t_j\|_2-\|x^{t'}_i-x^{t'}_j\|_2\| + w_2\sum\|T^{t-1}_j(x^t_i)-T^{t'-1}_j(x^{t'}_i)\|_2$
  - 作者强调：该正则在以往方法中因初始几何被破坏而失效，本方法修复初始化后其才能真正发挥作用。
- **渲染正则**：RGB 损失（含 D-SSIM、LPIPS）、掩码紧致损失 $\mathcal{L}_{mask}$、深度一致性损失 $\mathcal{L}_{depth}$、2D 跟踪损失 $\mathcal{L}_{2dtrack}$。
- **总损失**：$\mathcal{L}_{total} = \omega_{rgb}\mathcal{L}_{rgb}+\omega_{mask}\mathcal{L}_{mask}+\omega_{depth}\mathcal{L}_{depth}+\omega_{2dtrack}\mathcal{L}_{2dtrack}+\omega_{arap}\mathcal{L}_{arap}$。

## 3. 实验设计

### 3.1 数据集与 Benchmark
- **iPhone360（本文新建）**：6 个场景（block2、goat、jacket、jelly、pull-up、walk-around），单手持相机连续拍摄（无相机瞬移），测试相机与训练视角相距 **70°–135°**，支持极端新视角下的 360° 评估；用 LiDAR 度量深度做尺度/平移校正，相机参数来自传感器。
- **iPhone 数据集**：5 个场景（apple、block、paper-windmill、spin、teddy），单目设定但训练/测试相机间距有限（< 45°）。
- **DAVIS 数据集**：快速运动物体，无 GT 相机参数与深度图，更贴近真实场景（in-the-wild）。

### 3.2 评价指标
- **感知指标**：CLIP-I（渲染与 GT 的 CLIP 相似度）、CLIP-T（间隔 5 帧渲染帧之间的时序一致性）、LPIPS（AlexNet 特征）。
- **像素级指标**：PSNR、SSIM（论文指出在单目大视角外推下像素级指标与感知质量错位，故两者并报）。
- iPhone360 上因极端视角下背景含大量空白，评测限定在以 GT 动态物体掩码为中心扩展的边界框内进行。

### 3.3 对比方法
- 动态 4D 重建：**MoSca**、**HiMoR**、**SoM（Shape of Motion）**、**Deformable 3DGS**、**Marbles**
- NeRF 系：**T-NeRF**、**HyperNeRF**
- 扩散先验组合：**DIFIX3D+**（用于验证本方法作为扩散方法的更强起点）

## 4. 资源与算力

- **论文正文中未明确说明**使用的 GPU 型号、数量、训练时长、显存占用或总计算量。
- 仅提及训练使用 Adam 优化器（参考文献 [18]），以及 AnchorTAP3D 的时序窗口长度为 L=16（重叠 8 帧）等超参。
- 作者提到扩散类方法需要大量训练生成模型的计算开销（作为对比动机），但未给出自身方法的算力统计。
- **结论**：算力信息缺失，无法评估方法的训练成本与可复现性开销。

## 5. 实验数量与充分性

### 实验规模概览
| 实验类型 | 数量/范围 |
|---|---|
| 主实验数据集 | 3 个（iPhone360、iPhone、DAVIS） |
| iPhone360 定量 | 6 个场景 × 3 个指标（CLIP-I/CLIP-T/LPIPS） |
| iPhone 定量 | 5 个场景 × 3 个指标，含 7 个基线方法对比 |
| 像素级评测 | iPhone 与 iPhone360 各一组 PSNR/SSIM |
| 消融实验 | 2 个变体（w/o 3D init、w/o Anchor），2 个场景（walk-around、jelly），定性为主 |
| 扩散组合实验 | 与 DIFIX3D+ 结合，1 组对比 |
| 定性对比 | iPhone360 新视角、bullet-time、iPhone 极端视角、DAVIS in-the-wild |

### 充分性与公平性评价
- **优点**：覆盖合成/真实、单目/野外、普通/极端新视角等多种条件；同时报告感知与像素指标，避免单一指标的误导；消融设计针对性明确（区分"2D 提升初始化"与"朴素 3D 跟踪初始化"）。
- **不足**：
  - 消融实验仅提供**定性结果**，缺少定量的消融指标表格，说服力受限。
  - 消融仅在 2 个场景上验证，样本偏少。
  - iPhone360 上 LPIPS 在 Jelly 场景（0.3538 vs HiMoR 0.3539）和 CLIP-T 在 Goat/Jelly 场景（Ours 反而略低）出现少量劣于基线的情况，论文未做深入分析。
  - 所有指标均在物体掩码区域内计算，背景重建质量未被评估。

## 6. 主要结论与发现

1. **初始化是瓶颈所在**：现有单目 4D 重建失败的根本原因是 2D 提升式初始化导致的遮挡区域几何歧义，而非优化策略本身；修复初始化后 ARAP 正则才能按预期生效。
2. **AnchorTAP3D 有效**：以高置信 2D 轨迹为锚点条件化 3D 跟踪，能显著抑制长期误差漂移，优于纯 2D 提升与朴素 3D 跟踪（TAPIP3D）。
3. **SOTA 性能**：在 iPhone360、iPhone、DAVIS 三个数据集上，无论定性还是定量均取得最优结果；iPhone 数据集上平均 CLIP-I 达 0.9015、LPIPS 降至 0.3877，均优于 HiMoR 等基线。
4. **数据集贡献**：iPhone360 首次提供 70°–135° 大视角差的单目动态物体 360° 评测基准。
5. **与扩散互补**：本方法保持的几何使其可作为扩散先验（DIFIX3D+）的更优起点，优于其他基线组合。

## 7. 优点

- **问题定位精准**：清楚指出现有方法失败源于"初始化阶段的遮挡几何歧义"，并给出可验证的因果解释（优化无法挽救损坏的初始化）。
- **方法免训练、可插拔**：AnchorTAP3D 无需额外训练，即插即用地整合 2D 跟踪的鲁棒性与 3D 跟踪的几何理解，工程上简洁高效。
- **数据贡献实在**：iPhone360 填补了现有数据集（HyperNeRF、Nerfies、iPhone）视角差不足的空白，且遵循真实单目采集流程，具有独立价值。
- **评测设计审慎**：同时报告感知指标与像素指标，并解释为何在大外推设定下像素指标会失真；针对背景空白问题设计掩码边界框评测协议。
- **验证维度丰富**：涵盖定量、定性、bullet-time 360° 渲染、in-the-wild、扩散组合、初始化消融等多种视角。

## 8. 不足与局限

- **依赖预训练模型**：AnchorTAP3D 虽优于朴素应用，但整体性能仍受限于预训练 2D/3D 跟踪模型的能力上限，无自有训练或微调。
- **背景无法合成**：若极端视角下的背景在输入视频中完全不可见，方法无法合成，需依赖扩散先验补足（作者将其列为未来工作）。
- **像素级精度仍弱**：在 iPhone360 的大外推设定下 PSNR（11.34）与 SSIM（0.7012）绝对值很低，像素级重建精度提升空间明显。
- **算力信息缺失**：未报告 GPU 型号、数量、训练时长，影响成本评估与复现性判断。
- **消融不够充分**：消融仅定性、仅 2 个场景，缺少各损失项（如 $\mathcal{L}_{arap}$、$\mathcal{L}_{2dtrack}$）的独立消融与超参敏感性分析。
- **评测范围受限**：iPhone360 仅 6 个场景，规模偏小；评测集中于物体前景掩码区域，未覆盖背景与全局场景质量。
- **个别指标非单调占优**：部分场景的 CLIP-T 或 LPIPS 略逊于 HiMoR，论文未对这类反例做出解释。
- **数据集自建自评风险**：iPhone360 由作者自建并用于主要评测，虽协议透明，但缺少第三方独立验证。

（完）
