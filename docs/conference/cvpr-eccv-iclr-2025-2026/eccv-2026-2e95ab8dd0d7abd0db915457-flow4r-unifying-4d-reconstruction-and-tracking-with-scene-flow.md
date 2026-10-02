---
title: "Flow4R: Unifying 4D Reconstruction and Tracking with Scene Flow"
title_zh: Flow4R：用场景流统一4D重建与跟踪
authors: "Shenhan Qian, Ganlin Zhang, Elliott (Shangzhe) Wu, Daniel Cremers"
date: 2026
publication_date: 2026
publication_date_precision: year
publication_date_source: conference year only; exact release date unverified
publication_date_kind: unknown
pdf: "https://media.eventhosts.cc/Conferences/ECCV2026/pdfs/10079.pdf"
tags: ["query:dr"]
score: 9.0
evidence: 用场景流统一4D重建与跟踪
tldr: 动态三维场景的重建与跟踪是计算机视觉的基础难题，现有方法常将几何与运动解耦：静态多视图重建假设世界刚性，动态跟踪则依赖显式自运动估计或独立物体运动模型。Flow4R提出统一框架，以相对场景流作为连接三维结构、相机自运动与动态物体运动的中心表示。给定两视图输入，共享ViT预测三维点位置、场景流、位姿权重与置信图，实现几何与运动的联合建模。
source: ECCV-2026-Accepted-Program
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-2e95ab8dd0d7abd0db915457/fig-001.webp\", \"caption\": \"\", \"page\": 2, \"index\": 1, \"width\": 1435, \"height\": 685}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-2e95ab8dd0d7abd0db915457/fig-002.webp\", \"caption\": \"\", \"page\": 7, \"index\": 2, \"width\": 433, \"height\": 483}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-2e95ab8dd0d7abd0db915457/fig-003.webp\", \"caption\": \"\", \"page\": 7, \"index\": 3, \"width\": 557, \"height\": 286}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-2e95ab8dd0d7abd0db915457/fig-004.webp\", \"caption\": \"\", \"page\": 7, \"index\": 4, \"width\": 613, \"height\": 531}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-2e95ab8dd0d7abd0db915457/fig-005.webp\", \"caption\": \"\", \"page\": 7, \"index\": 5, \"width\": 518, \"height\": 363}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-2e95ab8dd0d7abd0db915457/fig-006.webp\", \"caption\": \"\", \"page\": 13, \"index\": 6, \"width\": 512, \"height\": 512}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-2e95ab8dd0d7abd0db915457/fig-007.webp\", \"caption\": \"\", \"page\": 13, \"index\": 7, \"width\": 645, \"height\": 652}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-2e95ab8dd0d7abd0db915457/fig-008.webp\", \"caption\": \"\", \"page\": 13, \"index\": 8, \"width\": 646, \"height\": 652}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-2e95ab8dd0d7abd0db915457/fig-009.webp\", \"caption\": \"\", \"page\": 13, \"index\": 9, \"width\": 512, \"height\": 507}]"
motivation: 现有方法将几何与运动解耦，静态重建假设刚性，动态跟踪依赖显式自运动估计。
method: Flow4R以相对场景流为中心表示，用共享ViT从两视图预测三维点位置、场景流、位姿权重与置信图。
result: 该流中心公式统一了三维结构、相机自运动与动态物体运动。
conclusion: 为4D重建与跟踪提供了统一的场景流框架。
---

## Abstract
Reconstructing and tracking dynamic 3D scenes is a funda-mental challenge in computer vision. Existing methods typically decou-ple geometry from motion: static multi-view reconstruction systems as-sume a rigid world, whereas dynamic tracking frameworks rely on explicitego-motion estimation or separate object motion models. In this work,we propose Flow4R, a unified framework that treats relative scene flowas the central representation linking 3D structure, camera ego-motion,and dynamic object motion. Given a two-view input, Flow4R employs ashared Vision Transformer to predict a compact, pixel-aligned propertyset comprising 3D point positions, scene flow, pose weights, and con-fidence maps. This flow-centric formulation allows local geometry andbidirectional motion to be jointly inferred in a single feedforward pass,eliminating the need for explicit pose regression heads or complex bundleadjustment. By training jointly on static and dynamic datasets, Flow4Rachieves state-of-the-art performance on 4D reconstruction and trackingbenchmarks, demonstrating the power of the flow-centric formulation forspatiotemporal scene understanding.

---

## 论文详细总结（自动生成）

# Flow4R 论文中文结构化总结

## 1. 核心问题与研究动机

