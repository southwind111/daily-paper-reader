---
title: "FreeTimeGS: Free Gaussian Primitives at Anytime Anywhere for Dynamic Scene Reconstruction"
title_zh: FreeTimeGS：面向动态场景重建的自由时空高斯基元
authors: "Wang, Yifan, Yang, Peishan, Xu, Zhen, Sun, Jiaming, Zhang, Zhanhua, Chen, Yong, Bao, Hujun, Peng, Sida, Zhou, Xiaowei"
date: 2025
publication_date: 2025
publication_date_precision: year
publication_date_source: conference year only; exact release date unverified
publication_date_kind: unknown
pdf: "https://openaccess.thecvf.com/content/CVPR2025/papers/Wang_FreeTimeGS_Free_Gaussian_Primitives_at_Anytime_Anywhere_for_Dynamic_Scene_CVPR_2025_paper.pdf"
tags: ["query:dr"]
score: 10.0
evidence: 自由时空高斯基元动态场景重建
tldr: 针对现有在规范空间定义高斯基元并用形变场映射的方法难以应对复杂运动、形变场优化困难的问题，本文提出4D表示FreeTimeGS。它允许高斯基元在任意时间和位置自由出现，摆脱规范空间约束，从而增强对动态3D场景的建模灵活性。实验表明该方法能更好处理复杂运动并支持实时动态视角合成，为动态场景重建提供了新的4D表示范式。
source: CVPR-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-wang-freetimegs-free-gaussian-primitives-at-anytime-anywhere-for-dynamic-scene-cvpr-2025-paper/fig-001.webp\", \"caption\": \"\", \"page\": 3, \"index\": 1, \"width\": 616, \"height\": 1025}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-wang-freetimegs-free-gaussian-primitives-at-anytime-anywhere-for-dynamic-scene-cvpr-2025-paper/fig-002.webp\", \"caption\": \"\", \"page\": 3, \"index\": 2, \"width\": 632, \"height\": 1070}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-wang-freetimegs-free-gaussian-primitives-at-anytime-anywhere-for-dynamic-scene-cvpr-2025-paper/fig-003.webp\", \"caption\": \"\", \"page\": 3, \"index\": 3, \"width\": 462, \"height\": 498}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-wang-freetimegs-free-gaussian-primitives-at-anytime-anywhere-for-dynamic-scene-cvpr-2025-paper/fig-004.webp\", \"caption\": \"\", \"page\": 3, \"index\": 4, \"width\": 441, \"height\": 475}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-wang-freetimegs-free-gaussian-primitives-at-anytime-anywhere-for-dynamic-scene-cvpr-2025-paper/fig-005.webp\", \"caption\": \"\", \"page\": 3, \"index\": 5, \"width\": 660, \"height\": 260}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-wang-freetimegs-free-gaussian-primitives-at-anytime-anywhere-for-dynamic-scene-cvpr-2025-paper/fig-006.webp\", \"caption\": \"\", \"page\": 3, \"index\": 6, \"width\": 649, \"height\": 229}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-wang-freetimegs-free-gaussian-primitives-at-anytime-anywhere-for-dynamic-scene-cvpr-2025-paper/fig-007.webp\", \"caption\": \"\", \"page\": 3, \"index\": 7, \"width\": 904, \"height\": 871}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-wang-freetimegs-free-gaussian-primitives-at-anytime-anywhere-for-dynamic-scene-cvpr-2025-paper/fig-008.webp\", \"caption\": \"\", \"page\": 3, \"index\": 8, \"width\": 630, \"height\": 203}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-wang-freetimegs-free-gaussian-primitives-at-anytime-anywhere-for-dynamic-scene-cvpr-2025-paper/fig-009.webp\", \"caption\": \"\", \"page\": 3, \"index\": 9, \"width\": 585, \"height\": 772}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-wang-freetimegs-free-gaussian-primitives-at-anytime-anywhere-for-dynamic-scene-cvpr-2025-paper/fig-010.webp\", \"caption\": \"\", \"page\": 3, \"index\": 10, \"width\": 645, \"height\": 868}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-wang-freetimegs-free-gaussian-primitives-at-anytime-anywhere-for-dynamic-scene-cvpr-2025-paper/fig-011.webp\", \"caption\": \"\", \"page\": 3, \"index\": 11, \"width\": 674, \"height\": 480}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-wang-freetimegs-free-gaussian-primitives-at-anytime-anywhere-for-dynamic-scene-cvpr-2025-paper/fig-012.webp\", \"caption\": \"\", \"page\": 3, \"index\": 12, \"width\": 1881, \"height\": 1058}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-wang-freetimegs-free-gaussian-primitives-at-anytime-anywhere-for-dynamic-scene-cvpr-2025-paper/fig-013.webp\", \"caption\": \"\", \"page\": 3, \"index\": 13, \"width\": 445, \"height\": 316}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-wang-freetimegs-free-gaussian-primitives-at-anytime-anywhere-for-dynamic-scene-cvpr-2025-paper/fig-014.webp\", \"caption\": \"\", \"page\": 3, \"index\": 14, \"width\": 875, \"height\": 871}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-wang-freetimegs-free-gaussian-primitives-at-anytime-anywhere-for-dynamic-scene-cvpr-2025-paper/fig-015.webp\", \"caption\": \"\", \"page\": 3, \"index\": 15, \"width\": 675, \"height\": 760}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-wang-freetimegs-free-gaussian-primitives-at-anytime-anywhere-for-dynamic-scene-cvpr-2025-paper/fig-016.webp\", \"caption\": \"\", \"page\": 3, \"index\": 16, \"width\": 648, \"height\": 725}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-wang-freetimegs-free-gaussian-primitives-at-anytime-anywhere-for-dynamic-scene-cvpr-2025-paper/fig-017.webp\", \"caption\": \"\", \"page\": 6, \"index\": 17, \"width\": 657, \"height\": 438}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-wang-freetimegs-free-gaussian-primitives-at-anytime-anywhere-for-dynamic-scene-cvpr-2025-paper/fig-018.webp\", \"caption\": \"\", \"page\": 6, \"index\": 18, \"width\": 657, \"height\": 438}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-wang-freetimegs-free-gaussian-primitives-at-anytime-anywhere-for-dynamic-scene-cvpr-2025-paper/fig-019.webp\", \"caption\": \"\", \"page\": 6, \"index\": 19, \"width\": 657, \"height\": 438}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-wang-freetimegs-free-gaussian-primitives-at-anytime-anywhere-for-dynamic-scene-cvpr-2025-paper/fig-020.webp\", \"caption\": \"\", \"page\": 6, \"index\": 20, \"width\": 657, \"height\": 438}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-wang-freetimegs-free-gaussian-primitives-at-anytime-anywhere-for-dynamic-scene-cvpr-2025-paper/fig-021.webp\", \"caption\": \"\", \"page\": 6, \"index\": 21, \"width\": 657, \"height\": 438}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-wang-freetimegs-free-gaussian-primitives-at-anytime-anywhere-for-dynamic-scene-cvpr-2025-paper/fig-022.webp\", \"caption\": \"\", \"page\": 6, \"index\": 22, \"width\": 657, \"height\": 438}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-wang-freetimegs-free-gaussian-primitives-at-anytime-anywhere-for-dynamic-scene-cvpr-2025-paper/fig-023.webp\", \"caption\": \"\", \"page\": 6, \"index\": 23, \"width\": 657, \"height\": 438}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-wang-freetimegs-free-gaussian-primitives-at-anytime-anywhere-for-dynamic-scene-cvpr-2025-paper/fig-024.webp\", \"caption\": \"\", \"page\": 6, \"index\": 24, \"width\": 657, \"height\": 438}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-wang-freetimegs-free-gaussian-primitives-at-anytime-anywhere-for-dynamic-scene-cvpr-2025-paper/fig-025.webp\", \"caption\": \"\", \"page\": 6, \"index\": 25, \"width\": 657, \"height\": 438}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-wang-freetimegs-free-gaussian-primitives-at-anytime-anywhere-for-dynamic-scene-cvpr-2025-paper/fig-026.webp\", \"caption\": \"\", \"page\": 6, \"index\": 26, \"width\": 657, \"height\": 438}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-wang-freetimegs-free-gaussian-primitives-at-anytime-anywhere-for-dynamic-scene-cvpr-2025-paper/fig-027.webp\", \"caption\": \"\", \"page\": 6, \"index\": 27, \"width\": 657, \"height\": 438}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-wang-freetimegs-free-gaussian-primitives-at-anytime-anywhere-for-dynamic-scene-cvpr-2025-paper/fig-028.webp\", \"caption\": \"\", \"page\": 6, \"index\": 28, \"width\": 657, \"height\": 438}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-wang-freetimegs-free-gaussian-primitives-at-anytime-anywhere-for-dynamic-scene-cvpr-2025-paper/fig-029.webp\", \"caption\": \"\", \"page\": 6, \"index\": 29, \"width\": 657, \"height\": 438}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-wang-freetimegs-free-gaussian-primitives-at-anytime-anywhere-for-dynamic-scene-cvpr-2025-paper/fig-030.webp\", \"caption\": \"\", \"page\": 6, \"index\": 30, \"width\": 657, \"height\": 438}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-wang-freetimegs-free-gaussian-primitives-at-anytime-anywhere-for-dynamic-scene-cvpr-2025-paper/fig-031.webp\", \"caption\": \"\", \"page\": 6, \"index\": 31, \"width\": 657, \"height\": 438}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-wang-freetimegs-free-gaussian-primitives-at-anytime-anywhere-for-dynamic-scene-cvpr-2025-paper/fig-032.webp\", \"caption\": \"\", \"page\": 6, \"index\": 32, \"width\": 657, \"height\": 438}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-wang-freetimegs-free-gaussian-primitives-at-anytime-anywhere-for-dynamic-scene-cvpr-2025-paper/fig-033.webp\", \"caption\": \"\", \"page\": 6, \"index\": 33, \"width\": 676, \"height\": 507}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-wang-freetimegs-free-gaussian-primitives-at-anytime-anywhere-for-dynamic-scene-cvpr-2025-paper/fig-034.webp\", \"caption\": \"\", \"page\": 6, \"index\": 34, \"width\": 676, \"height\": 507}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-wang-freetimegs-free-gaussian-primitives-at-anytime-anywhere-for-dynamic-scene-cvpr-2025-paper/fig-035.webp\", \"caption\": \"\", \"page\": 6, \"index\": 35, \"width\": 675, \"height\": 506}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-wang-freetimegs-free-gaussian-primitives-at-anytime-anywhere-for-dynamic-scene-cvpr-2025-paper/fig-036.webp\", \"caption\": \"\", \"page\": 6, \"index\": 36, \"width\": 676, \"height\": 504}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-wang-freetimegs-free-gaussian-primitives-at-anytime-anywhere-for-dynamic-scene-cvpr-2025-paper/fig-037.webp\", \"caption\": \"\", \"page\": 7, \"index\": 37, \"width\": 699, \"height\": 465}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-wang-freetimegs-free-gaussian-primitives-at-anytime-anywhere-for-dynamic-scene-cvpr-2025-paper/fig-038.webp\", \"caption\": \"\", \"page\": 7, \"index\": 38, \"width\": 699, \"height\": 465}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-wang-freetimegs-free-gaussian-primitives-at-anytime-anywhere-for-dynamic-scene-cvpr-2025-paper/fig-039.webp\", \"caption\": \"\", \"page\": 7, \"index\": 39, \"width\": 699, \"height\": 465}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-wang-freetimegs-free-gaussian-primitives-at-anytime-anywhere-for-dynamic-scene-cvpr-2025-paper/fig-040.webp\", \"caption\": \"\", \"page\": 7, \"index\": 40, \"width\": 699, \"height\": 465}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-wang-freetimegs-free-gaussian-primitives-at-anytime-anywhere-for-dynamic-scene-cvpr-2025-paper/fig-041.webp\", \"caption\": \"\", \"page\": 7, \"index\": 41, \"width\": 699, \"height\": 465}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-wang-freetimegs-free-gaussian-primitives-at-anytime-anywhere-for-dynamic-scene-cvpr-2025-paper/fig-042.webp\", \"caption\": \"\", \"page\": 7, \"index\": 42, \"width\": 699, \"height\": 465}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-wang-freetimegs-free-gaussian-primitives-at-anytime-anywhere-for-dynamic-scene-cvpr-2025-paper/fig-043.webp\", \"caption\": \"\", \"page\": 7, \"index\": 43, \"width\": 699, \"height\": 465}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-wang-freetimegs-free-gaussian-primitives-at-anytime-anywhere-for-dynamic-scene-cvpr-2025-paper/fig-044.webp\", \"caption\": \"\", \"page\": 7, \"index\": 44, \"width\": 699, \"height\": 465}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-wang-freetimegs-free-gaussian-primitives-at-anytime-anywhere-for-dynamic-scene-cvpr-2025-paper/fig-045.webp\", \"caption\": \"\", \"page\": 7, \"index\": 45, \"width\": 699, \"height\": 465}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-wang-freetimegs-free-gaussian-primitives-at-anytime-anywhere-for-dynamic-scene-cvpr-2025-paper/fig-046.webp\", \"caption\": \"\", \"page\": 7, \"index\": 46, \"width\": 699, \"height\": 465}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-wang-freetimegs-free-gaussian-primitives-at-anytime-anywhere-for-dynamic-scene-cvpr-2025-paper/fig-047.webp\", \"caption\": \"\", \"page\": 7, \"index\": 47, \"width\": 699, \"height\": 465}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-wang-freetimegs-free-gaussian-primitives-at-anytime-anywhere-for-dynamic-scene-cvpr-2025-paper/fig-048.webp\", \"caption\": \"\", \"page\": 7, \"index\": 48, \"width\": 699, \"height\": 465}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-wang-freetimegs-free-gaussian-primitives-at-anytime-anywhere-for-dynamic-scene-cvpr-2025-paper/fig-049.webp\", \"caption\": \"\", \"page\": 7, \"index\": 49, \"width\": 699, \"height\": 465}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-wang-freetimegs-free-gaussian-primitives-at-anytime-anywhere-for-dynamic-scene-cvpr-2025-paper/fig-050.webp\", \"caption\": \"\", \"page\": 7, \"index\": 50, \"width\": 699, \"height\": 465}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-wang-freetimegs-free-gaussian-primitives-at-anytime-anywhere-for-dynamic-scene-cvpr-2025-paper/fig-051.webp\", \"caption\": \"\", \"page\": 7, \"index\": 51, \"width\": 699, \"height\": 465}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-wang-freetimegs-free-gaussian-primitives-at-anytime-anywhere-for-dynamic-scene-cvpr-2025-paper/fig-052.webp\", \"caption\": \"\", \"page\": 7, \"index\": 52, \"width\": 699, \"height\": 465}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-wang-freetimegs-free-gaussian-primitives-at-anytime-anywhere-for-dynamic-scene-cvpr-2025-paper/fig-053.webp\", \"caption\": \"\", \"page\": 8, \"index\": 53, \"width\": 646, \"height\": 646}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-wang-freetimegs-free-gaussian-primitives-at-anytime-anywhere-for-dynamic-scene-cvpr-2025-paper/fig-054.webp\", \"caption\": \"\", \"page\": 8, \"index\": 54, \"width\": 646, \"height\": 646}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-wang-freetimegs-free-gaussian-primitives-at-anytime-anywhere-for-dynamic-scene-cvpr-2025-paper/fig-055.webp\", \"caption\": \"\", \"page\": 8, \"index\": 55, \"width\": 646, \"height\": 646}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-wang-freetimegs-free-gaussian-primitives-at-anytime-anywhere-for-dynamic-scene-cvpr-2025-paper/fig-056.webp\", \"caption\": \"\", \"page\": 8, \"index\": 56, \"width\": 646, \"height\": 646}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-wang-freetimegs-free-gaussian-primitives-at-anytime-anywhere-for-dynamic-scene-cvpr-2025-paper/fig-057.webp\", \"caption\": \"\", \"page\": 8, \"index\": 57, \"width\": 646, \"height\": 646}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-wang-freetimegs-free-gaussian-primitives-at-anytime-anywhere-for-dynamic-scene-cvpr-2025-paper/fig-058.webp\", \"caption\": \"\", \"page\": 8, \"index\": 58, \"width\": 646, \"height\": 646}]"
motivation: 基于规范空间高斯与形变场的动态重建方法在复杂运动场景中难以优化形变场。
method: 提出4D表示FreeTimeGS，允许高斯基元在任意时间和位置出现，增强建模动态3D场景的灵活性。
result: 该表示能更好地处理复杂运动，并支持实时动态视角合成。
conclusion: 摆脱规范空间约束的自由高斯基元为复杂动态场景重建提供了更灵活的4D表示。
---

