---
title: "Link to the Past: Temporal Propagation for Fast 3D Human Reconstruction from Monocular Video"
title_zh: 链接过去：面向单目视频快速三维人体重建的时间传播
authors: "Marchellus, Matthew, Noor, Nadhira, Park, In Kyu"
date: 2025
publication_date: 2025
publication_date_precision: year
publication_date_source: conference year only; exact release date unverified
publication_date_kind: unknown
pdf: "https://openaccess.thecvf.com/content/CVPR2025/papers/Marchellus_Link_to_the_Past_Temporal_Propagation_for_Fast_3D_Human_CVPR_2025_paper.pdf"
tags: ["query:dr"]
score: 8.0
evidence: 利用时间传播从单目视频快速重建三维人体
tldr: 针对单目视频三维穿衣人体重建速度与质量难以兼顾、逐视频优化耗时数分钟至数小时而无法实时的问题，本文提出TemPoFast3D，利用人体外观的时间连贯性减少冗余计算，将像素对齐重建网络改造为可插拔的快速方案。实验表明其在保持重建质量的同时大幅降低计算开销，实现单目视频的快速三维人体重建，为实时应用提供了可行路径。
source: CVPR-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-marchellus-link-to-the-past-temporal-propagation-for-fast-3d-human-cvpr-2025-paper/fig-001.webp\", \"caption\": \"\", \"page\": 1, \"index\": 1, \"width\": 5044, \"height\": 1324}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-marchellus-link-to-the-past-temporal-propagation-for-fast-3d-human-cvpr-2025-paper/fig-002.webp\", \"caption\": \"\", \"page\": 3, \"index\": 2, \"width\": 5510, \"height\": 3430}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-marchellus-link-to-the-past-temporal-propagation-for-fast-3d-human-cvpr-2025-paper/fig-003.webp\", \"caption\": \"\", \"page\": 4, \"index\": 3, \"width\": 2736, \"height\": 1298}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-marchellus-link-to-the-past-temporal-propagation-for-fast-3d-human-cvpr-2025-paper/fig-004.webp\", \"caption\": \"\", \"page\": 5, \"index\": 4, \"width\": 3168, \"height\": 2016}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-marchellus-link-to-the-past-temporal-propagation-for-fast-3d-human-cvpr-2025-paper/fig-005.webp\", \"caption\": \"\", \"page\": 7, \"index\": 5, \"width\": 3254, \"height\": 1882}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-marchellus-link-to-the-past-temporal-propagation-for-fast-3d-human-cvpr-2025-paper/fig-006.webp\", \"caption\": \"\", \"page\": 8, \"index\": 6, \"width\": 2412, \"height\": 1340}]"
motivation: 单目视频三维人体重建难以兼顾速度与质量，逐视频优化耗时数分钟至数小时，无法实时应用。
method: 提出TemPoFast3D，利用人体外观的时间连贯性减少冗余计算，将像素对齐重建网络改造为可插拔的快速方案。
result: 在保持重建质量的同时显著降低计算量，实现单目视频的快速三维穿衣人体重建。
conclusion: 表明时间传播可有效加速动态人体重建，为实时单目视频重建提供实用路径。
---

## Abstract
Fast 3D clothed human reconstruction from monocular video remains a significant challenge in computer vision, particularly in balancing computational efficiency with reconstruction quality. Current approaches are either focused on static image reconstruction but too computationally intensive, or achieve high quality through per-video optimization that requires minutes to hours of processing, making them unsuitable for real-time applications. To this end, we present TemPoFast3D, a novel method that leverages temporal coherency of human appearance to reduce redundant computation while maintaining reconstruction quality. Our approach is a "plug-and play" solution that uniquely transforms pixel-aligned reconstruction networks to handle continuous video streams by maintaining and refining a canonical appearance representation through efficient coordinate mapping. Extensive experiments demonstrate that TemPoFast3D matches or exceeds state-of-the-art methods across standard metrics while providing high-quality textured reconstruction across diverse pose and appearance, with a maximum speed of 12 FPS.

---

## 论文详细总结（自动生成）

## 1. 核心问题与整体含义

- **研究动机**：从单目视频快速重建三维穿衣人体在 VR、远程呈现、人机交互等场景中很重要，但现有方法难以兼顾速度与质量。
- **现有路线的问题**：
  - 单图像像素对齐方法（如 PIFu、PIFuHD、ECON、GTA、SIFU 等）重建细节好，但计算开销大，且主要面向静态图像。
  - 视频/头像方法（如 NeRF、Gaussian Splatting 类）质量高，但通常需要逐视频优化，耗时从数分钟到数小时，难以实时。
  - 已有实时方法往往牺牲质量、依赖额外输入（模板、多视角、深度）或缺乏真正 3D 纹理重建能力。
