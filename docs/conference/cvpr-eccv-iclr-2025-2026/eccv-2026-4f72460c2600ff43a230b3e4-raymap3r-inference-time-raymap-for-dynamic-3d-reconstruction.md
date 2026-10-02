---
title: "RayMap3R: Inference-Time RayMap for Dynamic 3D Reconstruction"
title_zh: RayMap3R：面向动态三维重建的推理时RayMap
authors: "Feiran Wang, Zezhou Shang, Gaowen Liu, Yan Yan"
date: 2026
publication_date: 2026
publication_date_precision: year
publication_date_source: conference year only; exact release date unverified
publication_date_kind: unknown
pdf: "https://media.eventhosts.cc/Conferences/ECCV2026/pdfs/6634.pdf"
tags: ["query:dr"]
score: 9.0
evidence: 免训练流式实时动态场景重建框架
tldr: 流式前馈三维重建可实时联合估计几何与相机位姿，但缺乏显式动态推理时会被运动物体干扰，产生伪影与漂移。本文提出免训练的流式框架RayMap3R，观察到RayMap预测存在静态场景偏置，据此构建双分支推理，通过对比RayMap与图像预测识别动态区域并在记忆更新中抑制其干扰，同时引入重置度量对齐与状态感知平滑以保持度量一致性。实验显示该方法能有效减轻运动物体带来的漂移，实现更稳健的实时动态场景重建。其价值在于无需训练即可为流式重建注入动态推理能力。
source: ECCV-2026-Accepted-Program
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-4f72460c2600ff43a230b3e4/fig-001.webp\", \"caption\": \"\", \"page\": 1, \"index\": 1, \"width\": 878, \"height\": 627}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-4f72460c2600ff43a230b3e4/fig-002.webp\", \"caption\": \"\", \"page\": 1, \"index\": 2, \"width\": 906, \"height\": 645}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-4f72460c2600ff43a230b3e4/fig-003.webp\", \"caption\": \"\", \"page\": 1, \"index\": 3, \"width\": 956, \"height\": 682}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-4f72460c2600ff43a230b3e4/fig-004.webp\", \"caption\": \"\", \"page\": 6, \"index\": 4, \"width\": 553, \"height\": 278}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-4f72460c2600ff43a230b3e4/fig-005.webp\", \"caption\": \"\", \"page\": 6, \"index\": 5, \"width\": 550, \"height\": 278}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-4f72460c2600ff43a230b3e4/fig-006.webp\", \"caption\": \"\", \"page\": 6, \"index\": 6, \"width\": 737, \"height\": 556}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-4f72460c2600ff43a230b3e4/fig-007.webp\", \"caption\": \"\", \"page\": 7, \"index\": 7, \"width\": 512, \"height\": 288}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-4f72460c2600ff43a230b3e4/fig-008.webp\", \"caption\": \"\", \"page\": 7, \"index\": 8, \"width\": 512, \"height\": 288}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-4f72460c2600ff43a230b3e4/fig-009.webp\", \"caption\": \"\", \"page\": 7, \"index\": 9, \"width\": 528, \"height\": 334}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-4f72460c2600ff43a230b3e4/fig-010.webp\", \"caption\": \"\", \"page\": 7, \"index\": 10, \"width\": 512, \"height\": 288}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-4f72460c2600ff43a230b3e4/fig-011.webp\", \"caption\": \"\", \"page\": 7, \"index\": 11, \"width\": 512, \"height\": 288}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-4f72460c2600ff43a230b3e4/fig-012.webp\", \"caption\": \"\", \"page\": 7, \"index\": 12, \"width\": 512, \"height\": 288}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-4f72460c2600ff43a230b3e4/fig-013.webp\", \"caption\": \"\", \"page\": 7, \"index\": 13, \"width\": 528, \"height\": 334}]"
motivation: 流式前馈重建缺乏动态推理，运动物体会导致伪影与漂移，影响实时重建质量。
method: 提出免训练流式框架，利用RayMap的静态偏置构建双分支对比识别动态区域，并加入重置度量对齐与状态感知平滑。
result: 在抑制运动物体干扰的同时保持度量一致性，减轻漂移并提升实时动态场景重建的稳健性。
conclusion: 无需训练即可为流式三维重建引入动态推理，提升实时重建在动态环境下的可靠性。
---

