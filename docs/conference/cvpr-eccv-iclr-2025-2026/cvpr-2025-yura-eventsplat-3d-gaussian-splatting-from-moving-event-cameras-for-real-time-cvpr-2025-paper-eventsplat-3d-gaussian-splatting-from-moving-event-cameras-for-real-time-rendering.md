---
title: "EventSplat: 3D Gaussian Splatting from Moving Event Cameras for Real-time Rendering"
title_zh: EventSplat：基于移动事件相机的三维高斯泼溅实时渲染
authors: "Yura, Toshiya, Mirzaei, Ashkan, Gilitschenski, Igor"
date: 2025
publication_date: 2025
publication_date_precision: year
publication_date_source: conference year only; exact release date unverified
publication_date_kind: unknown
pdf: "https://openaccess.thecvf.com/content/CVPR2025/papers/Yura_EventSplat_3D_Gaussian_Splatting_from_Moving_Event_Cameras_for_Real-time_CVPR_2025_paper.pdf"
tags: ["query:dr"]
score: 6.0
evidence: 基于移动事件相机的高斯泼溅实时渲染
tldr: 在快速相机运动下进行新视角合成具有挑战性，事件相机凭借高时间分辨率与高动态范围提供了解决契机。本文提出EventSplat，利用事件相机数据结合高斯泼溅进行新视角合成，借助事件转视频模型提供的先验初始化优化过程，并用样条插值获得沿相机轨迹的高质量位姿。实验表明该方法提升了快速运动相机的重建质量，克服了事件NeRF方法的计算局限，实现了实时渲染。
source: CVPR-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-yura-eventsplat-3d-gaussian-splatting-from-moving-event-cameras-for-real-time-cvpr-2025-paper/fig-001.webp\", \"caption\": \"\", \"page\": 2, \"index\": 1, \"width\": 800, \"height\": 800}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-yura-eventsplat-3d-gaussian-splatting-from-moving-event-cameras-for-real-time-cvpr-2025-paper/fig-002.webp\", \"caption\": \"\", \"page\": 2, \"index\": 2, \"width\": 800, \"height\": 800}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-yura-eventsplat-3d-gaussian-splatting-from-moving-event-cameras-for-real-time-cvpr-2025-paper/fig-003.webp\", \"caption\": \"\", \"page\": 2, \"index\": 3, \"width\": 800, \"height\": 800}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-yura-eventsplat-3d-gaussian-splatting-from-moving-event-cameras-for-real-time-cvpr-2025-paper/fig-004.webp\", \"caption\": \"\", \"page\": 2, \"index\": 4, \"width\": 640, \"height\": 480}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-yura-eventsplat-3d-gaussian-splatting-from-moving-event-cameras-for-real-time-cvpr-2025-paper/fig-005.webp\", \"caption\": \"\", \"page\": 2, \"index\": 5, \"width\": 640, \"height\": 480}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-yura-eventsplat-3d-gaussian-splatting-from-moving-event-cameras-for-real-time-cvpr-2025-paper/fig-006.webp\", \"caption\": \"\", \"page\": 2, \"index\": 6, \"width\": 640, \"height\": 480}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-yura-eventsplat-3d-gaussian-splatting-from-moving-event-cameras-for-real-time-cvpr-2025-paper/fig-007.webp\", \"caption\": \"\", \"page\": 2, \"index\": 7, \"width\": 640, \"height\": 480}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-yura-eventsplat-3d-gaussian-splatting-from-moving-event-cameras-for-real-time-cvpr-2025-paper/fig-008.webp\", \"caption\": \"\", \"page\": 2, \"index\": 8, \"width\": 800, \"height\": 800}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-yura-eventsplat-3d-gaussian-splatting-from-moving-event-cameras-for-real-time-cvpr-2025-paper/fig-009.webp\", \"caption\": \"\", \"page\": 2, \"index\": 9, \"width\": 438, \"height\": 408}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-yura-eventsplat-3d-gaussian-splatting-from-moving-event-cameras-for-real-time-cvpr-2025-paper/fig-010.webp\", \"caption\": \"\", \"page\": 4, \"index\": 10, \"width\": 524, \"height\": 487}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-yura-eventsplat-3d-gaussian-splatting-from-moving-event-cameras-for-real-time-cvpr-2025-paper/fig-011.webp\", \"caption\": \"\", \"page\": 6, \"index\": 11, \"width\": 409, \"height\": 409}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-yura-eventsplat-3d-gaussian-splatting-from-moving-event-cameras-for-real-time-cvpr-2025-paper/fig-012.webp\", \"caption\": \"\", \"page\": 6, \"index\": 12, \"width\": 409, \"height\": 409}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-yura-eventsplat-3d-gaussian-splatting-from-moving-event-cameras-for-real-time-cvpr-2025-paper/fig-013.webp\", \"caption\": \"\", \"page\": 6, \"index\": 13, \"width\": 409, \"height\": 409}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-yura-eventsplat-3d-gaussian-splatting-from-moving-event-cameras-for-real-time-cvpr-2025-paper/fig-014.webp\", \"caption\": \"\", \"page\": 6, \"index\": 14, \"width\": 450, \"height\": 450}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-yura-eventsplat-3d-gaussian-splatting-from-moving-event-cameras-for-real-time-cvpr-2025-paper/fig-015.webp\", \"caption\": \"\", \"page\": 6, \"index\": 15, \"width\": 450, \"height\": 450}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-yura-eventsplat-3d-gaussian-splatting-from-moving-event-cameras-for-real-time-cvpr-2025-paper/fig-016.webp\", \"caption\": \"\", \"page\": 6, \"index\": 16, \"width\": 450, \"height\": 450}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-yura-eventsplat-3d-gaussian-splatting-from-moving-event-cameras-for-real-time-cvpr-2025-paper/fig-017.webp\", \"caption\": \"\", \"page\": 6, \"index\": 17, \"width\": 450, \"height\": 450}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-yura-eventsplat-3d-gaussian-splatting-from-moving-event-cameras-for-real-time-cvpr-2025-paper/fig-018.webp\", \"caption\": \"\", \"page\": 6, \"index\": 18, \"width\": 450, \"height\": 450}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-yura-eventsplat-3d-gaussian-splatting-from-moving-event-cameras-for-real-time-cvpr-2025-paper/fig-019.webp\", \"caption\": \"\", \"page\": 6, \"index\": 19, \"width\": 450, \"height\": 450}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-yura-eventsplat-3d-gaussian-splatting-from-moving-event-cameras-for-real-time-cvpr-2025-paper/fig-020.webp\", \"caption\": \"\", \"page\": 6, \"index\": 20, \"width\": 450, \"height\": 450}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-yura-eventsplat-3d-gaussian-splatting-from-moving-event-cameras-for-real-time-cvpr-2025-paper/fig-021.webp\", \"caption\": \"\", \"page\": 6, \"index\": 21, \"width\": 450, \"height\": 450}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-yura-eventsplat-3d-gaussian-splatting-from-moving-event-cameras-for-real-time-cvpr-2025-paper/fig-022.webp\", \"caption\": \"\", \"page\": 6, \"index\": 22, \"width\": 451, \"height\": 451}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-yura-eventsplat-3d-gaussian-splatting-from-moving-event-cameras-for-real-time-cvpr-2025-paper/fig-023.webp\", \"caption\": \"\", \"page\": 8, \"index\": 23, \"width\": 572, \"height\": 429}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-yura-eventsplat-3d-gaussian-splatting-from-moving-event-cameras-for-real-time-cvpr-2025-paper/fig-024.webp\", \"caption\": \"\", \"page\": 8, \"index\": 24, \"width\": 572, \"height\": 429}]"
motivation: 快速相机运动下的新视角合成面临挑战，事件相机具备高时间分辨率与高动态范围优势。
method: 提出事件相机高斯泼溅方法，借助事件转视频模型初始化并用样条插值获取高质量位姿。
result: 提升了快速运动相机的重建质量，克服了事件NeRF方法的计算局限并实现实时渲染。
conclusion: 为事件相机下的实时新视角合成提供了高效方案。
---

