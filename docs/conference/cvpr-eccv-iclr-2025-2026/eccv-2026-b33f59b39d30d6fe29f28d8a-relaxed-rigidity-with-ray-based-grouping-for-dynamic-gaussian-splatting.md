---
title: Relaxed Rigidity with Ray-based Grouping for Dynamic Gaussian Splatting
title_zh: 基于射线分组的松弛刚性动态高斯泼溅
authors: "Junoh Lee, Junmyeong Lee, Yeon-Ji Song, Inhwan Bae, Jisu Shin, Hae-Gon Jeon, Jin-Hwa Kim"
date: 2026
publication_date: 2026
publication_date_precision: year
publication_date_source: conference year only; exact release date unverified
publication_date_kind: unknown
pdf: "https://media.eventhosts.cc/Conferences/ECCV2026/pdfs/6640.pdf"
tags: ["query:dr"]
score: 9.0
evidence: 基于射线分组的动态高斯泼溅保持四维几何
tldr: 用三维高斯泼溅重建动态场景前景广阔，但多数方法难以让高斯运动符合真实物理动态，在单目视频中尤为突出，运动不一致会破坏局部几何结构并降低重建质量，因此许多方法依赖光流或二维轨迹等外部先验。本文提出基于射线分组的方法，在四维场景中显式保持高斯随时间的局部几何结构，使运动更连贯。实验表明该方法在单目视频数据集上提升了动态重建质量并减少对外部先验的依赖。其贡献在于以几何结构一致性约束高斯运动，推进了动态高斯泼溅的物理合理性。
source: ECCV-2026-Accepted-Program
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-b33f59b39d30d6fe29f28d8a/fig-001.webp\", \"caption\": \"\", \"page\": 2, \"index\": 1, \"width\": 800, \"height\": 800}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-b33f59b39d30d6fe29f28d8a/fig-002.webp\", \"caption\": \"\", \"page\": 2, \"index\": 2, \"width\": 800, \"height\": 800}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-b33f59b39d30d6fe29f28d8a/fig-003.webp\", \"caption\": \"\", \"page\": 2, \"index\": 3, \"width\": 272, \"height\": 800}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-b33f59b39d30d6fe29f28d8a/fig-004.webp\", \"caption\": \"\", \"page\": 2, \"index\": 4, \"width\": 596, \"height\": 744}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-b33f59b39d30d6fe29f28d8a/fig-005.webp\", \"caption\": \"\", \"page\": 2, \"index\": 5, \"width\": 555, \"height\": 760}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-b33f59b39d30d6fe29f28d8a/fig-006.webp\", \"caption\": \"\", \"page\": 2, \"index\": 6, \"width\": 266, \"height\": 800}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-b33f59b39d30d6fe29f28d8a/fig-007.webp\", \"caption\": \"\", \"page\": 2, \"index\": 7, \"width\": 593, \"height\": 558}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-b33f59b39d30d6fe29f28d8a/fig-008.webp\", \"caption\": \"\", \"page\": 5, \"index\": 8, \"width\": 406, \"height\": 655}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-b33f59b39d30d6fe29f28d8a/fig-009.webp\", \"caption\": \"\", \"page\": 5, \"index\": 9, \"width\": 452, \"height\": 686}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-b33f59b39d30d6fe29f28d8a/fig-010.webp\", \"caption\": \"\", \"page\": 5, \"index\": 10, \"width\": 605, \"height\": 644}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-b33f59b39d30d6fe29f28d8a/fig-011.webp\", \"caption\": \"\", \"page\": 5, \"index\": 11, \"width\": 664, \"height\": 349}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-b33f59b39d30d6fe29f28d8a/fig-012.webp\", \"caption\": \"\", \"page\": 5, \"index\": 12, \"width\": 417, \"height\": 374}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-b33f59b39d30d6fe29f28d8a/fig-013.webp\", \"caption\": \"\", \"page\": 5, \"index\": 13, \"width\": 325, \"height\": 628}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-b33f59b39d30d6fe29f28d8a/fig-014.webp\", \"caption\": \"\", \"page\": 5, \"index\": 14, \"width\": 793, \"height\": 1409}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-b33f59b39d30d6fe29f28d8a/fig-015.webp\", \"caption\": \"\", \"page\": 10, \"index\": 15, \"width\": 274, \"height\": 491}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-b33f59b39d30d6fe29f28d8a/fig-016.webp\", \"caption\": \"\", \"page\": 10, \"index\": 16, \"width\": 274, \"height\": 491}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-b33f59b39d30d6fe29f28d8a/fig-017.webp\", \"caption\": \"\", \"page\": 10, \"index\": 17, \"width\": 274, \"height\": 491}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-b33f59b39d30d6fe29f28d8a/fig-018.webp\", \"caption\": \"\", \"page\": 10, \"index\": 18, \"width\": 274, \"height\": 491}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-b33f59b39d30d6fe29f28d8a/fig-019.webp\", \"caption\": \"\", \"page\": 10, \"index\": 19, \"width\": 274, \"height\": 491}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-b33f59b39d30d6fe29f28d8a/fig-020.webp\", \"caption\": \"\", \"page\": 10, \"index\": 20, \"width\": 274, \"height\": 491}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-b33f59b39d30d6fe29f28d8a/fig-021.webp\", \"caption\": \"\", \"page\": 10, \"index\": 21, \"width\": 274, \"height\": 491}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-b33f59b39d30d6fe29f28d8a/fig-022.webp\", \"caption\": \"\", \"page\": 10, \"index\": 22, \"width\": 274, \"height\": 491}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-b33f59b39d30d6fe29f28d8a/fig-023.webp\", \"caption\": \"\", \"page\": 10, \"index\": 23, \"width\": 274, \"height\": 491}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-b33f59b39d30d6fe29f28d8a/fig-024.webp\", \"caption\": \"\", \"page\": 10, \"index\": 24, \"width\": 274, \"height\": 491}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-b33f59b39d30d6fe29f28d8a/fig-025.webp\", \"caption\": \"\", \"page\": 10, \"index\": 25, \"width\": 274, \"height\": 491}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-b33f59b39d30d6fe29f28d8a/fig-026.webp\", \"caption\": \"\", \"page\": 10, \"index\": 26, \"width\": 274, \"height\": 491}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-b33f59b39d30d6fe29f28d8a/fig-027.webp\", \"caption\": \"\", \"page\": 10, \"index\": 27, \"width\": 274, \"height\": 491}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-b33f59b39d30d6fe29f28d8a/fig-028.webp\", \"caption\": \"\", \"page\": 10, \"index\": 28, \"width\": 274, \"height\": 491}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-b33f59b39d30d6fe29f28d8a/fig-029.webp\", \"caption\": \"\", \"page\": 10, \"index\": 29, \"width\": 274, \"height\": 491}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-b33f59b39d30d6fe29f28d8a/fig-030.webp\", \"caption\": \"\", \"page\": 10, \"index\": 30, \"width\": 274, \"height\": 491}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-b33f59b39d30d6fe29f28d8a/fig-031.webp\", \"caption\": \"\", \"page\": 10, \"index\": 31, \"width\": 274, \"height\": 491}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-b33f59b39d30d6fe29f28d8a/fig-032.webp\", \"caption\": \"\", \"page\": 10, \"index\": 32, \"width\": 274, \"height\": 491}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-b33f59b39d30d6fe29f28d8a/fig-033.webp\", \"caption\": \"\", \"page\": 14, \"index\": 33, \"width\": 536, \"height\": 385}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-b33f59b39d30d6fe29f28d8a/fig-034.webp\", \"caption\": \"\", \"page\": 14, \"index\": 34, \"width\": 536, \"height\": 385}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-b33f59b39d30d6fe29f28d8a/fig-035.webp\", \"caption\": \"\", \"page\": 14, \"index\": 35, \"width\": 536, \"height\": 385}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-b33f59b39d30d6fe29f28d8a/fig-036.webp\", \"caption\": \"\", \"page\": 14, \"index\": 36, \"width\": 536, \"height\": 385}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-b33f59b39d30d6fe29f28d8a/fig-037.webp\", \"caption\": \"\", \"page\": 14, \"index\": 37, \"width\": 473, \"height\": 339}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-b33f59b39d30d6fe29f28d8a/fig-038.webp\", \"caption\": \"\", \"page\": 14, \"index\": 38, \"width\": 473, \"height\": 339}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-b33f59b39d30d6fe29f28d8a/fig-039.webp\", \"caption\": \"\", \"page\": 14, \"index\": 39, \"width\": 473, \"height\": 339}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-b33f59b39d30d6fe29f28d8a/fig-040.webp\", \"caption\": \"\", \"page\": 14, \"index\": 40, \"width\": 473, \"height\": 339}]"
motivation: 动态高斯泼溅难以使高斯运动符合真实物理动态，单目视频中易破坏局部几何结构。
method: 提出基于射线分组的方法，在四维场景中显式保持高斯随时间的局部几何结构。
result: 在单目视频数据集上提升了动态重建质量，并减少对光流等外部先验的依赖。
conclusion: 以几何一致性约束高斯运动，提升了动态高斯泼溅重建的物理合理性。
---