## Abstract
Streaming feed-forward 3D reconstruction enables real-timejoint estimation of scene geometry and camera poses from RGB images.However, without explicit dynamic reasoning, streaming models can beaffected by moving objects, causing artifacts and drift. In this work, wepropose RayMap3R, a training-free streaming framework for dynamicscene reconstruction. We observe that RayMap-based predictions exhibita static-scene bias, providing an internal cue for dynamic identification.Based on this observation, we construct a dual-branch inference schemethat identifies dynamic regions by contrasting RayMap and image pre-dictions, suppressing their interference during memory updates. We fur-ther introduce reset metric alignment and state-aware smoothing to pre-serve metric consistency and stabilize predicted trajectories. Our methodachieves state-of-the-art performance among streaming approaches ondynamic scene reconstruction across multiple benchmarks. The projectpage and code are available at https://raymap3r.github.io/.

---

## 论文详细总结（自动生成）

# RayMap3R 论文总结

## 1. 核心问题与整体含义

- **研究背景**：前馈三维重建模型（DUSt3R、MASt3R、VGGT 等）能从单目图像估计点云、深度和相机位姿，但多为离线范式，需先获得全部帧，且计算与内存随序列长度快速增长（200 帧可需约 48 GB）。
- **流式范式**：Spann3R、CUT3R、Point3R、StreamVGGT、TTT3R 等引入记忆机制（空间记忆库、隐式循环状态、显式点锚），实现恒定内存、高频实时推理。
- **核心痛点**：
  - 流式模型缺乏显式动态物体识别机制，训练数据中动态标注稀缺，逐帧处理历史上下文有限，易受运动物体干扰，产生伪影与相机漂移。
  - 逐帧预测会累积位姿噪声；长序列记忆遗忘导致的周期性重置会引入**度量失配（scale mismatch）**，误差持续累积。
  - 现有动态重建方法多依赖外部模块（光流估计、分割、跟踪），带来额外开销与域依赖，泛化差。
- **整体含义**：本文发现"仅用 RayMap 预测存在静态场景偏置"这一内在线索，将其转化为**免训练、无需外部模块**的动态识别信号，为流式重建注入动态推理能力，同时保持实时性与恒定内存。

## 2. 方法论

### 2.1 基础表示与记忆机制
- **RayMap**：H×W×6 的逐像素张量，编码每条光线的世界坐标原点 c 与单位方向 d（由内参 K 与外参 T=[R|τ] 决定）；c 对所有像素恒定，d 编码视线方向。
- **记忆机制**：采用 CUT3R/TTT3R 式隐式记忆，潜在状态 s_t 编码时刻 t 的场景理解；训练时图像 token f_t 与 RayMap token r_t 交互更新状态，推理时可仅凭图像或仅凭 RayMap 查询。

### 2.2 关键观察：RayMap 静态偏置
- 给定同一记忆状态 s_{t-1}，主分支（图像+RayMap）重建含动态前景的场景，而 RayMap-only 分支倾向重建静态背景、抑制运动物体。
- **归因**：① 训练集以静态场景为主、动态标注有限，模型形成静态先验；② RayMap token 仅编码相机几何、无外观线索，模型只能依赖记忆中时序一致的静态结构。
- **验证**：在 MPI Sintel、DAVIS 2017、TUM RGB-D 共 108 段序列上，两分支逐像素深度差与真值动态比例正相关（Spearman ρ=0.77，p<10⁻²²）。