## Abstract
This paper addresses the challenge of reconstructing dynamic 3D scenes with complex motions. Some recent works define 3D Gaussian primitives in the canonical space and use deformation fields to map canonical primitives to observation spaces, achieving real-time dynamic view synthesis. However, these methods often struggle to handle scenes with complex motions due to the difficulty of optimizing deformation fields. To overcome this problem, we propose FreeTimeGS, a novel 4D representation that allows Gaussian primitives to appear at arbitrary time and locations. In contrast to canonical Gaussian primitives, our representation possesses the strong flexibility, thus improving the ability to model dynamic 3D scenes. In addition, we endow each Gaussian primitive with an motion function, allowing it to move to neighboring regions over time, which reduces the temporal redundancy. Experiments results on several datasets show that the rendering quality of our method outperforms recent methods by a large margin. The code will be released for reproducibility.

---

## 论文详细总结（自动生成）

# FreeTimeGS 论文中文总结

## 1. 核心问题与整体含义（研究动机与背景）

- **研究领域**：动态三维场景重建与自由视角合成（Dynamic View Synthesis），目标是从多视角视频中生成动态场景的新视角图像。
- **应用背景**：电影制作、视频游戏、虚拟现实等场景均需要高质量、实时的动态场景重建。
- **现有方法的两条主要路线**：
  - 基于 NeRF 的隐式表示：渲染质量高但计算开销大、渲染速度慢。
  - 基于 3D Gaussian Splatting 的方法：将高斯基元定义在**规范空间（canonical space）**，再用 MLP 形变场将规范基元映射到观测空间，实现实时渲染。
