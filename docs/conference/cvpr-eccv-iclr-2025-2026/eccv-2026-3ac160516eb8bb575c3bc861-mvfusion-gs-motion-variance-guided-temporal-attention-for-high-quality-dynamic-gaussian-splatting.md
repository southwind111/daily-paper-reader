---
title: "MVFusion-GS: Motion-Variance Guided Temporal Attention for High-Quality Dynamic Gaussian Splatting"
title_zh: MVFusion-GS：运动方差引导的时间注意力高质量动态高斯泼溅
authors: "Jianwei Hu, Tingxuan Huang, Hengyu Zhou, Ningna Wang, Xiaohu Guo, Jinshan Lai, Bin Wang"
date: 2026
publication_date: 2026
publication_date_precision: year
publication_date_source: conference year only; exact release date unverified
publication_date_kind: unknown
pdf: "https://media.eventhosts.cc/Conferences/ECCV2026/pdfs/10106.pdf"
tags: ["query:dr"]
score: 9.0
evidence: 结合时间注意力的运动感知动态高斯泼溅
tldr: 将3D高斯泼溅扩展到动态场景的形变网络普遍缺乏显式运动感知，既未捕捉长期运动强度也未利用短期时间一致性，导致前景形变不准与背景伪静态残差。本文提出MVFusion-GS，引入运动方差引导精修与时间注意力两种运动感知机制增强形变网络。实验表明其显著改善动态场景重建质量并抑制背景残差。
source: ECCV-2026-Accepted-Program
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-3ac160516eb8bb575c3bc861/fig-001.webp\", \"caption\": \"\", \"page\": 1, \"index\": 1, \"width\": 1053, \"height\": 493}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-3ac160516eb8bb575c3bc861/fig-002.webp\", \"caption\": \"\", \"page\": 1, \"index\": 2, \"width\": 505, \"height\": 377}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-3ac160516eb8bb575c3bc861/fig-003.webp\", \"caption\": \"\", \"page\": 1, \"index\": 3, \"width\": 536, \"height\": 816}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-3ac160516eb8bb575c3bc861/fig-004.webp\", \"caption\": \"\", \"page\": 1, \"index\": 4, \"width\": 997, \"height\": 432}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-3ac160516eb8bb575c3bc861/fig-005.webp\", \"caption\": \"\", \"page\": 1, \"index\": 5, \"width\": 997, \"height\": 562}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-3ac160516eb8bb575c3bc861/fig-006.webp\", \"caption\": \"\", \"page\": 1, \"index\": 6, \"width\": 500, \"height\": 377}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-3ac160516eb8bb575c3bc861/fig-007.webp\", \"caption\": \"\", \"page\": 1, \"index\": 7, \"width\": 503, \"height\": 377}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-3ac160516eb8bb575c3bc861/fig-008.webp\", \"caption\": \"\", \"page\": 1, \"index\": 8, \"width\": 535, \"height\": 816}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-3ac160516eb8bb575c3bc861/fig-009.webp\", \"caption\": \"\", \"page\": 1, \"index\": 9, \"width\": 503, \"height\": 377}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-3ac160516eb8bb575c3bc861/fig-010.webp\", \"caption\": \"\", \"page\": 1, \"index\": 10, \"width\": 502, \"height\": 377}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-3ac160516eb8bb575c3bc861/fig-011.webp\", \"caption\": \"\", \"page\": 1, \"index\": 11, \"width\": 1352, \"height\": 1014}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-3ac160516eb8bb575c3bc861/fig-012.webp\", \"caption\": \"\", \"page\": 1, \"index\": 12, \"width\": 1352, \"height\": 1014}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-3ac160516eb8bb575c3bc861/fig-013.webp\", \"caption\": \"\", \"page\": 8, \"index\": 13, \"width\": 1352, \"height\": 1014}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-3ac160516eb8bb575c3bc861/fig-014.webp\", \"caption\": \"\", \"page\": 8, \"index\": 14, \"width\": 1352, \"height\": 1014}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-3ac160516eb8bb575c3bc861/fig-015.webp\", \"caption\": \"\", \"page\": 8, \"index\": 15, \"width\": 1352, \"height\": 1014}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-3ac160516eb8bb575c3bc861/fig-016.webp\", \"caption\": \"\", \"page\": 8, \"index\": 16, \"width\": 1352, \"height\": 1014}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-3ac160516eb8bb575c3bc861/fig-017.webp\", \"caption\": \"\", \"page\": 12, \"index\": 17, \"width\": 1513, \"height\": 377}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-3ac160516eb8bb575c3bc861/fig-018.webp\", \"caption\": \"\", \"page\": 12, \"index\": 18, \"width\": 1513, \"height\": 377}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-3ac160516eb8bb575c3bc861/fig-019.webp\", \"caption\": \"\", \"page\": 12, \"index\": 19, \"width\": 1513, \"height\": 377}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-3ac160516eb8bb575c3bc861/fig-020.webp\", \"caption\": \"\", \"page\": 13, \"index\": 20, \"width\": 479, \"height\": 269}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-3ac160516eb8bb575c3bc861/fig-021.webp\", \"caption\": \"\", \"page\": 13, \"index\": 21, \"width\": 2523, \"height\": 377}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-3ac160516eb8bb575c3bc861/fig-022.webp\", \"caption\": \"\", \"page\": 13, \"index\": 22, \"width\": 2523, \"height\": 377}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-3ac160516eb8bb575c3bc861/fig-023.webp\", \"caption\": \"\", \"page\": 13, \"index\": 23, \"width\": 2523, \"height\": 377}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-3ac160516eb8bb575c3bc861/fig-024.webp\", \"caption\": \"\", \"page\": 13, \"index\": 24, \"width\": 2523, \"height\": 377}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-3ac160516eb8bb575c3bc861/fig-025.webp\", \"caption\": \"\", \"page\": 13, \"index\": 25, \"width\": 479, \"height\": 269}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-3ac160516eb8bb575c3bc861/fig-026.webp\", \"caption\": \"\", \"page\": 13, \"index\": 26, \"width\": 479, \"height\": 269}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-3ac160516eb8bb575c3bc861/fig-027.webp\", \"caption\": \"\", \"page\": 13, \"index\": 27, \"width\": 479, \"height\": 269}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-3ac160516eb8bb575c3bc861/fig-028.webp\", \"caption\": \"\", \"page\": 13, \"index\": 28, \"width\": 479, \"height\": 269}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-3ac160516eb8bb575c3bc861/fig-029.webp\", \"caption\": \"\", \"page\": 13, \"index\": 29, \"width\": 2523, \"height\": 377}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-3ac160516eb8bb575c3bc861/fig-030.webp\", \"caption\": \"\", \"page\": 13, \"index\": 30, \"width\": 503, \"height\": 377}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-3ac160516eb8bb575c3bc861/fig-031.webp\", \"caption\": \"\", \"page\": 13, \"index\": 31, \"width\": 503, \"height\": 377}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-3ac160516eb8bb575c3bc861/fig-032.webp\", \"caption\": \"\", \"page\": 13, \"index\": 32, \"width\": 431, \"height\": 431}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-3ac160516eb8bb575c3bc861/fig-033.webp\", \"caption\": \"\", \"page\": 13, \"index\": 33, \"width\": 431, \"height\": 431}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-3ac160516eb8bb575c3bc861/fig-034.webp\", \"caption\": \"\", \"page\": 13, \"index\": 34, \"width\": 431, \"height\": 431}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-3ac160516eb8bb575c3bc861/fig-035.webp\", \"caption\": \"\", \"page\": 13, \"index\": 35, \"width\": 503, \"height\": 377}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-3ac160516eb8bb575c3bc861/fig-036.webp\", \"caption\": \"\", \"page\": 15, \"index\": 36, \"width\": 1352, \"height\": 1014}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-3ac160516eb8bb575c3bc861/fig-037.webp\", \"caption\": \"\", \"page\": 15, \"index\": 37, \"width\": 1352, \"height\": 1014}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-3ac160516eb8bb575c3bc861/fig-038.webp\", \"caption\": \"\", \"page\": 15, \"index\": 38, \"width\": 1352, \"height\": 1014}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-3ac160516eb8bb575c3bc861/fig-039.webp\", \"caption\": \"\", \"page\": 15, \"index\": 39, \"width\": 1352, \"height\": 1014}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-3ac160516eb8bb575c3bc861/fig-040.webp\", \"caption\": \"\", \"page\": 15, \"index\": 40, \"width\": 1352, \"height\": 1014}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-3ac160516eb8bb575c3bc861/fig-041.webp\", \"caption\": \"\", \"page\": 15, \"index\": 41, \"width\": 1352, \"height\": 1014}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-3ac160516eb8bb575c3bc861/fig-042.webp\", \"caption\": \"\", \"page\": 15, \"index\": 42, \"width\": 1352, \"height\": 1014}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-3ac160516eb8bb575c3bc861/fig-043.webp\", \"caption\": \"\", \"page\": 15, \"index\": 43, \"width\": 1352, \"height\": 1014}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-3ac160516eb8bb575c3bc861/fig-044.webp\", \"caption\": \"\", \"page\": 15, \"index\": 44, \"width\": 1352, \"height\": 1014}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-3ac160516eb8bb575c3bc861/fig-045.webp\", \"caption\": \"\", \"page\": 15, \"index\": 45, \"width\": 1352, \"height\": 1014}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-3ac160516eb8bb575c3bc861/fig-046.webp\", \"caption\": \"\", \"page\": 15, \"index\": 46, \"width\": 1352, \"height\": 1014}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-3ac160516eb8bb575c3bc861/fig-047.webp\", \"caption\": \"\", \"page\": 15, \"index\": 47, \"width\": 1352, \"height\": 1014}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-3ac160516eb8bb575c3bc861/fig-048.webp\", \"caption\": \"\", \"page\": 15, \"index\": 48, \"width\": 1352, \"height\": 1014}]"
motivation: 现有形变网络缺乏显式运动感知，难以捕捉长期运动强度与短期时间一致性。
method: 提出运动方差引导精修与时间注意力两种运动感知机制增强形变网络。
result: 改善前景形变精度并抑制背景伪静态残差。
conclusion: 提升了动态高斯泼溅的重建质量。
---