## Abstract
We introduce a method for using event camera data in novel view synthesis via Gaussian Splatting. Event cameras offer exceptional temporal resolution and a high dynamic range. Leveraging these capabilities allows us to effectively address the novel view synthesis challenge in the presence of fast camera motion. For initialization of the optimization process, our approach uses prior knowledge encoded in an event-to-video model. We also use spline interpolation for obtaining high quality poses along the event camera trajectory. This enhances the reconstruction quality from fast-moving cameras while overcoming the computational limitations traditionally associated with event-based Neural Radiance Field (NeRF) methods. Our experimental evaluation demonstrates that our results achieve higher visual fidelity and better performance than existing event-based NeRF approaches while being an order of magnitude faster to render.

---

## 论文详细总结（自动生成）

## 1. 核心问题与整体含义

- **研究动机**：事件相机具有高时间分辨率、低延迟、高动态范围和低功耗等优势，适合快速相机运动、强运动模糊或困难光照下的视觉任务。
- **核心问题**：传统新视角合成依赖 RGB 图像监督；事件 NeRF 虽能利用事件数据，但体渲染采样成本高，难以实时。3D Gaussian Splatting（3DGS）可实时渲染，但原始 3DGS 需要 RGB 图像监督，难以直接使用事件流。
- **整体含义**：本文提出 EventSplat，将移动事件相机数据与 3DGS 结合，用事件累积信号监督高斯优化，实现静态场景下高质量、实时的的新视角合成，尤其适用于传统相机失效的场景。