- **核心痛点**：现有基于规范空间 + 形变场的方法（如 Deformable-3DGS、4DGS、STGS）在**复杂、快速运动场景**下表现不佳。原因是当物体大幅移动时，需要建立规范空间与观测空间之间的**长距离对应关系**，而该对应关系难以从 RGB 观测中恢复；此外，4DGS 将几何与速度纠缠、在角空间优化速度，STGS 使用多项式与角速度导致参数过多，均难以优化。
- **论文整体含义**：提出一种全新的 4D 表示 **FreeTimeGS**，允许高斯基元在**任意时间和任意位置**自由出现，摆脱规范空间约束，从而增强对复杂动态场景的建模能力，同时保持实时渲染速度。

## 2. 方法论：核心思想与关键技术细节

### 2.1 核心思想
- 不再将高斯基元固定于规范空间，而是让每个高斯基元携带**自身的出现时间、持续时长与速度**，在任意时空位置出现并随时间移动。
- 每个高斯基元包含 **8 个可学习参数**：位置、时间、持续时长、速度、尺度、朝向、不透明度、球谐系数（SH）。

### 2.2 运动与外观建模
- **运动函数**（线性运动，降低优化难度）：
  - μx(t) = μx + v · (t − μt)
  - 其中 v 为速度，μx 为原始位置，μt 为原始时间。