## Abstract
3D Gaussian Splatting (3DGS) enables real-time novel viewsynthesis for static scenes. Extending it to dynamic scenes via deforma-tion fields has recently attracted significant attention, particularly fordynamic scene reconstruction and distractor-free reconstruction. How-ever, existing deformation networks lack explicit motion awareness: theyneither capture long-term motion intensity nor exploit short-term tempo-ral coherence, leading to inaccurate foreground deformation and pseudo-static residuals in the background. We present MVFusion-GS, a methodthat enhances deformation networks with two complementary motion-aware mechanisms. The Motion-Variance Guided Refinement ag-gregates per-Gaussian deformation statistics across time to estimate mo-tion variance and uses it to guide dynamic-static separation during defor-mation prediction. The MotionFormer Temporal Attention moduleapplies Transformer self-attention over neighboring timesteps to modellocal motion dependencies and improve temporal consistency. Extensiveexperiments on both dynamic scene reconstruction and distractor-free re-construction benchmarks demonstrate state-of-the-art performance, show-ing that explicit motion awareness improves both foreground motionmodeling and static background reconstruction.

---

## 论文详细总结（自动生成）

# MVFusion-GS 论文中文总结

## 1. 核心问题与整体含义（研究动机与背景）

- **背景**：3D Gaussian Splatting（3DGS）已实现静态场景的实时新视角合成。通过形变场（deformation field）将其扩展到动态场景，是当前热点，代表性任务有两类：
  - **动态场景重建**：高保真重建前景运动；
  - **无干扰物重建（distractor-free reconstruction）**：从随手拍摄的图像中分离行人、车辆等瞬态干扰物，恢复干净的静态背景。