- **核心洞察**：视频中人体姿态快速变化，但身体形状与衣物几何在短时间内具有时间连贯性，因此不必每帧从零完整重建。
- **整体含义**：论文提出 TemPoFast3D，把像素对齐隐式重建与规范空间—姿态空间坐标映射结合，通过时间传播复用历史帧信息，实现单目视频快速 3D 人体重建，最高 12 FPS，并保持与 SOTA 可比的重建质量。

## 2. 方法论

- **总体思想**：
  - 将原本在姿态空间进行的像素对齐隐式函数查询，转移到**规范空间**中进行，并维护、细化一个跨帧一致的规范外观/形状表示。
  - 设计为“即插即用”框架，可替换特征提取网络和查询网络，兼容已有 SMPL 引导的像素对齐重建骨干，如 GTA、SIFU。
- **基础流程**：
  - 输入 RGB 帧，先提取图像特征图，并回归 SMPL 参数。
  - 传统 PIFu 类方法在姿态空间采样 3D 点，投影到图像得到像素对齐特征，再预测 occupancy 和颜色。
  - 本文改为在规范空间采样和推理，通过 SMPL 的线性混合蒙皮建立规范空间与姿态空间的**双向映射**。
- **坐标映射关键细节**：
  - 对规范坐标 \(x_c\)，通过 K 近邻搜索关联到 SMPL 规范顶点 \(s_c\)。
  - 将 SMPL 每顶点变换矩阵 \(T_s\) 传递给任意坐标，得到 \(T_x\)。
  - 姿态坐标可写为 \(x_p = T_x x_c\)，反向也可映射，从而把像素对齐特征用于规范空间推理。
- **体积边界过滤**：
  - 有效人体几何主要位于规范 SMPL 网格附近，因此用二值 mask 保留近邻体积，剔除无关查询点。
  - 作用是减少查询点数量，并避免外部规范点被错误映射到姿态人体内部造成伪影。
- **姿态网格生成与颜色推理**：
  - 在规范空间提取 occupancy 等值面，用 Marching Cubes 得到规范网格。
  - 再通过最近邻 SMPL 顶点变换将规范顶点变形到姿态空间，得到姿态顶点。
  - 姿态顶点对齐输入图像后，用颜色查询网络预测颜色，实现像素对齐纹理推理。
- **时间传播与高效推理**：
  - 设置帧阈值 \(n=5\)：前 5 帧做完整形状推理，建立可靠规范形状表示；之后进入高效推理。
  - **跳过粗到细推理**：已有传播的规范形状可作为几何先验，不再全体积预测，只细化必要区域。
  - **可见性引导采样**：通过网格光栅化计算规范 SMPL 顶点可见性，再用 KNN 传播到规范坐标，只查询当前视角可见区域。
  - **表面邻近采样**：只采样 occupancy 位于窄带 \([α, β] = [0.4, 0.7]\) 的点，减少查询数量并保留表面细节。
  - **颜色传播与可见性处理**：可见顶点用颜色网络预测；遮挡或低可见顶点通过规范空间 KNN 从上一帧规范顶点传播颜色，再合并。
- **多视角扩展**：
  - 独立处理每个视角，并将各视角的规范表示合并，利用统一规范空间进行时间与空间融合，无需架构修改。

## 3. 实验设计

- **数据集与场景**：
  - **THuman2.0**：526 个扫描，490 训练、15 验证、21 测试；用于单图像几何与纹理评估，也是像素对齐网络预训练数据。
  - **CAPE**：零样本评估，分为 CAPE-NFP 和 CAPE-FP，对应非时尚和时尚姿态。
  - **NeuMan**：视频评估，使用 bike、citron、jogging、seattle 序列及官方测试划分。
- **评价指标**：
  - 单图像：Chamfer distance、P2S、L2 normal error、PSNR。
  - 视频：PSNR、SSIM、LPIPS，并比较平均 FPS 和训练时间。
- **对比方法**：
  - 单图像：PIFu、PIFuHD、ECON、GTA、SIFU，以及重评估版本。
  - 视频：HumanNerf、InstantAvatar、NeuMan、Vid2Avatar、GaussianAvatar、3DGS-Avatar、ExAvatar。
- **本文配置**：
  - 使用 GTA 和 SIFU 作为像素对齐骨干，记为 TPF3D-GTA、TPF3D-SIFU。
  - 另有三视角配置 TPF3D-GTA-3v、TPF3D-SIFU-3v，使用 0°、120°、240° 正交视图。
  - 规范空间重建分辨率 256³；帧阈值 \(n=5\)；表面邻近采样阈值 α=0.4、β=0.7，采样后随机打乱以提升覆盖。
- **消融实验**：
  - 在 NeuMan 的 citron 序列上逐步加入坐标映射、线性层、可见性引导采样、表面邻近采样、限制采样点、TorchScript，分析速度与质量变化。

## 4. 资源与算力

- 文中明确提到：实现使用 PyTorch，运行在**单张 NVIDIA RTX 4090 GPU** 上。
- 像素对齐重建网络使用