## Abstract
The reconstruction of dynamic 3D scenes using 3D GaussianSplatting has shown significant promise. A key challenge, however, re-mains in modeling realistic motion, as most methods fail to align the mo-tion of Gaussians with real-world physical dynamics. This misalignmentis particularly problematic for monocular video datasets, where failingto maintain coherent motion undermines local geometric structure, ulti-mately leading to degraded reconstruction quality. Consequently, manystate-of-the-art approaches rely heavily on external priors, such as opti-cal flow or 2D tracks, to enforce temporal coherence. In this work, wepropose a novel method to explicitly preserve the local geometric struc-ture of Gaussians across time in 4D scenes. Our core idea is to introducea view-space ray grouping strategy that clusters Gaussians intersectedby the same ray, considering only those whose α-blending weights ex-ceed a threshold. We then apply constraints to these groups to maintaina consistent spatial distribution, effectively preserving their local geom-etry. This approach enforces a more locally coherent motion model byensuring that local geometry remains stable over time, eliminating thereliance on external guidance. We demonstrate the efficacy of our methodby integrating it into two distinct baseline models. Extensive experimentson challenging monocular datasets show that our approach significantlyoutperforms existing methods, achieving superior temporal consistencyand reconstruction quality.

---

## 论文详细总结（自动生成）