- **核心问题**：动态三维场景的**重建与跟踪**是计算机视觉的基础难题，其本质需要同时推理**几何、运动与时间**三个耦合因素。
- **现有方法的割裂**：
  - 静态多视图重建系统（如 DUSt3R、VGGT 及其变体）默认世界是**刚性**的，将所有点预测在共享参考坐标系中，在动态场景下参考系选择存在歧义。
  - 动态跟踪框架则依赖**显式自运动估计**（如掩码动态区域后估计相机位姿）或**独立的物体运动模型**（如为不同时间戳设置单独的回归头）。
  - 这种"几何与运动解耦"的做法导致流程脆弱、难以跨场景与运动类型泛化。
- **核心洞察**：运动是相对的——图像中观测到的运动是物体运动与观测者自运动的叠加；而"哪里是静态参考系"本质上是**任务依赖且主观**的（论文以"自动扶梯"为例说明参考系的切换）。因此，更通用的方案是预测**相对运动**。
- **关键选择**：**场景流（scene flow）** 定义在相机空间中，天然**与参考坐标系的选择无关**，可作为连接三维结构、相机自运动与动态物体运动的统一中心表示。
- **整体含义**：Flow4R 将 4D 感知完全重述为场景流推理，用一次前向传播同时完成重建与跟踪，去除显式位姿回归头与复杂光束法平差（bundle adjustment）。

## 2. 方法论

### 2.1 核心思想
- 给定一对图像 $(I, I')$，预测一组紧凑的**像素对齐属性集** $S(I,I') = \{P, F, W, C\}$：
  - $P \in \mathbb{R}^{H\times W \times 3}$：局部欧氏空间中的**点位置图**；
  - $F \in \mathbb{R}^{H\times W \times 3}$：**场景流图**，将 $I$ 中的点映射到 $I'$ 的坐标系与时间戳；
  - $W \in (0,1)^{H\times W}$：**位姿权重图**（归一化，$\sum W_i = 1$），标识哪些像素对相机位姿估计可靠；
  - $C \in (1,\infty)^{H\times W}$：**置信度图**。