- **核心问题**：现有形变网络缺乏**显式运动感知**——既不捕捉长期运动强度，也不利用短期时间一致性。结果是：
  - 前景形变预测不准；
  - 低幅或瞬态运动被欠建模，产生“伪静态”（pseudo-static）残差泄漏到静态背景分支，污染背景重建。
- **整体含义**：作者以 DeGauss 的解耦动态–静态高斯框架为基线，指出其形变网络仅通过时空网格编码局部 (x, t) 特征，没有显式刻画每个高斯所经历的运动模式及其跨帧时间上下文。MVFusion-GS 通过两个互补的运动感知机制增强形变网络，试图在**同一框架内同时改善动态前景重建与静态背景纯净度**，即“双任务插件”。

## 2. 方法论

### 2.1 核心思想
- 把基线形变网络视为**粗预测器**，在其特征空间上增加轻量级运动感知精修，精修后的形变为：
  - ΔG_d(t) = ΔG_d^base(t) + ΔG_d^MR(t)
  - 其中 ΔG_d^MR(t) = Φ( h_base(t) + h_MVG(t) + h_MFTA(t) )
- 两个模块**只作用于特征空间**，与原形变头 Φ 融合后由**未修改的形变头**解码，因此可作为插件无缝接入已有形变式高斯流水线。
- 二者互补：MVG 提供**长期全局轨迹先验**用于粗粒度动静分离；MFTA 用**短期时间上下文**精修瞬时形变，提升时间一致性。

