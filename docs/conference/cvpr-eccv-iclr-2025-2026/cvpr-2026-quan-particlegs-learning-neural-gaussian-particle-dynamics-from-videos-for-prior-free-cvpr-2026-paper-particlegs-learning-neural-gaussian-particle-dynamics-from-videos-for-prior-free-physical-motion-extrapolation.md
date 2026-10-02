---
title: "ParticleGS: Learning Neural Gaussian Particle Dynamics from Videos for Prior-free Physical Motion Extrapolation"
title_zh: ParticleGS：从视频学习神经高斯粒子动力学以实现无先验物理运动外推
authors: "Quan, Jinsheng, Miao, Qiaowei, Xu, Yichao, Lin, Zizhuo, Li, Ying, Yang, Wei, Li, Zhihui, Luo, Yawei"
date: 2026
publication_date: 2026
publication_date_precision: year
publication_date_source: conference year only; exact release date unverified
publication_date_kind: unknown
pdf: "https://openaccess.thecvf.com/content/CVPR2026/papers/Quan_ParticleGS_Learning_Neural_Gaussian_Particle_Dynamics_from_Videos_for_Prior-free_CVPR_2026_paper.pdf"
tags: ["query:dr"]
score: 8.0
evidence: 将动态三维场景建模为物理系统以实现四维运动外推
tldr: 现有动态三维重建虽能高保真地进行时间插值渲染，却在预测未来时缺乏物理一致性。本文提出ParticleGS，将动态三维场景重构为物理系统，用编码器分解静态属性与初始动态物理场，并以神经常微分方程演化器学习连续时间动力学。实验表明其能实现无先验的物理一致运动外推，超越仅能插值的重建方法，为动态场景的物理一致预测与未来外推提供了新框架。
source: CVPR-2026-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-quan-particlegs-learning-neural-gaussian-particle-dynamics-from-videos-for-prior-free-cvpr-2026-paper/fig-001.webp\", \"caption\": \"\", \"page\": 1, \"index\": 1, \"width\": 524, \"height\": 698}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-quan-particlegs-learning-neural-gaussian-particle-dynamics-from-videos-for-prior-free-cvpr-2026-paper/fig-002.webp\", \"caption\": \"\", \"page\": 1, \"index\": 2, \"width\": 523, \"height\": 698}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-quan-particlegs-learning-neural-gaussian-particle-dynamics-from-videos-for-prior-free-cvpr-2026-paper/fig-003.webp\", \"caption\": \"\", \"page\": 1, \"index\": 3, \"width\": 524, \"height\": 698}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-quan-particlegs-learning-neural-gaussian-particle-dynamics-from-videos-for-prior-free-cvpr-2026-paper/fig-004.webp\", \"caption\": \"\", \"page\": 4, \"index\": 4, \"width\": 400, \"height\": 400}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-quan-particlegs-learning-neural-gaussian-particle-dynamics-from-videos-for-prior-free-cvpr-2026-paper/fig-005.webp\", \"caption\": \"\", \"page\": 4, \"index\": 5, \"width\": 400, \"height\": 400}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-quan-particlegs-learning-neural-gaussian-particle-dynamics-from-videos-for-prior-free-cvpr-2026-paper/fig-006.webp\", \"caption\": \"\", \"page\": 4, \"index\": 6, \"width\": 400, \"height\": 400}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-quan-particlegs-learning-neural-gaussian-particle-dynamics-from-videos-for-prior-free-cvpr-2026-paper/fig-007.webp\", \"caption\": \"\", \"page\": 4, \"index\": 7, \"width\": 400, \"height\": 400}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-quan-particlegs-learning-neural-gaussian-particle-dynamics-from-videos-for-prior-free-cvpr-2026-paper/fig-008.webp\", \"caption\": \"\", \"page\": 4, \"index\": 8, \"width\": 400, \"height\": 400}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-quan-particlegs-learning-neural-gaussian-particle-dynamics-from-videos-for-prior-free-cvpr-2026-paper/fig-009.webp\", \"caption\": \"\", \"page\": 4, \"index\": 9, \"width\": 400, \"height\": 400}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-quan-particlegs-learning-neural-gaussian-particle-dynamics-from-videos-for-prior-free-cvpr-2026-paper/fig-010.webp\", \"caption\": \"\", \"page\": 7, \"index\": 10, \"width\": 400, \"height\": 400}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-quan-particlegs-learning-neural-gaussian-particle-dynamics-from-videos-for-prior-free-cvpr-2026-paper/fig-011.webp\", \"caption\": \"\", \"page\": 7, \"index\": 11, \"width\": 400, \"height\": 400}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-quan-particlegs-learning-neural-gaussian-particle-dynamics-from-videos-for-prior-free-cvpr-2026-paper/fig-012.webp\", \"caption\": \"\", \"page\": 7, \"index\": 12, \"width\": 400, \"height\": 400}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-quan-particlegs-learning-neural-gaussian-particle-dynamics-from-videos-for-prior-free-cvpr-2026-paper/fig-013.webp\", \"caption\": \"\", \"page\": 7, \"index\": 13, \"width\": 400, \"height\": 400}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-quan-particlegs-learning-neural-gaussian-particle-dynamics-from-videos-for-prior-free-cvpr-2026-paper/fig-014.webp\", \"caption\": \"\", \"page\": 7, \"index\": 14, \"width\": 400, \"height\": 400}]"
motivation: 现有动态三维重建能高保真插值渲染，但在预测未来时缺乏物理一致性。
method: 提出ParticleGS，将动态场景建模为物理系统，用编码器分解静态属性与动态物理场，并用神经常微分方程演化器学习连续时间动力学。
result: 在无先验条件下实现物理一致的运动外推，超越仅能时间插值的重建方法。
conclusion: 为动态场景的物理一致预测与未来外推提供了新框架。
---