- 对称地定义 $S(I',I)=\{P',F',W',C'\}$，双向预测使参数在编码器、解码器与预测头之间**完全共享**。

### 2.2 场景流分解（关键技术细节）
- **流映射**：$P_i^{vt} = P_i + F_i$，其中 $v,t$ 表示从 $I$ 到 $I'$ 的视角与时间切换。
- **加权最小二乘求解相机位姿**：
  $\hat{T} = \arg\min_{T \in SE(3)} \sum_{i=1}^{HW} W_i \|P_i^{vt} - T P_i\|^2$
- **刚性分量（相机运动）**：$F_i^v = P_i^v - P_i$，其中 $P_i^v = \hat{T} P_i$。
- **非刚性分量（物体运动）**：$F_i^t = F_i - F_i^v$。
- **3D 点跟踪**：$P_i^t = \hat{T}^{-1} P_i^{vt} = \hat{T}^{-1}(P_i + F_i)$。
- **焦距估计**：$\hat{f} = \arg\min_f \sum_i \|\hat{p}_i - \pi(f,c,P_i)\|^2$。
- **光流**：将 $P_i$ 与 $P_i^{vt}$ 投影到图像平面后作差 $f_i = p_i^{vt} - p_i$。

### 2.3 网络与训练策略
- **架构**：基于双视图 Transformer（借鉴 DUSt3R/MASt3R 的跨注意力范式），编码器、解码器、预测头共享参数；对称公式省去了人工构造对称图像对。
- **序列处理**：采用 **锚定连接（anchored connections）** 范式（类 St4RTrack），将序列帧与单一锚帧配对。由于同时预测锚视图的局部点图，可用锚点平均范数 $s_n$ 对齐各配对预测的**度量尺度**，实现无需全局光束法平差的长期一致跟踪。
- **归一化**：遵循 DUSt3R，按点图均值欧氏范数归一化以实现尺度不变性。
- **损失函数（共 5 项）**：
  - **点位置损失** $L_P$：置信度加权回归，含不确定性正则项 $-\alpha \log C_i$。
  - **3D 运动损失** $L_F$：监督 $P^{vt}$（而非直接监督 $F$），来源包括场景流、光流、3D 点跟踪标注。
  - **2D 运动损失** $L_f$：投影坐标上的光流/2D 跟踪监督（不加置信度权重，因处于 2D 投影空间）。
  - **位姿权重损失** $L_W$：**自监督**——通过可微位姿求解器反传，且对 $P$、$P^{vt}$ 阻断梯度，使 $W$ 成为唯一被优化参数，迫使网络自动学会"屏蔽动态/远景/遮挡/反光像素、聚焦稳定静态结构"。
  - **刚性运动损失** $L_{F^v}$：利用真值相机位姿诱导的刚性流增强监督；动态数据集上用 $sg(W_i)\times HW$ 降权非刚性区域，静态数据集上权重恒为 1。
  - **总损失**：$L = \lambda_1 L_P + \lambda_2 L_F + \lambda_3 L_f + \lambda_4 L_W + \lambda_5 L_{F^v}$，其中 $\lambda_1=1$，$\lambda_2=\lambda_4=\lambda_5=0.5$，$\lambda_3=0.3$，$\alpha=0.2$。
- **一个重要的实现选择**：尽管 $F$ 与 $P^{vt}$ 数学等价（$F = P^{vt} - P$），但实验发现**直接预测并监督 $P^{vt}$ 显著优于预测 $F$**，因为 $P^{vt}$ 更贴近最终评估指标（绝对点位置），可减少中间变换的误差累积。

## 3. 实验设计

### 3.1 数据集
- **训练数据**：静态+动态、真实+合成的混合数据集，共 22 个来源，包括 Habitat、BlendedMVS、MegaDepth、ARKitScenes、CO3D、Static Scenes 3D、ScanNet++、Waymo、TartanAir、UnReal4K、WildRGBD、DL3DV、MapFree、ScanNet、HyperSim、Virtual KITTI 2、Spring、PointOdyssey、Dynamic Replica、Kubric、OmniWorld-Game。部分使用 DUSt3R、CUT3R、MonST3R、CoTracker 的预处理数据。
- **标注类型**：Virtual KITTI 2 提供真值场景流；Spring、Dynamic Replica、OmniWorld-Game 提供光流；PointOdyssey、Dynamic Replica、Kubric 提供 3D 点跟踪。

### 3.2 基准与评价指标
- **WorldTrack 基准**（遵循 St4RTrack）：
  - **3D 点跟踪**：Aria Digital Twin（ADT）、Panoptic Studio（PS）两个真实数据集 + PointOdyssey（PO）、Dynamic Replica（DR）两个合成数据集；指标为 **APD3D**（δ₃D ∈ {0.1m, 0.3m, 0.5m, 1.0m}，前 64 帧平均），分"所有点"与"动态点"两类。
  - **动态 3D 重建**：PointOdyssey 与 TUM-Dynamics；指标为 APD3D 与 EPE。
- **对比方法**：3D 点跟踪对比 SpatialTracker（相机坐标系 3D 跟踪）、MonST3R、POMATO、St4RTrack；重建对比 DUSt3R、MASt3R、MonST3R（含 +GA 全局对齐变体）、POMATO、St4RTrack。

### 3.3 主要结果
- **3D 点跟踪（Tab. 1）**：Flow4R 在 ADT（78.6）、DR（78.5）、PO（71.1）上取得最优，PS 上略逊；参数仅 **0.4B**，少于多数基线（0.7B）。
- **3D 重建（Tab. 2）**：PointOdyssey 上 APD 81.00 / EPE 0.182 最优；TUM-Dynamics 上 APD 79.87 / EPE 0.202，略低于 St4RTrack（83.42 / 0.185），但优于所有其他方法及带后优化方法。
- **消融实验（Tab. 3）**：对比三种变体（预测 $F$ 回归 $\bar{F}$、预测 $F$ 回归 $\bar{P}^{vt}$、预测 $P^{vt}$ 回归 $\bar{P}^{vt}$），**直接预测 $P^{vt}$ 且回归 $\bar{P}^{vt}$** 在全部 6 个数据集/指标组合上最优。
- **运行时效率（Tab. 4）**：在 RTX PRO 6000 上，吞吐 26.8 pairs/s（St4RTrack 27.9），但显存占用 **3152 MB vs 6711 MB**，节省超过 50% VRAM。

## 4. 资源与算力

- **GPU**：8 张 NVIDIA A100/H100。
- **训练配置**：
  - 第一阶段：线性头，分辨率 224，训练 100 epoch，每 epoch 采样 90 万对；batch size 256。
  - 第二阶段：DPT 头，分辨率 512，随机宽高比，训练 100 epoch，每 epoch 采样 8.4 万对；batch size 64。
- **训练时长**：整体约 **4 天**。
- **优化器**：Adam，线性学习率 warmup（第一阶段 10 epoch，第二阶段 20 epoch）至峰值 1e-4，再按余弦曲线衰减至 1e-6；梯度裁剪最大范数 10。
- **初始化**：从 CroCo 初始化（而非多数基线那样从 DUSt3R/MASt3R/MonST3R 微调），原因是公式发生了变化。

## 5. 实验数量与充分性

- **实验组数概览**：
  - 3D 点跟踪：4 个数据集 × 2 类点（所有点/动态点）× 5 种方法对比。
  - 3D 重建：2 个数据集 × 2 个指标 × 9 种方法配置对比。
  - 运动表示消融：3 个变体 × 6 个数据集/指标组合。
  - 运行时效率：与最强基线 St4RTrack 的吞吐与显存对比。
  - 定性可视化：静态场景、动态跳跃机器人、远近视角静止火车、四人舞蹈四类场景，以及全局坐标系下的 3D 可视化。
- **充分性与客观性评估**：
  - **优点**：覆盖静态/动态、真实/合成、单目/多视图多类数据，且与 St4RTrack 采用完全相同的评测协议（WorldTrack），可比性较强；消融设计直接针对其核心设计选择（预测目标与监督目标），结论清晰。
  - **可商榷之处**：消融仅做了"运动表示"这一项，未对位姿权重损失的自监督机制、锚定连接 vs 局部连接、置信度共享等设计做系统性消融；消融实验仅训练了总 epoch 的一半，作者称"足以观察相对趋势"，但这会削弱绝对数值的说服力。
  - **公平性**：作者明确指出 POMATO 因顺序模型仅支持"他帧到锚帧"跟踪，故改用其成对模型评估，处理较为透明；但 Flow4R 从 CroCo 初始化而非 DUSt3R 微调，与其他基线在预训练起点上不完全对等。

## 6. 主要结论与发现

- 以**相对场景流为中心**的统一表示，可以同时承载 3D 结构、相机自运动与动态物体运动，无需显式位姿回归头或全局光束法平差。
- **联合静态与动态数据集**训练有效：静态场景用深度+相对位姿计算刚性流监督；动态场景通过可微位姿求解器**自监督学习位姿权重图**，自动分割静态参考区域并降权动态/远景/遮挡像素。
- 位姿权重图在推理时**可灵活调整或覆盖**，以按下游任务切换参考坐标系。
- 预测**局部点图（两视图都预测）** 使得用共享锚视图对齐任意帧对的度量尺度成为可能，实现一致 3D 轨迹跟踪。
- 实验证明：**直接预测 $P^{vt}$ 优于预测 $F$**，因其更贴近最终评估指标、避免误差累积。
- 在 4D 重建与跟踪基准上达到 SOTA 或极具竞争力的水平，且**参数量更少、显存占用降低 50% 以上**。

## 7. 优点

- **表示层面的创新**：将 4D 感知统一为场景流这一坐标系无关的表示，概念简洁且物理意义明确，从根本上回避了"参考系选择歧义"问题。

- **训练策略的自洽性**：位姿权重图 $W$ 完全通过自监督学习获得（阻断 $P$、$P^{vt}$ 的梯度，仅优化 $W$），无需任何"动态区域"标注即可自动学会聚焦静态结构，这与"运动是相对的、参考系是任务依赖的"这一核心洞察在方法论上高度一致。
- **工程效率显著**：0.4B 参数、显存占用仅为 St4RTrack 的约一半（3152 MB vs 6711 MB），在保持甚至超越精度的同时降低了部署门槛，说明统一表示并未以计算代价换取性能。
- **无需后处理**：去掉显式位姿回归头与全局光束法平差，端到端一次前向即输出结构、位姿、跟踪与光流，流程简洁、可微、易扩展。
- **评测规范透明**：沿用 WorldTrack 协议，与 St4RTrack 在数据划分、指标（APD3D、EPE）与帧数设定上完全对齐；对 POMATO 等不兼容顺序模型的处理方式明确交代，减少了"隐性不公平"的嫌疑。
- **监督信号利用充分**：同时利用场景流、光流、3D 点跟踪、真值位姿诱导的刚性流等多种异构标注，并通过统一到 $P^{vt}$ 这一共同预测目标上加以融合，避免了多任务头之间的表示冲突。
- **双向对称设计**：通过对称定义 $S(I,I')$ 与 $S(I',I)$ 并共享全部参数，天然获得双向预测能力，无需人工构造镜像样本，且为尺度对齐提供了锚视图依据。

## 8. 局限性与可改进之处

- **消融覆盖面偏窄**：论文仅针对"运动表示（预测 $F$ vs $P^{vt}$、监督 $\bar F$ vs $\bar P^{vt}$）"做了消融，而位姿权重损失的自监督机制、锚定连接 vs 局部连接、置信度图是否共享、双向预测的必要性等关键设计均缺少消融支撑，读者难以判断各模块的独立贡献。
- **消融训练不充分**：消融模型仅训练总 epoch 的一半，作者以"足以观察相对趋势"为由说明，但这使绝对数值与主实验不可直接比较，结论的稳健性打折。
- **预训练起点不完全对等**：Flow4R 从 CroCo 初始化，而多数基线（DUSt3R/MASt3R/MonST3R/St4RTrack）从更强的三维预训练权重微调。作者以"公式已变"解释，但这一差异可能同时影响公平性与可复现性。
- **个别基准上未达最优**：在 Panoptic Studio 的 3D 点跟踪上略逊于基线；在 TUM-Dynamics 的重建上 APD3D/EPE 均低于 St4RTrack（79.87/0.202 vs 83.42/0.185）。论文对此的解释与差距来源分析略显单薄。
- **动态场景下的尺度与长期漂移**：虽然用锚视图平均范数对齐度量尺度，但锚定连接本质上是"以单一锚帧为中心"的近似，在锚帧本身含大量动态内容或长时间序列中，尺度一致性与漂移控制仍缺乏定量分析。
- **评测基准的覆盖**：WorldTrack 的 3D 点跟踪数据集以室内/多人场景为主，缺少自动驾驶（如 Waymo 动态部分）与大规模户外动态场景的定量评测，尽管训练数据中包含 Waymo，但未见相应测试。
- **运行时对比维度有限**：效率仅与 St4RTrack 对比吞吐与显存，未给出与 MonST3R、POMATO 等更重基线（含后优化）的完整效率对照，也未报告训练成本与推理延迟随帧数增长的曲线。

## 9. 对领域的启发与潜在影响

- **"以相对运动为中心"的范式转移**：论文提出参考系选择本身是任务依赖且主观的，因此与其强行确定一个世界坐标系，不如直接预测坐标系无关的相对场景流。这一思路可推广到 SLAM、动态 NeRF/3DGS、机器人操作中的相对位姿估计等场景。
- **自监督位姿权重作为隐式动态分割**：将"哪些像素可信"交由可微位姿求解器反向优化，等价于让网络在训练中自发学习动态/静态分割，为无需标注的动态感知提供了新思路，也可能反过来服务于运动分割、异常检测等任务。
- **统一表示降低系统复杂度**：把结构、相机运动、物体运动、光流、3D 跟踪统一到 $\{P, F, W, C\}$ 一组像素对齐属性上，提示未来 4D 基础模型可以用"共享解码器 + 多任务监督"的方式替代"多模块级联 + 后处理"的传统流水线。
- **监督目标的经验法则**：直接预测与最终评估指标对齐的物理量（$P^{vt}$ 而非 $F$）能减少中间变换的误差累积，这一发现对更广泛的多任务密集预测（如深度+光流联合估计）具有借鉴意义。
- **轻量化与实用的平衡**：在参数量与显存显著下降的前提下达到 SOTA/接近 SOTA，说明"统一表示"并不必然意味着模型膨胀，为可部署的 4D 感知系统提供了参考。

## 10. 总体评价

Flow4R 的核心贡献不在于单个模块的工程改进，而在于**重新定义了 4D 感知的问题表述**：把"重建 + 跟踪"从"先估计位姿、再分离动态物体"的解耦范式，转变为"直接预测坐标系无关的相对场景流"。这一表述在物理上自洽（运动相对性）、在实现上简洁（无位姿头、无 BA）、在效果上有竞争力（WorldTrack 上多项 SOTA、显存减半），并对"参考系歧义"这一长期困扰动态三维重建的问题给出了原理性的回应。

其主要不足在于实验验证的**广度与严谨性**：消融维度单一且训练不充分，预训练起点与其他基线不完全对等，个别基准上未达最优，长期序列的尺度一致性与漂移缺乏定量刻画。因此，论文的**方法论说服力强于其经验证据的完备性**——它更像一篇提出新范式的"观点 + 原型"论文，而非穷尽式验证的基准论文。

总体而言，Flow4R 为 4D 场景理解提供了一条清晰且具扩展性的技术路线：以场景流为统一接口，让几何、运动与时间在同一表示中自然耦合，其思想价值可能超过其当前的实验数字本身，值得后续在更大规模、更多模态（如多视图、事件相机、长序列）下进一步验证与拓展。

（完）