- **颜色**：使用球谐模型，依据移动后位置 μx(t) 处的视线方向 d(μx(t)) 计算。
- **不透明度**：
  - σ(x, t) = σ(t) · σ · exp( −½ (x − μx(t))ᵀ Σ⁻¹ (x − μx(t)) )
  - Σ = R S Sᵀ Rᵀ，由尺度与朝向决定。
- **时间不透明度**（单峰高斯分布，使时间与持续时长可被渲染梯度自动调整）：
  - σ(t) = exp( −½ ((t − μt) / s)² )
  - s 为持续时长。

### 2.3 训练策略
- **渲染损失**：
  - Lrender = λimg Limg + λssim Lssim + λperc Lperc
- **4D 正则化**：
  - 观察发现部分高斯基元不透明度接近 1，会阻碍梯度反传到所有基元，导致优化陷入局部极小值。
  - Lreg(t) = (1/N) Σᵢ (σ · sg[σ(t)])，其中 sg[·] 为停止梯度操作，σ(t) 作为权重以减轻对低影响基元的惩罚。
- **周期性重定位（Periodic Relocation）**：
  - 每 N 次迭代，将低不透明度基元移动到高采样分数区域。
  - 采样分数 s = λg ∇g + λo σ，其中 ∇g 为空间梯度，σ 为不透明度。