# 论文总结：《Relaxed Rigidity with Ray-based Grouping for Dynamic Gaussian Splatting》

## 1. 核心问题与研究动机

- **背景**：3D Gaussian Splatting（3DGS）因其显式表示与高效训练/渲染，被广泛扩展到动态场景（4DGS）。但在单目视频下，高斯的运动估计本质上是欠约束的病态问题，常出现"过约束"或"欠约束"。
- **核心痛点**：
  - **依赖外部先验**：多数 SOTA 方法（如 MotionGS、Shape of Motion）依赖光流、2D 轨迹、单目深度等外部模型提供运动监督。这些先验定义在 2D 屏幕空间而非底层 3D 几何，只能提供间接且可能不一致的监督，误差与歧义会传播到优化过程。
  - **严格刚性假设的缺陷**：以 KNN 分组 + ARAP 为代表的刚性约束，仅依据欧氏距离分组，**忽略了高斯原语自身的尺度、不透明度等属性**，且无法适应拓扑变化与非刚性的真实运动。
- **整体含义**：论文主张**不依赖任何外部先验**，仅从图像监督中让动态 3DGS 学到局部一致的物理运动，从而在保持局部几何结构的同时允许非刚性形变。

## 2. 方法论

### 2.1 核心思想
利用 3DGS 光栅化管线**本身已按射线对高斯排序并做 α 混合**这一机制，把它"复用"为分组函数：同一条视线射线、α 混合权重超过阈值的高斯构成一个运动一致组，再对组内施加"松弛刚性"约束。

### 2.2 关键技术细节

- **射线分组（Ray-based Grouping, RG）**
  - 对每个像素 $p_j$，定义组 $N_j = \{G_i \mid w_i > \tau\}$，其中 $w_i = T_i(1-e^{-\alpha_i})$ 为 3DGS 的 α 混合贡献权重。
  - 阈值 $\tau$ 充当**隐式、遮挡感知的过滤器**：不透明遮挡物后透射率急剧衰减，因此过滤后自然只保留未被遮挡表面上的空间连续高斯，避免前景/背景纠缠。
  - 相比 KNN 的固定 20 邻居，该策略**组大小高度自适应**（图 3 显示分布范围很宽），可覆盖细结构到稠密体积，且几乎不引入额外计算开销（复用光栅化排序结果）。