### 2.3 双分支动态识别与记忆门控
- 两分支共享冻结状态 s_{t-1}：
  - 主分支：ŷ_main = Dec(f_t + r_t, s_{t-1})
  - RayMap 分支：ŷ_raymap = Dec(r'_t, s_{t-1})，其中 r'_t 由主分支预测位姿 T̂_t 重映射得到。
- 逐像素相对深度差 δ_i = |z_main − z_raymap| / |z_main|，越大越可能是动态内容。
- **聚合两步**：像素级分数经主分支置信度加权池化为图像 token 级分数 δ_tok；再借解码器状态 token 与图像 token 的交叉注意力权重 A_jk 投影为状态 token 级分数 δ_state。
- **静态权重**：α_t = σ(γ·(median(δ_state) − δ_state) / IQR(δ_state))，高 α 保留完整更新，低 α 被抑制；α_t 经指数移动平均增强时序稳定性。
- **状态更新**：s_t = s_{t-1} + α_t ⊙ Δs_t；另用像素级静态图构造加权全局特征，使位姿检索偏向静态区域。
- 预热期后逐帧执行，无需反向传播，内存恒定。

### 2.4 重置度量对齐（Reset Metric Alignment）
- 记忆周期性重置会使同一重复帧在重置前后产生不一致的相机参数与几何，表现为分段间尺度失配并传播为系统性漂移。
- 利用"重复帧在重置前后应重建一致"的性质，估计对齐两段点云重建的 **Sim(3) 变换**（含尺度与位姿偏移），并施加到新分段所有后续帧，恢复度量一致性。

### 2.5 状态感知平滑（State-Aware Smoothing）
- 定义状态变化信号 sc_t（Δs_t 的逐 token L2 范数均值，取门控更新前的完整变化量）与轨迹加速度 a_t = ‖d_t − d_{t−1}‖₂。
- 乘积 a_t×sc_t 同时刻画运动不规则性与模型不确定性，可降低单一信号的误判（匀速快速运动加速度低，不应过度平滑）。
- 平滑系数 β_t = 1/(1 + λ|a_t×sc_t|)，指数滤波帧间位移：d̂_t = β_t d_t + (1−β_t) d̂_{t−1}；乘积大时 β→0 抑制抖动，小时 β→1 保留原始位移。
- 递推位置 τ̂_t = τ̂_{t−1} + d̂_t，展开后为闭式轨迹（式 6），形成自适应衰减，完全在线、开销可忽略。

## 3. 实验设计

- **任务与数据集**：
  - **视频深度估计**：Sintel（动态合成）、KITTI（室外）、Bonn（室内）；指标 Abs Rel、δ<1.25；两种协议——逐序列尺度对齐（相对深度）与度量尺度（绝对尺度）。
  - **相机位姿估计**：Sintel（复杂动态）、TUM-dynamics（真实动态）、ScanNet（静态室内）；指标 ATE、RPE_t、RPE_r，采用 Sim(3) 对齐。
  - **三维重建**：7-Scenes（每场景 200 帧）；指标 Acc、Comp、NC、Chamfer，报告 Mean/Median/Min。
  - **定性**：DAVIS 动态视频对比 CUT3R、TTT3R。
- **对比方法**：
  - 流式：Spann3R、CUT3R、Point3R、StreamVGGT、TTT3R。
  - 离线（作参考）：DUSt3R、MASt3R、MonST3R、VGGT（及 GA 变体）。
- **分析实验**：
  - 推理速度与显存（Tab. 4，ScanNet，50/1000 视角）。
  - 组件消融（Tab. 5，以 CUT3R 为基座，R/M/S 组合共 5 组，覆盖三项任务）。
  - 静态偏置定量分析（Tab. 6，108 段序列，指标 disc、AUC、IoU、Spearman ρ）。

## 4. 资源与算力

- 论文明确提到推理速度与显存评测在**单张 NVIDIA RTX A6000 48GB GPU** 上完成。
- 由于方法为**免训练（training-free）**框架，论文未报告训练时长、GPU 数量或训练算力开销；其依赖的 CUT3R 骨干网络训练成本也未在文中说明。
- 评测显示：50 视角显存 9.2 GB / 13.8 FPS，1000 视角 9.4 GB / 13.8 FPS，内存不随序列增长。

## 5. 实验数量与充分性

- **规模**：三大主任务（深度、位姿、重建）+ 定性对比 + 三组分析实验（速度/显存、组件消融、静态偏置统计），覆盖合成与真实、动态与静态、室内与室外场景，数据面较广。
- **消融**：R、R+M、R+S、Full 共 5 种配置 × 3 项任务指标，能清晰拆分各组件贡献，设计合理。
- **静态偏置验证**：108 段序列、6631 帧、三类数据集，给出 disc/AUC/IoU/ρ 多角度统计，证据较扎实。
- **公平性**：与同类流式方法在相同协议（per-sequence 与 metric-scale、Sim(3) 对齐）下对比，离线方法单独标注为参考，比较方式基本客观。
- **不足**：仅在 CUT3R 单一骨干上验证；未与专门面向动态场景的方法（如 Easi3R、基于光流/分割的动态重建方案）直接对比；速度评测只在一个数据集、单卡上进行。

## 6. 主要结论与发现

- RayMap-only 预测的**静态偏置是普遍存在的**，可作为免训练动态识别信号（真实数据集 AUC>0.5，序列级 Spearman ρ 最高 0.900）。
- 在流式方法中，RayMap3R 在深度、位姿、三维重建三类任务上**整体领先**，动态场景（Sintel、TUM-dynamics）提升尤为显著。
- 组件贡献互补：双分支（R）对深度与重建提升最大；度量对齐（M）主要改善 Chamfer（全局点云一致性）；状态感知平滑（S）主要改善轨迹精度。
- 在静态 ScanNet 上与最优流式方法持平，说明动态过滤在无运动物体时不会损害性能。
- 保持恒定内存与实时推理（13.8 FPS），但相对 CUT3R 有约 30% 速度下降、显存从 6.4 GB 增至 9.2 GB。

## 7. 优点

- **免训练、即插即用**：无需额外标注、重训练或外部模块（光流/分割/跟踪），仅靠模型内在偏置实现动态识别。
- **观察新颖且验证充分**：将"RayMap-only 的静态偏置"转化为可用信号，并用跨数据集统计（相关性、AUC、IoU）系统支撑。
- **方法链条完整**：动态抑制（α 门控）、度量一致（Sim(3) 对齐）、轨迹稳定（β 平滑）三方面互补，分别针对记忆污染、尺度漂移、位姿噪声。
- **在线因果设计**：状态感知平滑为闭式递推，无需存储历史，开销可忽略。
- **实验覆盖广**：动态/静态、合成/真实、室内/室外，三任务多指标，定性结果（如船体文字清晰可辨）具说服力。

## 8. 不足与局限

- **骨干依赖性强**：静态偏置继承自 CUT3R 骨干，其可靠性可能依赖模型训练时是否见过动态场景；未验证在其他 RayMap 类架构（如离线模型）上的可迁移性。
- **动态图精度有限**：平均 IoU 仅约 0.203，且 Sintel 上 AUC 低于 0.5，作者承认其定位是"软门控线索"而非精确分割。
- **部分指标非最优**：Sintel 相对深度低于 StreamVGGT；度量尺度下 Sintel 绝对误差高于 Point3R；旋转 RPE、法向一致性（NC）未全面领先（Spann3R 的 NC 更高）。
- **性能代价**：双分支带来约 30% 吞吐下降与更高显存，与"实时恒定内存"目标存在权衡。
- **前提假设**：重置度量对齐依赖存在可用的重复帧；平滑系数 λ、静态权重 γ 等超参的敏感性未在正文展开分析。
- **算力信息缺失**：作为免训练方法虽可理解，但未报告骨干训练成本与评测硬件以外的资源情况。
- **应用限制**：方法定位于带循环记忆且原生支持 RayMap-only 查询的流式模型，适用范围相对狭窄。

（完）