- **4D 初始化**：
  - 用 ROMA 进行多视角 2D 匹配并三角化得到 3D 点，初始化位置与时间。
  - 用 k 近邻匹配两帧 3D 点，以平移量作为速度初始化。
  - 对速度优化率做退火调度：λt = λ₀^(1−t) + λ₁^t，早期建模快速运动、后期建模复杂运动。

### 2.4 实现细节
- PyTorch 实现，Adam 优化器，与 3DGS 设置一致。
- 300 帧序列训练 30k 次迭代。
- λreg = 1e−2；λimg = 0.8，λssim = 0.2，λperc = 0.01。
- 采样分数中 λg = 0.5，λo = 0.5；周期重定位每 N = 100 次迭代执行一次。

## 3. 实验设计

### 3.1 数据集
- **Neural3DV**：6 个场景，19–21 个相机，分辨率 2704×2028 @ 30 FPS，取前 300 帧，图像缩放比 0.5。
- **ENeRF-Outdoor**：3 个户外动态场景，18 个同步相机，分辨率 1920×1080 @ 60 FPS，取前 300 帧，缩放比 1。
- **SelfCap（自采集）**：8 个场景，60 帧，22–24 个相机，分辨率 3840×2160 @ 60 FPS，缩放比 0.5，包含跳舞、与宠物玩耍、修自行车等**快速复杂运动**场景。