### 2.2 Motion-Variance Guided Refinement（MVG）
- **动机**：标准时空网格只编码局部 (x, t)，无全局运动行为线索，导致低幅/瞬态运动欠拟合，产生伪静态残差。
- **轨迹采样**：每 E 次训练迭代，从训练相机采样 K 个时间戳 {t_k}，对全部 N 个动态高斯评估形变网络，得到位置位移 Δpos、旋转幅度 θ=‖Δr‖₂、对数尺度变化 Δℓ = log(s+Δs) − log(s)。
- **全局轨迹签名（13D）**：对采样轨迹统计时序均值与方差，构成
  - 位置（6d：均值 + 方差）
  - 旋转幅度（2d：均值 + 方差）
  - 各向同性尺度（2d）
  - 各向异性尺度（2d）
  - 运动强度（1d）
- **运动强度分数**：s_intensity = 0.7·σ_pos + 0.2·σ_scale + 0.1·σ_rot，权重为经验设定。位置方差反映大位移，尺度方差反映深度相关尺寸变化，旋转方差反映局部关节式运动；融合后前景/背景对比更清晰。
- **局部方差字典**：定义局部运动方差 e_i(t_k) = σ({Δpos_i,j}, j∈[k−w, k+w])，仅在稀疏采样时间戳上存储，任意时刻通过线性插值查询。例如 300 帧序列每高斯只存 10 个值，约 30× 压缩。
- **注入方式**：将全局签名 v_i 与查询到的局部强度 e_i(t) 通过轻量 MLP 映射到形变特征维度，得到 h_MVG，与基线特征融合。所有运动描述子**不参与梯度传播**，计算后缓存复用。

### 2.3 MotionFormer Temporal Attention（MFTA）
- **动机**：MVG 只给轨迹级统计，缺少当前帧附近的短期时间交互，而局部上下文对消解运动歧义很关键。
- **时间 token 构造**：对时间 t_i 构造邻域 T(t_i) = {t_{i−w}, t_i, t_{i+w}}，每个时刻的 token 为
  - z_{i,t} = [ h_{i,t}, Φ(h_{i,t}), e_i(t) ]
  - 即形变特征、预测形变量与瞬时运动强度的拼接。
- **注意力**：以当前 token 为 Query，对时间邻居做**交叉注意力**（query-centered cross-attention），输出经轻量 MLP 得到 h_MFTA，再与基线特征融合。