## Abstract
The ability to extrapolate dynamic 3D scenes beyond the observed timeframe is fundamental to advancing physical world understanding and predictive modeling. Existing dynamic 3D reconstruction methods have achieved high-fidelity rendering of temporal interpolation, but typically lack physical consistency in predicting the future. To overcome this issue, we propose ParticleGS, a physics-based framework that reformulates dynamic 3D scenes as physically grounded systems. ParticleGS comprises three key components: 1) an encoder that decomposes the scene into static properties and initial dynamic physical fields; 2) an evolver based on Neural Ordinary Differential Equations (Neural ODEs) that learns continuous-time dynamics for motion extrapolation; and 3) a decoder that reconstructs 3D Gaussians from evolved particle states for rendering. Through this design, ParticleGS integrates physical reasoning into dynamic 3D representations, enabling accurate and consistent prediction of the future. Experiments show that ParticleGS achieves state-of-the-art performance in extrapolation while maintaining rendering quality.

---

## 论文详细总结（自动生成）

# ParticleGS 论文总结

## 1. 核心问题与整体含义
- **研究动机**：现有动态 3D 重建/渲染方法（NeRF、3DGS 系列）能高质量完成时间插值，但通常把未来状态预测为“时间的函数”，只记忆或拟合已观测时间段内的变形，缺乏对物理规律的学习。
- **核心问题**：如何从多视角视频中直接学习动态 3D 场景的潜在物理动力学，并外推到观测时间范围之外，使未来高斯运动与外观既准确又物理一致。
- **整体含义**：论文将动态 3D 场景重新表述为受物理状态驱动的粒子系统，尝试连接动态 3D 表示与物理推理，为游戏、自动驾驶、机器人等需要未来预测的应用提供新框架。

## 2. 方法论
- **核心思想**：不再用时间条件变形模型 \(D(P,t)=P_t\)，而是将每个 3D Gaussian 视为粒子，用物理状态集合 \(Z_t\) 驱动高斯变形，即 \(R(D(P,Z_t),v)=\hat I_v^t\)。相比单纯时间戳，\(Z_t\) 具备时空感知、物理合理性和 Markov 性质。
- **三大组件**：
  - **Dynamics Latent Space Encoder**：将 canonical Gaussians 编码为初始物理状态 \(Z_0\)