### 3.2 评价指标（Benchmark）
- **PSNR**（越高越好）、**DSSIM₁ / DSSIM₂**（越高越好）、**LPIPS**（越低越好）、**FPS**（渲染速度）。
- 在 SelfCap 上同时报告**整图（entire）** 与**仅动态区域（dynamic）** 的指标。

### 3.3 对比方法
- Neural Volume、LLFF、DyNeRF、HexPlane、K-Planes、MixVoxels-L/X、HyperReel、NeRFPlayer、Deformable-3DGS、C-D3DGS、SWinGS、Ex4DGS、4DGS、STGS、ENeRF、4K4D 等。
- 主要对比对象为当前 SOTA 的 **4DGS** 与 **STGS**。

### 3.4 主要实验结果
- **Neural3DV**：PSNR 33.19，优于 4DGS（32.01）与 STGS（32.05）。
- **ENeRF-Outdoor**：PSNR 25.36，DSSIM₂ 0.077，LPIPS 0.244，FPS 454，全面领先。
- **SelfCap**：整图 27.41 dB / 动态区域 29.38 dB，相比 4DGS 提升 2.4 dB / 4.1 dB，相比 STGS 提升 1.4 dB / 2.6 dB；渲染速度 467 FPS。
- 论文称在单张 RTX 4090 上以 1080p 分辨率可达 **450+ FPS** 实时渲染。

