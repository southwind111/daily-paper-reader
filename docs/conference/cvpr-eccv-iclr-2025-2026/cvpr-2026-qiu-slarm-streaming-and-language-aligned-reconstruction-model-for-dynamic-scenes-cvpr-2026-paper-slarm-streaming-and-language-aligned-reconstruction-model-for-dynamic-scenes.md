---
title: "SLARM: Streaming and Language-Aligned Reconstruction Model for Dynamic Scenes"
title_zh: SLARM：面向动态场景的流式语言对齐重建模型
authors: "Qiu, Zhicheng, Meng, Jiarui, Luo, Tong-an, Huang, Yican, Feng, Xuan, Li, Xuanfu, Xu, Zhan"
date: 2026
publication_date: 2026
publication_date_precision: year
publication_date_source: conference year only; exact release date unverified
publication_date_kind: unknown
pdf: "https://openaccess.thecvf.com/content/CVPR2026/papers/Qiu_SLARM_Streaming_and_Language-Aligned_Reconstruction_Model_for_Dynamic_Scenes_CVPR_2026_paper.pdf"
tags: ["query:dr"]
score: 9.0
evidence: 前馈式动态场景重建与实时流式推理
tldr: 动态场景重建通常需要兼顾几何、语义与实时性，而现有方法往往难以统一。SLARM是一个前馈模型，通过高阶运动建模捕捉复杂非均匀运动，无需光流监督，仅用可微渲染训练，并从LSeg蒸馏语义特征实现语言对齐。它采用窗口因果注意力处理图像序列，实现低延迟流式推理且不累积内存开销。该框架统一了动态重建、语义理解与实时推理，并支持自然语言查询。
source: CVPR-2026-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-qiu-slarm-streaming-and-language-aligned-reconstruction-model-for-dynamic-scenes-cvpr-2026-paper/fig-001.webp\", \"caption\": \"\", \"page\": 1, \"index\": 1, \"width\": 759, \"height\": 192}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-qiu-slarm-streaming-and-language-aligned-reconstruction-model-for-dynamic-scenes-cvpr-2026-paper/fig-002.webp\", \"caption\": \"\", \"page\": 1, \"index\": 2, \"width\": 660, \"height\": 891}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-qiu-slarm-streaming-and-language-aligned-reconstruction-model-for-dynamic-scenes-cvpr-2026-paper/fig-003.webp\", \"caption\": \"\", \"page\": 1, \"index\": 3, \"width\": 505, \"height\": 391}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-qiu-slarm-streaming-and-language-aligned-reconstruction-model-for-dynamic-scenes-cvpr-2026-paper/fig-004.webp\", \"caption\": \"\", \"page\": 1, \"index\": 4, \"width\": 815, \"height\": 520}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-qiu-slarm-streaming-and-language-aligned-reconstruction-model-for-dynamic-scenes-cvpr-2026-paper/fig-005.webp\", \"caption\": \"\", \"page\": 1, \"index\": 5, \"width\": 505, \"height\": 394}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-qiu-slarm-streaming-and-language-aligned-reconstruction-model-for-dynamic-scenes-cvpr-2026-paper/fig-006.webp\", \"caption\": \"\", \"page\": 1, \"index\": 6, \"width\": 720, \"height\": 580}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-qiu-slarm-streaming-and-language-aligned-reconstruction-model-for-dynamic-scenes-cvpr-2026-paper/fig-007.webp\", \"caption\": \"\", \"page\": 5, \"index\": 7, \"width\": 480, \"height\": 320}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-qiu-slarm-streaming-and-language-aligned-reconstruction-model-for-dynamic-scenes-cvpr-2026-paper/fig-008.webp\", \"caption\": \"\", \"page\": 6, \"index\": 8, \"width\": 962, \"height\": 532}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-qiu-slarm-streaming-and-language-aligned-reconstruction-model-for-dynamic-scenes-cvpr-2026-paper/fig-009.webp\", \"caption\": \"\", \"page\": 6, \"index\": 9, \"width\": 955, \"height\": 531}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-qiu-slarm-streaming-and-language-aligned-reconstruction-model-for-dynamic-scenes-cvpr-2026-paper/fig-010.webp\", \"caption\": \"\", \"page\": 6, \"index\": 10, \"width\": 975, \"height\": 614}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-qiu-slarm-streaming-and-language-aligned-reconstruction-model-for-dynamic-scenes-cvpr-2026-paper/fig-011.webp\", \"caption\": \"\", \"page\": 8, \"index\": 11, \"width\": 480, \"height\": 320}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-qiu-slarm-streaming-and-language-aligned-reconstruction-model-for-dynamic-scenes-cvpr-2026-paper/fig-012.webp\", \"caption\": \"\", \"page\": 8, \"index\": 12, \"width\": 480, \"height\": 320}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-qiu-slarm-streaming-and-language-aligned-reconstruction-model-for-dynamic-scenes-cvpr-2026-paper/fig-013.webp\", \"caption\": \"\", \"page\": 8, \"index\": 13, \"width\": 480, \"height\": 320}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-qiu-slarm-streaming-and-language-aligned-reconstruction-model-for-dynamic-scenes-cvpr-2026-paper/fig-014.webp\", \"caption\": \"\", \"page\": 8, \"index\": 14, \"width\": 480, \"height\": 320}]"
motivation: 动态场景重建需兼顾几何、语义与实时性，现有方法难以统一。
method: SLARM以高阶运动建模捕捉非均匀运动，仅用可微渲染训练，并蒸馏LSeg语义实现语言对齐，采用窗口因果注意力流式推理。
result: 模型实现低延迟流式推理且不累积内存，动态重建精度与鲁棒性提升。
conclusion: 统一了动态重建、语义理解与实时推理，并支持自然语言查询。
---