- **运动一致性正则（Motion Coherence Regularization, MCR）**
  - 位移 $d_{i,t} = \mu_{i,t+\Delta t} - \mu_{i,t}$，组均值 $\bar d_{N_j,t}$。
  - 损失 $L_{MCR} = 1 - \frac{d_{i,t}\cdot \bar d_{N_j,t}}{\|d_{i,t}\|\|\bar d_{N_j,t}\|+\epsilon}$（余弦相似度）。
  - **只约束方向一致性，不惩罚位移幅值差异**，仅作用于 $\|d_{i,t}\| > 0.0001$ 的运动高斯——这正是"松弛刚性"的关键，避免退化为严格刚性平移。

- **谱正则（Spectral Regularization, SR）**
  - 计算组内高斯位置协方差矩阵 $K_t$、$K_{t+\Delta t}$，对其升序特征值 $\sigma_{t,r}$ 施加 Huber 损失：$L_{SR} = \sum_{r\in\{1,2,3\}} \text{Huber}(\sigma_{t,r}, \sigma_{t+\Delta t,r})$。
  - 仅匹配**特征值谱**，对刚性旋转不变，允许灵活非刚性形变，同时保持局部形状统计与空间体积；且不最小化整体尺度，避免组内收缩。只对含 1 个以上高斯的组生效。
  - 对比的 ARAP 基线（式 12）通过对齐局部旋转并惩罚残差失真来施加严格点对点刚性，仅用于消融对比。

- **Welford 在线协方差**：为高效计算沿射线的协方差，采用 Welford 递推算法（式 13–14），可在单遍（single pass）内完成并嵌入光栅化管线。

- **最终目标函数**：$L = (1-\lambda_{dssim})L_1 + \lambda_{dssim}L_{dssim} + \lambda_{MCR}L_{MCR} + \lambda_{SR}L_{SR}$。

## 3. 实验设计

- **数据集 / 场景**
  - **D-NeRF**：8 个合成形变场景（360° 单目），800×800，剔除 Lego 场景（训练/测试时间不对齐）。
  - **HyperNeRF**：真实场景（噪声、光照变化、拓扑变化），使用 vrig 划分（手持双摄，左右交替取帧训练），536×960，COLMAP 估位姿，点云来自 RTD。
  - **NeRF-DS**：7 个含镜面反射的真实场景，480×270，左摄训练/右摄测试。
- **Benchmark 指标**：D-NeRF 用 PSNR/SSIM/LPIPS_V；HyperNeRF 用 PSNR/MS-SSIM/LPIPS_A；NeRF-DS 用 PSNR/SSIM/MS-SSIM/LPIPS_V。
- **对比方法 / 集成基线**：将正则项插入 **4 个代表性 4DGS 框架**——RTD（HexPlanes 形变场）、MoDec-GS（scaffold 表示）、Grid4D（hash-grid 形变编码）三个形变场类，以及 Ex4DGS（样条轨迹参数化）。另与 NeRF、D-NeRF、TiNeuVox、HyperNeRF、NeRF-DS、3D-GS、D3DGS、GaGS 等对比。
- **消融实验**：以 RTD 为基础，对比 KNN vs RG 分组、ARAP vs MCR/SR 各组件移除、以及 $\tau$、$\lambda_{MCR}$、$\lambda_{SR}$、时间间隔的超参分析（Trex 场景），并做轨迹可视化。

## 4. 资源与算力

- **明确信息**：所有实验在**单张 NVIDIA RTX 3090 GPU** 上完成；基于各基线官方实现，保持基线架构与超参不变。
- **训练开销**：引入正则后训练时间约增加 **2 倍**（主要来自光栅化中的协方差处理与 SVD）；但在 Full 配置下，RG 比 KNN 分组**快 6%–25%**。推理/渲染阶段无额外开销。
- **未明确**：论文未报告总训练时长（小时/天）、总 GPU 卡数（仅提及单卡）、能耗或多次运行方差，也未给出各场景具体训练迭代数。

## 5. 实验数量与充分性