### 3.5 消融实验
- 在 SelfCap 的 dance1 序列（60 帧）及其中运动最快的 10 帧子序列上评估。
- 消融组件包括：**运动表示**（替换为 4DGS 运动表示）、**4D 正则化**、**周期性重定位**、**4D 初始化**。
- 另对正则化权重 λreg 做敏感性分析（0、1e−3、1e−2、1e−1），最终选 1e−2。

## 4. 资源与算力

- 论文明确提到训练使用 **单张 RTX 4090 GPU**。
- **训练时长**：300 帧序列训练 30k 次迭代，约 **1 小时**。
- 渲染速度在单张 RTX 4090 上达到约 450–467 FPS（1080p）。
- 论文**未明确说明**是否使用了多卡训练、CPU 型号、显存占用等更详细的算力信息。

## 5. 实验数量与充分性

- **数据集覆盖**：3 个数据集（Neural3DV、ENeRF-Outdoor、自采集 SelfCap），涵盖室内、室外、快速复杂运动场景。
- **对比实验**：在三个数据集上分别与 10+ 种基线方法进行定量与定性比较。
- **消融实验**：4 组主要组件消融 + 1 组正则化权重敏感性实验，共 5 组左右。
- **评估维度**：同时报告全图与动态区域指标，兼顾质量（PSNR/DSSIM/LPIPS）与效率（FPS）。
- **充分性评价**：
  - 优点：数据集多样、对比方法全面、消融实验覆盖所有关键组件，指标设计较为客观。
  - 潜在不足：消融实验仅在自采集数据集的单一序列（dance1）上进行，泛化性证据略有限；对训练时长与显存等资源细节披露不足。

## 6. 主要结论与发现

- FreeTimeGS 在多个公开数据集上取得了**最优渲染质量**，尤其在**快速复杂运动区域**优势显著。
- 允许高斯基元在任意时空出现，并赋予显式运动函数，可**降低时间冗余**、提升建模灵活性。
- 由于只需建模**短距离运动**，运动函数可采用简单线性形式，缓解了形变场方法中长距离对应难以优化的问题。
- 4D 正则化能有效缓解因高不透明度基元导致的**局部极小值**问题，提升细节区域渲染质量。
- 周期性重定位与 4D 初始化策略分别有助于控制基元数量、提升快速运动建模能力。
- 方法支持**实时渲染**（450+ FPS @ 1080p），在质量与效率上均优于 4DGS 与 STGS。

## 7. 优点

- **表示创新性强**：打破规范空间约束，提出“任意时间、任意位置”的自由高斯基元，思路简洁而有效。
- **运动建模简单高效**：线性运动函数 + 时间不透明度函数，参数少、易优化，避免 4DGS/STGS 中角空间或多项式带来的优化困难。
- **训练策略完备**：4D 正则化、周期性重定位、4D 初始化三者协同，针对性解决优化与效率问题。
- **实验全面且公平**：在多个数据集上与众多 SOTA 方法对比，并对 4DGS/STGS 调整相机近平面以最大化漂浮物去除，尽量保证公平。
- **质量与速度兼得**：在提升 PSNR 的同时保持 450+ FPS 的实时渲染能力。
- **可复现性承诺**：论文明确表示将公开代码。

## 8. 不足与局限

- **重建耗时长**：每个动态场景仍需约 1 小时的逐场景优化，无法做到免优化重建。
- **不支持重光照（relighting）**：当前表示仅面向新视角合成，未建模表面法线与材质属性。
- **消融实验覆盖有限**：仅在 SelfCap 的 dance1 单序列上做消融，未在多个数据集/场景上验证各组件泛化性。
- **资源信息不完整**：未报告显存占用、多卡情况、总实验算力开销等细节。
- **对比公平性细节**：虽然对 4DGS/STGS 调整了近平面设置，但其他基线是否经过同等调优未完全说明。
- **应用限制**：方法依赖多视角同步视频采集，对稀疏视角或单目场景的适用性未验证。
- **数据偏差风险**：自采集数据集场景数量有限（8 个），且以人物日常活动为主，对更广泛动态场景的泛化能力有待进一步验证。

（完）