## Abstract
We propose SLARM, a feed-forward model that unifies dynamic scene reconstruction, semantic understanding, and real-time streaming inference. SLARM captures complex, non-uniform motion through higher-order motion modeling, trained solely on differentiable renderings without any flow supervision. Besides, SLARM distills semantic features from LSeg to obtain language-aligned representations. This design enables semantic querying via natural language, and the tight coupling between semantics and geometry further enhances the accuracy and robustness of dynamic reconstruction. Moreover, SLARM processes image sequences using window-based causal attention, achieving stable, low-latency streaming inference without accumulating memory cost. Within this unified framework, SLARM achieves state-of-the-art results in dynamic estimation, rendering quality, and scene parsing, improving motion accuracy by 21%, reconstruction PSNR by 1.6 dB, and segmentation mIoU by 20% over existing methods.

---

## 论文详细总结（自动生成）

# SLARM 论文中文总结

## 1. 核心问题与整体含义

- **研究背景**：NeRF、3DGS 推动了 3D 场景重建，但动态场景重建仍多依赖逐场景优化，耗时从数分钟到数小时，泛化能力有限。
- **前馈重建趋势**：DUST3R、PixelSplat、VGGT、MapAnything 等将数据驱动范式引入 3D 重建，但大多面向静态场景，动态环境下的前馈重建仍不充分。
- **现有动态方法不足**：STORM 可从多时刻、已知位姿图像重建动态 3D 场景，但存在三点局限：
  - 运动建模过简，假设匀速运动，难以处理非线性、非均匀动态；
  - 功能单一，仅关注几何重建，缺少高层语义理解；
  - 推理效率不足，需要批量多帧和跨时间插值，不支持增量流式推理。
- **论文整体含义**：SLARM 是一个前馈式 4D 高斯推理框架，统一动态重建、语义理解和实时流式推理，面向自动驾驶、具身 AI 等需要低延迟、长时序部署的场景。

## 2. 方法论

### 2.1 核心思想