### 2.4 训练策略与损失
- **三阶段训练**：
  1. **基础几何**：仅优化高斯几何，禁用形变网络，激进致密化与不透明度重置；
  2. **基础形变**：几何稳定后启用基线形变网络学习时空变换，阶段末启用时间分支开始收集运动统计；
  3. **运动感知精修**：激活零初始化的 MVG 与 MFTA 分支，与基线特征融合端到端训练。
- **损失**：L = λ₁L_rgb + λ₂L_ssim + λ₃L_reg（L1 光度损失、结构相似性损失、高斯正则项如尺度与长宽比约束）。
- **推理**：直接复用缓存的 MVG 描述子，时间模块可选择性关闭以提升效率。
- **实现细节**：基于 DeGauss 框架（PyTorch），训练 30k 迭代，Adam 优化器；运动统计每 2000 迭代更新一次，采样 K=64 个时间戳；时间窗口 w=5。

## 3. 实验设计

- **数据集 / Benchmark**：
  - **NeRF On-the-Go**：真实随手拍摄场景，含行人、自行车、车辆等瞬态干扰物；每场景约 100 张图像，使用 7 个场景，在遮挡图像上训练、在少量干净留出视角上评估（无干扰物重建）。
  - **RobustNeRF**：静态场景中人工放置干扰物，跨拍摄被移动或移除，制造跨视角不一致（无干扰物重建）。
  - **Neu3D**：约 20 台同步静态相机拍摄约 300 帧的多视角动态视频；按标准协议视角 0 测试、其余训练（动态场景重建）。
- **评价指标**：PSNR、SSIM、LPIPS。
- **对比方法**：
  - NeRF On-the-Go / RobustNeRF：RobustNeRF、NeRF On-the-go、3DGS、WildGaussians、DeSplat、SpotlessSplats、DeGauss；
  - Neu3D：NeRFPlayer、HexPlane、K-Planes、MixVoxels、SWinGS、4DGS、MangoGS、DeGauss；
  - 另设 **MVFusion-GS (4DGS plug-in)** 变体，验证 MVG/MFTA 作为单分支 4DGS 插件的通用性。

## 4. 资源与算力

- 文中明确说明：训练使用**单张 NVIDIA RTX 3090 GPU**，30k 迭代，Adam 优化器。
- **未明确说明**：GPU 数量仅为 1 张（表述为单卡），但未给出具体训练时长、显存占用、推理速度（FPS）或总 GPU 小时数；也未报告缓存运动统计带来的额外存储/计算开销的定量数据。
- 其余设置沿用 DeGauss 默认配置；敏感性分析（运动分数融合权重、统计更新间隔、时间窗口大小、时间一致性）放在补充材料，正文未展开。

## 5. 实验数量与充分性

- **主要定量实验**（3 组主表）：
  - 表 1：NeRF On-the-Go 无干扰物重建，6 个场景 × 3 指标，7 个对比方法；
  - 表 2：NeRF On-the-Go 前景动态区域重建（与 DeGauss 逐场景对比）；
  - 表 3：RobustNeRF，4 个场景 × 3 指标，4 个对比方法；
  - 表 4：Neu3D，7 个场景 × 3 指标，8 个对比方法，并含插件变体。
- **消融实验**（表 5）：约 7 个变体，覆盖无 MVG/MFTA、无 MVG、仅位置方差、无 MFTA、自注意力替代交叉注意力、完整模型；在 Neu3D 与 NeRF On-the-Go 上均报告。
- **定性实验**：图 6/7（NeRF On-the-Go 背景与全合成对比）、图 8（RobustNeRF）、图 9（Neu3D），以及图 4 的运动方差热图可视化。
- **充分性评估**：
  - 优点：覆盖两个任务、三个数据集、多类 SOTA 基线，并额外验证插件泛化性；消融维度较有针对性。
  - 局限：消融主要在 Neu3D 上展开，NeRF On-the-Go 上作者自述 PSNR 差异较小，仅凭感知指标推断趋势；补充材料的敏感性分析未在正文呈现，无法从正文判断超参稳健性。
  - 公平性：所有方法在同一基准协议下比较，但未详细说明各基线是否使用官方推荐超参、是否统一训练迭代数/分辨率；表 2 仅与 DeGauss 对比，未扩展到其他基线的前景区域评测。