## 2. 方法论

- **核心思想**：用事件累积图近似对数强度变化，并通过 3DGS 栅格化两个相机位姿下的视图，构造 log-difference 图像进行监督，从而让 3DGS 能从事件数据中学习场景表示。
- **事件建模**：
  - 事件表示为 \(e=(t,x,y,p)\)，其中 \(t\) 为时间戳，\((x,y)\) 为像素坐标，\(p\in\{-1,1\}\) 为极性。
  - 当像素当前 log 强度与最近事件时 log 强度差超过阈值 \(\Delta\) 时触发事件。
  - 目标建模为时间区间内 log 强度变化积分：\(E(a,b)=\int_a^b \log(I'(t))dt\)。
- **事件累积**：
  - 随机采样子轨迹起点和终点，长度约为总事件数的 1% 到 10%。
  - 累积 log 强度变化图 \(D_{x,y}=\sum p_k\Delta\)，作为事件相机对积分的近似。
- **训练视图生成与 Remosaicing**：
  - 对两个位姿 \(P_{kstart}\)、\(P_{kend}\) 分别用当前 3DGS 栅格化得到 RGB 视图。
  - 对颜色事件相机，执行 remosaicing，恢复 Bayer 模式，再取 log，得到 \(\hat L_1,\hat L_2\)。
  - 计算 log-difference 图像 \(\hat D=\hat L_2-\hat L_1\)，与事件累积图 \(D\) 计算损失。
- **事件到视频引导初始化**：
  - 使用预训练 event-to-video 模型从事件流生成图像，再经 SfM 得到初始点云/高斯位置。
  - 该初始化虽含噪声，但保留纹理和背景信息，优于随机初始化。
- **相机轨迹插值**：
  - 使用三次样条插值和球面三次样条插值，在稀疏或固定频率位姿之间估计高频相机轨迹，使事件可对应更准确的位姿。
- **损失函数**：
  - \(L=(1-\lambda)L_1+\lambda L_{SSIM}\)，结合重建与感知相似性。
  - 只在实际累积事件的像素处计算损失，并进行去畸变处理。

## 3. 实验设计

- **数据集/场景**：
  - **合成场景**：基于 ESIM 的 7 个合成场景，包括 chair、drums、ficus、hotdog、lego、materials、mic，白背景，含复杂结构和多样光照。
  - **真实场景**：
    - EDS 数据集序列：03_rocket_earth_dark、07_ziggy_and_fuzz_hdr、08_peanuts_running、11_all_characters、13_airplane。
    - TUM-VIE 数据集序列：mocap-1d-trans、mocap-desk2。
- **Benchmark 与指标**：
  - 使用 PSNR、SSIM、LPIPS（VGG16）评估新视角合成质量。
  - 同时比较渲染速度，单位毫秒。
  - 合成场景见表 1 与图 3；真实 EDS 场景见表 2；TUM-VIE 主要在 图 4 中定性展示。
- **对比方法**：
  - **Rob