- 给定带已知内参和外参的视频序列，SLARM 在每个时间步维护显式 4D 高斯表示，同时完成：
  - 当前几何与外观重建；
  - 每个高斯的 3D 场景流编码；
  - 每个高斯的语言对齐语义特征关联，支持文本查询。
- 核心目标：无需真实场景流监督，通过可微渲染自监督学习运动；通过 2D 基础模型蒸馏获得语言对齐语义；通过窗口因果注意力实现低延迟、常数内存的流式推理。

### 2.2 模型流程与表示

- 使用共享权重 ViT 提取图像 token，将图像分块。
- 注入几何先验：将像素视角射线编码为 6D Plücker 坐标，线性投影后加到视觉 token。
- 加入绝对时间戳的可学习嵌入。
- 拼接特殊 token：
  - Sky token：建模天空区域；
  - Affine token：补偿多相机曝光和白平衡变化。
- 使用交替注意力 Transformer 主干，交替进行帧内注意力和全局注意力。
- 高斯解码器为每像素回归 4DGS 参数：
  - 3D 位置 μ、旋转 q、尺度 s、不透明度 α、颜色 c；
  - 位置由 μ = o + d · r 得到，d 为预测深度，o、r 为相机射线原点和方向。
- 辅助头输出：
  - 动态属性向量，编码场景流；
  - 语义特征向量，对齐视觉-语言嵌入空间。

### 2.3 高阶运动建模

- 不同于 STORM 的匀速假设，SLARM 用多阶泰勒展开建模位移。
- 对每阶 l，网络预测标量速度 s_l 和 3D 方向向量 v_l，并计算运动系数：
  - m_l = s_l · v_l / ||v_l||_2。
- 给定时间偏移 Δt，总位移为：
  - Γ(Δt) = Σ_{l=0}^{L-1} m_l · (Δt)^{l+1} / (l+1)!。
- 实验中取 L = 3，对应位置的一阶、二阶、三阶时间导数：速度、加速度、加加速度。
- 高斯随时间变化时仅允许位置演化：
  - G_{t→t+Δt} = {μ_i + Γ_i(Δt), α_i, q_i, s_i, c_i}。
- 运动通过渲染监督学习：将变形后的高斯渲染为图像，与监督帧计算 MSE 和 LPIPS 损失。

### 2.4 语义特征蒸馏与语言对齐

- 每个高斯增加高维语义特征向量 f_sem。
- 渲染时同时合成 RGB 图和语义特征图，通过 alpha 混合时间变形后的高斯语义属性。
- 使用冻结的 LSeg 提取 2D 语义特征，并以 MSE 蒸馏到 4D 高斯表示：
  - L_sem = ||F_teacher - F_render_decoded||^2。
- 对已有语义标注的数据，将重建语义解码为特征图，与 CLIP 文本编码得到的类别文本特征计算内积，softmax 后做分类，使用交叉熵损失：
  - L_cls 形式为对每个位置分类到正确类别的负对数似然，温度 τ = 0.07。
- 该设计使语义特征可直接由自然语言查询，并可接入 LLM/VLM 进行推理。

### 2.5 流式 4D 重建

- 与离线动态重建不同，流式设置严格因果：推理时只能使用当前和过去帧。
- 模型输出当前时刻 3D 高斯 G_t 和位移场 Γ_t，条件为截至当前时刻的观测帧。
- 在线推理中，动态高斯仅向后传播到最近历史帧 t - Δt，通常 Δt = 5。
- 将高斯按运动幅度划分为静态和动态：
  - G_static = {g | ||Γ_g(Δt)|| ≤ τ_m}；
  - G_dynamic = {g | ||Γ_g(Δt)|| > τ_m}。
- 区间 [t - Δt, t] 的场景由静态几何和向后动态组成，避免新时间步出现渲染空洞。
- 使用窗口因果注意力，处理每帧独立并传播紧凑隐藏状态，实现常数延迟和常数内存。

### 2.6 损失函数与训练细节

- 总损失