## 6. 主要结论与发现

- **无干扰物重建**：在 NeRF On-the-Go 上三项平均指标均排名第一，且在全部 6 个场景取得最低 LPIPS；即使个别场景 PSNR 略低于 DeGauss，LPIPS 仍明显更优，说明背景更干净、伪影更少。RobustNeRF 上平均 PSNR 29.39、LPIPS 0.069，优于 DeGauss（28.89 / 0.085）。
- **动态场景重建**：Neu3D 上取得最佳平均 PSNR 与 LPIPS；动态区域 PSNR 达 31.78，优于 SpaceTimeGS（30.85）与 ST-4DGS（31.35）。作为 4DGS 插件使用时同样优于单分支基线，验证插件式设计的通用性。
- **前景改善显著**：表 2 显示前景动态区域平均 PSNR 从 DeGauss 的 22.93 提升到 27.60，说明运动感知精修不仅稳定背景，也显著提升动态物体重建。
- **消融结论**：运动统计有效（31.52→31.64），完整 13D 轨迹签名优于仅位置方差（31.93）；时间上下文聚合有效（去掉 MFTA 降至 31.78）；交叉注意力优于普通自注意力（32.01），完整模型最佳（32.07）。
- **核心发现**：显式运动感知能同时改善前景运动建模与静态背景重建，且“全局轨迹先验 + 短期时间注意力”具有互补增益。

## 7. 优点

- **插件式设计**：MVG/MFTA 只在特征空间操作，不修改原形变头，可无缝嵌入 4DGS、DeGauss 等不同流水线，工程迁移性好。
- **双任务统一**：同一框架同时服务动态场景重建与无干扰物重建，并在一套机制下解释“伪静态残差”问题，动机与解法对应清晰。
- **运动描述子设计紧凑**：13D 全局签名融合位置/旋转/各向同性/各向异性尺度统计，并用加权强度分数增强前景–背景可分性；图 4 的可视化直观支撑其判别能力。
- **效率考量**：运动统计不参与反向传播、缓存复用；局部方差字典稀疏存储 + 线性插值，300 帧仅存 10 个样本（约 30× 压缩）；推理时时间模块可关闭。
- **实验覆盖面较好**：三个数据集、两个任务、多类 2023–2025 年 SOTA 对比，并给出插件变体与逐场景结果，定性图对伪静态残差的展示有说服力。
- **消融设计有针对性**：分别验证 MVG 必要性、轨迹签名完整性与 MFTA/注意力形式的贡献。

## 8. 不足与局限

- **对基线形变场的依赖**：作者自述方法仍依赖基线形变场提供可靠运动线索；当初始形变对复杂前景运动欠拟合时，估计的方差判别性会下降。
- **极端场景失效风险**：在严重遮挡或运动证据极弱的情况下，仍可能残留伪影，需未来研究更鲁棒的运动感知高斯重分配。
- **超参与权重经验性**：运动强度分数权重（0.7/0.2/0.1）为经验选取，正文未给出敏感性分析（放在补充材料），泛化性证据不足。
- **算力与效率报告不完整**：仅说明单张 RTX 3090、30k 迭代，缺少训练时长、显存、推理 FPS 与缓存开销的定量对比，难以评估实际部署成本。
- **评测覆盖有限**：无干扰物重建主要基于两个数据集，场景规模较小（NeRF On-the-Go 7 个场景）；前景区域对比仅与 DeGauss 进行，未与其他 SOTA 扩展比较。
- **消融结论的统计强度**：NeRF On-the-Go 上各变体 PSNR 差距很小，主要依赖 LPIPS 推断趋势，缺乏显著性检验；动态与静态分支的掩码学习机制本身未做独立消融。
- **潜在偏差**：轨迹统计从训练相机采样，若训练视角分布偏斜或运动观测不充分，可能影响运动强度估计；跨数据集（单目 vs 多视角）适用性未系统验证。

（完）