- **规模**：3 个数据集 × 4 个基线模型的组合集成实验 + 定量表格（Tab. 1）；1 组消融（Tab. 2，RTD 上覆盖 D-NeRF 与 HyperNeRF 平均结果）；1 组超参分析（Tab. 3，Trex 单场景）；2 组定性对比（图 4、图 5，覆盖 Trex、Jumping Jacks、Broom、3D Printer、Sieve、Basin、Bell）；1 组轨迹可视化（图 7，5 个场景）。
- **充分性评价**：
  - **优点**：跨 4 个基线、3 个数据集验证"模型无关性"，覆盖合成与真实、刚性与镜面/拓扑变化场景，对比方法数量较多，公平性较好（保持基线架构与超参不变，仅加正则）。
  - **不足**：
    - 消融与超参分析**仅在 RTD 单模型、部分单场景**上进行，未在全部 4 个基线上验证各组件贡献；
    - 超参分析只用一个场景（Trex），统计代表性有限；
    - **摘要称集成到"两个基线"，正文实际为四个**，存在表述不一致；
    - 未报告多次运行的均值/方差或显著性检验；
    - 未与同样使用外部先验的方法（如 Shape of Motion、MotionGS）做直接定量对照，因而"消除对先验依赖"的论点缺少直接公平对比支撑。

## 6. 主要结论与发现

- 在全部基线与数据集上**一致提升重建质量**：D-NeRF 上相对基线平均提升 PSNR **+1.19 dB**（Ex4DGS +1.11、RTD +1.10、MoDec-GS +2.35、Grid4D +0.20）；Grid4D+Ours 取得最佳 PSNR **42.20**；HyperNeRF 上 Grid4D+Ours 取得最高 MS-SSIM **0.856**；在更难的 NeRF-DS 上提升尤其显著（MoDec-GS +0.83 dB）。
- 定性上能保留细结构（扫帚把手、手指、牙齿、鸡的眼睛），减少物体消失与形状扭曲；轨迹可视化显示基线出现轨迹错乱/漂移，本方法轨迹更结构化、紧贴物体表面。
- 结论：**物理合理的运动约束可在不依赖外部先验的前提下显著改善动态 3DGS 重建**，且该正则与现有方法互补、模型无关。

## 7. 优点

- **无需外部先验**：摆脱光流/2D 轨迹/深度的依赖，避免 2D 代理监督的误差传播。
- **巧妙复用光栅化**：把 α 混合的可见性排序当作分组函数，遮挡感知、组大小自适应，且分组几乎零额外成本，训练时无结构改动即可插入任意 4DGS 模型。
- **"松弛"设计合理**：MCR 只约束方向、SR 只匹配特征值谱，兼顾一致性与非刚性形变自由，明显优于 KNN+ARAP 的严格刚性。
- **工程效率**：Welford 单遍在线协方差计算，可嵌入渲染管线；RG 比 KNN 更快。
- **验证面较广**：4 个异构基线（形变场 / scaffold / hash-grid / 样条）均获提升，泛化性强。

## 8. 不足与局限

- **训练成本翻倍**：约 2× 训练时间，HyperNeRF 上开销更明显（协方差与 SVD 计算），对大规模场景的可扩展性存疑。
- **依赖可见性分组**：仅对射线可见且权重超阈的高斯分组，**被遮挡或贡献低的高斯得不到约束**；长时遮挡后重现的物体会如何演化未讨论。
- **阈值与超参敏感**：$\tau$ 过大会丢弃有效高斯、过小会引入噪声；$\lambda_{MCR}$ 过大会过约束非刚性运动，论文承认需逐数据集调参。
- **消融覆盖有限**：仅在 RTD 上做完整消融，超参分析仅单场景，结论的普适性证据不够强。
- **缺少直接对照**：未与基于外部先验的 SOTA 方法在同设置下定量比较，"消除先验依赖"的优势缺少直接证据。
- **算力说明不完整**：仅单张 RTX 3090，未报告总训练时长、重复实验统计，复现成本与稳定性难以评估。
- **应用限制**：面向单目视频，未验证多视角/大尺度室外场景；极端拓扑变化（如物体分裂/合并）下松弛刚性的表现仍待验证；摘要与正文关于基线数量的表述不一致。

（完）
