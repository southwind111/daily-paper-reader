---
title: Real-Time Dynamic Scene Rendering with Controlled Compressibility and Contact Awareness
title_zh: 可控压缩性与接触感知的实时动态场景渲染
authors: "Shi, Boya, Guan, Naiyang, Yi, Xiaodong"
date: 2026
publication_date: 2026
publication_date_precision: year
publication_date_source: conference year only; exact release date unverified
publication_date_kind: unknown
pdf: "https://openaccess.thecvf.com/content/CVPR2026/papers/Shi_Real-Time_Dynamic_Scene_Rendering_with_Controlled_Compressibility_and_Contact_Awareness_CVPR_2026_paper.pdf"
tags: ["query:dr"]
score: 8.0
evidence: 实时动态场景渲染，基于高斯基元与速度先验
tldr: 现有动态场景渲染方法常假设刚体或方向受限的运动，导致遮挡与接触边界处出现伪影。本文提出一种统一的、源感知的动态渲染框架，通过流形约束保证高斯基元一致性，并利用Helmholtz参数化、各向异性可压缩方向先验和仿射族投影预测速度。实验表明该方法在多个基准上有效减少伪影并提升渲染质量，为实时动态场景渲染提供了物理一致的表示方案。
source: CVPR-2026-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-shi-real-time-dynamic-scene-rendering-with-controlled-compressibility-and-contact-awareness-cvpr-2026-paper/fig-001.webp\", \"caption\": \"\", \"page\": 7, \"index\": 1, \"width\": 960, \"height\": 720}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-shi-real-time-dynamic-scene-rendering-with-controlled-compressibility-and-contact-awareness-cvpr-2026-paper/fig-002.webp\", \"caption\": \"\", \"page\": 7, \"index\": 2, \"width\": 960, \"height\": 720}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-shi-real-time-dynamic-scene-rendering-with-controlled-compressibility-and-contact-awareness-cvpr-2026-paper/fig-003.webp\", \"caption\": \"\", \"page\": 7, \"index\": 3, \"width\": 960, \"height\": 720}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-shi-real-time-dynamic-scene-rendering-with-controlled-compressibility-and-contact-awareness-cvpr-2026-paper/fig-004.webp\", \"caption\": \"\", \"page\": 7, \"index\": 4, \"width\": 960, \"height\": 720}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-shi-real-time-dynamic-scene-rendering-with-controlled-compressibility-and-contact-awareness-cvpr-2026-paper/fig-005.webp\", \"caption\": \"\", \"page\": 7, \"index\": 5, \"width\": 960, \"height\": 720}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-shi-real-time-dynamic-scene-rendering-with-controlled-compressibility-and-contact-awareness-cvpr-2026-paper/fig-006.webp\", \"caption\": \"\", \"page\": 7, \"index\": 6, \"width\": 960, \"height\": 720}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-shi-real-time-dynamic-scene-rendering-with-controlled-compressibility-and-contact-awareness-cvpr-2026-paper/fig-007.webp\", \"caption\": \"\", \"page\": 7, \"index\": 7, \"width\": 960, \"height\": 720}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-shi-real-time-dynamic-scene-rendering-with-controlled-compressibility-and-contact-awareness-cvpr-2026-paper/fig-008.webp\", \"caption\": \"\", \"page\": 7, \"index\": 8, \"width\": 960, \"height\": 720}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-shi-real-time-dynamic-scene-rendering-with-controlled-compressibility-and-contact-awareness-cvpr-2026-paper/fig-009.webp\", \"caption\": \"\", \"page\": 7, \"index\": 9, \"width\": 960, \"height\": 720}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-shi-real-time-dynamic-scene-rendering-with-controlled-compressibility-and-contact-awareness-cvpr-2026-paper/fig-010.webp\", \"caption\": \"\", \"page\": 7, \"index\": 10, \"width\": 960, \"height\": 720}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-shi-real-time-dynamic-scene-rendering-with-controlled-compressibility-and-contact-awareness-cvpr-2026-paper/fig-011.webp\", \"caption\": \"\", \"page\": 7, \"index\": 11, \"width\": 960, \"height\": 720}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-shi-real-time-dynamic-scene-rendering-with-controlled-compressibility-and-contact-awareness-cvpr-2026-paper/fig-012.webp\", \"caption\": \"\", \"page\": 7, \"index\": 12, \"width\": 960, \"height\": 720}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-shi-real-time-dynamic-scene-rendering-with-controlled-compressibility-and-contact-awareness-cvpr-2026-paper/fig-013.webp\", \"caption\": \"\", \"page\": 7, \"index\": 13, \"width\": 960, \"height\": 720}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-shi-real-time-dynamic-scene-rendering-with-controlled-compressibility-and-contact-awareness-cvpr-2026-paper/fig-014.webp\", \"caption\": \"\", \"page\": 7, \"index\": 14, \"width\": 960, \"height\": 720}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-shi-real-time-dynamic-scene-rendering-with-controlled-compressibility-and-contact-awareness-cvpr-2026-paper/fig-015.webp\", \"caption\": \"\", \"page\": 7, \"index\": 15, \"width\": 960, \"height\": 720}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-shi-real-time-dynamic-scene-rendering-with-controlled-compressibility-and-contact-awareness-cvpr-2026-paper/fig-016.webp\", \"caption\": \"\", \"page\": 7, \"index\": 16, \"width\": 960, \"height\": 720}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-shi-real-time-dynamic-scene-rendering-with-controlled-compressibility-and-contact-awareness-cvpr-2026-paper/fig-017.webp\", \"caption\": \"\", \"page\": 7, \"index\": 17, \"width\": 960, \"height\": 720}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-shi-real-time-dynamic-scene-rendering-with-controlled-compressibility-and-contact-awareness-cvpr-2026-paper/fig-018.webp\", \"caption\": \"\", \"page\": 7, \"index\": 18, \"width\": 960, \"height\": 720}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-shi-real-time-dynamic-scene-rendering-with-controlled-compressibility-and-contact-awareness-cvpr-2026-paper/fig-019.webp\", \"caption\": \"\", \"page\": 7, \"index\": 19, \"width\": 960, \"height\": 720}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-shi-real-time-dynamic-scene-rendering-with-controlled-compressibility-and-contact-awareness-cvpr-2026-paper/fig-020.webp\", \"caption\": \"\", \"page\": 7, \"index\": 20, \"width\": 960, \"height\": 720}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-shi-real-time-dynamic-scene-rendering-with-controlled-compressibility-and-contact-awareness-cvpr-2026-paper/fig-021.webp\", \"caption\": \"\", \"page\": 8, \"index\": 21, \"width\": 690, \"height\": 518}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-shi-real-time-dynamic-scene-rendering-with-controlled-compressibility-and-contact-awareness-cvpr-2026-paper/fig-022.webp\", \"caption\": \"\", \"page\": 8, \"index\": 22, \"width\": 690, \"height\": 518}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-shi-real-time-dynamic-scene-rendering-with-controlled-compressibility-and-contact-awareness-cvpr-2026-paper/fig-023.webp\", \"caption\": \"\", \"page\": 8, \"index\": 23, \"width\": 690, \"height\": 518}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-shi-real-time-dynamic-scene-rendering-with-controlled-compressibility-and-contact-awareness-cvpr-2026-paper/fig-024.webp\", \"caption\": \"\", \"page\": 8, \"index\": 24, \"width\": 691, \"height\": 518}]"
motivation: 现有动态渲染方法依赖刚体或方向受限假设，在真实运动与接触场景下于遮挡边界产生伪影。
method: 提出源感知框架，用流形约束保证高斯基元一致，并通过Helmholtz参数化、可压缩方向先验与仿射族投影预测速度。
result: 在多项基准实验上有效抑制遮挡与接触边界的渲染伪影，提升动态场景渲染质量。
conclusion: 为实时动态场景渲染提供了物理一致的表示与约束方案，拓展了动态渲染的适用范围。
---

## Abstract
Existing dynamic scene rendering methods often adopt rigid-body or direction-limited assumptions, yet real-world motion and contact routinely violate these, producing artifacts near occlusion boundaries. To address this, we introduce a unified, source-aware framework for dynamic rendering that enforces the consistency of Gaussian primitives under explicit manifold constraints. We project predicted velocities onto physically grounded priors via efficient, parallel inner solves: (i) a Helmholtz parameterization that separates divergence-free and potential-flow motion components; (ii) an anisotropic, compressible directional prior; and (iii) an affine family that disentangles rotation from isotropic scaling. Experiments on extensive benchmarks show consistent improvements over state-of-the-art methods in reconstruction fidelity and temporal coherence. Our approach ensures physically realistic rendering, especially near contacts, and substantially reduces motion-boundary artifacts.

---

## 论文详细总结（自动生成）

# 论文总结：可控压缩性与接触感知的实时动态场景渲染

## 1. 核心问题与研究动机

- **背景**：从时变多视角图像进行动态场景重建与视角合成，是计算机图形学的核心问题，广泛应用于 AR/VR 远程临场、视觉特效、机器人/数字孪生等对精度、物理合理性和周转时间要求极高的场景。
- **现有方法的两大缺陷**：
  - **物理假设过强**：主流方法（NeRF、3DGS 及其动态变体）通常假设**无源、体积守恒（不可压缩）**的运动，无法刻画真实世界中普遍存在的压缩/膨胀、曝光漂移、生长/衰减等非体积保持效应。
  - **忽视接触与摩擦**：遮挡边界处的接触、非穿透和切向滑移常被忽略，或仅用软惩罚近似，导致**边界伪影**。
- **技术挑战的交织性**：
  - 可压缩流与源项在图像证据下**弱可辨识**，需要精心设计的先验与时间正则化。
  - 接触集随时间**离散变化**，使目标函数非光滑，并引发运动先验间的组合爆炸。
  - 移动边界需满足**质量守恒**以防止虚假通量。
  - 低纹理区域、重复视角、谱重叠基导致法方程**病态**，需要归一化、阻尼与结构保持预条件。
  - 图像域导数**放大噪声**，单目噪声序列下提取符号距离等值面、法向与表面法向速度困难。
- **整体含义**：论文旨在构建一个**源感知、可压缩、接触感知**的统一动态渲染框架，在保持闭式/线性内层求解与实时性能的前提下，将物理约束融入可微渲染管线。

## 2. 方法论

### 2.1 核心思想

- 采用**投影式交替优化**：每步先求解一个凸最小二乘投影，将网络预测速度投影到物理先验（可压缩性、源项、流形/接触约束）上，得到代理场；再以 stop-gradient 方式用投影损失与连续性一致性损失更新网络参数。
- 三大互补参数化：**(i) Helmholtz 分解**（分离无散度与势流分量）；**(ii) 各向异性可压缩方向先验**；**(iii) 仿射族**（解耦旋转与各向同性缩放）。

### 2.2 源感知可压缩流

- **带源连续性方程**：∂tψ + u·∇ψ + ψ∇·u = q，其中 q>0 表示生成，q<0 表示消失。该式统一了可压缩平流与光度变化，使密度变化可归因于 ∇·u（体积压缩）或 q（真实耗散）。
- **2D/3D 目标**：在图像平面采样点上最小化源感知连续性残差（式 2）；在 3D 中用 Dirac δ 表示高斯基元的传输信号，拟合几何匹配能量（式 4），并采用前向差分残差（式 5）构造最小二乘问题，附带质量非负约束与时间平滑正则。
- **源建模**：引入比例衰减先验 q = λt ψ，产生由单个时变标量 λt 控制的指数演化。
- **可压缩参数化**：
  - 将体积变化限制在**指定子空间** E = span(V)，用正交投影 P = VVᵀ 分解速度为 u = uτ + P∇Φ，其中 uτ 无散度，∇·u 由势函数 Φ 沿 E 的拉普拉斯迹承担（式 6）。
  - **仿射族**：u(x,t) = Ω(t)x + E₀(t)x + κ(t)x + b(t)，其中 Ω 反对称（旋转）、E₀ 对称无迹（保体积剪切）、κ 为各向同性缩放（∇·u = dκ）、b 为平移；对 κ 施加 λκκ² 正则。
  - **Helmholtz 参数化**：用无散度基 b_k 与势流基 ∇φ_ℓ 展开速度（式 9），源汇场用 r_p 展开，最终形成线性最小二乘问题（式 11、12），含 λcomp‖α‖² 可压缩性惩罚。

### 2.3 物理引导训练目标

- **投影间隙损失 Lproj**（式 13）：约束网络速度 vθ 逼近投影场 ṽ；对 ṽ 停止梯度，依 Danskin 原理仅 vθ 获梯度（式 14）。
- **连续性一致性损失 LCE**（式 15）：惩罚源增强传输律的逐像素违背。
- **几何损失 Lgeo**（式 16）：对齐投影运动与高斯基元轨迹、质量平衡。

### 2.4 隐式曲面上的流形与接触约束

- **隐式曲面表示**：φ_k(x,t)=0，单位法向 n_k = ∇φ_k/‖∇φ_k‖，切向投影 P_T,k = I − n_k n_kᵀ，表面法向速度 b_k = −∂tφ_k/‖∇φ_k‖，接触集 A(x,t) = {k : |φ_k(x,t)| ≤ ε}。
- **逐点约束求解**：目标为 u* = argmin‖u − v_target‖² s.t. u ∈ ∩ C_k。
  - **粘着约束**：等式 n_kᵀu = b_k，正交投影有闭式解 u* = v − Aᵀ(AAᵀ)⁻¹(Av − b)（式 19、25）。
  - **非穿透**：单边不等式 nᵀu ≥ b，投影为式 26。
  - **库仑摩擦锥**：相对试探速度分解为法向 v̄n 与切向 v̄t，先投影法向 v̂n = max(v̄n,0)，再投影到锥体（式 20），得到 u* = u_surf,k + v̂n n_k + ṽ_t（式 21）；单锥的欧氏投影有闭式解（式 28）。
- **多点接触**：逐点求解小规模 SOCP，或用凸集投影（POCS）的短序列近似；也可在邻域 N 内拟合**局部仿射场** u(x)=Ax+b（式 22、30），保持凸性与并行性。
- **物理一致软惩罚**：L_nopen（式 33）与 L_fric（式 34）将接触条件编码为软约束，与投影损失共同构成外层优化目标。

## 3. 实验设计

- **数据集 / 基准**：
  - **Plenoptic Video Dataset**：6 个真实场景，每场景 15–20 个固定相机，训练用 17–20 视角、留 1 个测试，分辨率 1352×1014；由首帧构建 SfM 点云并下采样至 <10⁵ 点。
  - **D-NeRF Dataset**：8 个单目视频序列，每序列 50–200 帧训练、10–20 验证、20 测试，分辨率统一为 800×800。
- **对比方法**：
  - Plenoptic 上对比 DyNeRF、StreamRF、HyperReel、NeRFPlayer、K-Planes、MixVoxels、MSTH、STG、RealTime4DGS、Deformable4DGS。
  - D-NeRF 上对比 D-NeRF、TiNeuVox、K-Planes、FFDNeRF、MSTH、V4D、Deformable3DGS、Deformable4DGS。
- **评价指标**：PSNR↑、SSIM↑、LPIPS↓、训练时间、FPS。
- **消融研究**：在 D-NeRF 上进行 6 组配置（a–f），分别验证可压缩流、接触约束、GP（高斯基元级投影）与 LL（局部线性场投影）的贡献。

## 4. 资源与算力

- **GPU**：全部实验在**单张 NVIDIA RTX 3090** 上完成，基于 PyTorch 实现。
- **训练时长**：
  - Plenoptic：约 **14,000 步优化**，训练约 **35 分钟**。
  - D-NeRF：**20,000 次迭代**，训练约 **6 分钟**；每 8,000 步剪枝，15,000 步后禁用 3D 高斯增长；HexPlane 模块采用 ×2 上采样。
- **未明确说明**：论文未报告显存占用、能耗、多卡扩展性及超参数搜索成本；仅注明单卡设置。

## 5. 实验数量与充分性

- **实验组数**：2 个标准基准 + 1 组 6 配置消融 + 定性对比图（Plenoptic 上多场景、消融定性图），合计约 **3 大类、10 余组定量比较**。
- **充分性评估**：
  - **优点**：覆盖多视角与单目两类设定，对比方法涵盖 NeRF 系与 3DGS 系，消融逐项隔离各模块，定量+定性结合。
  - **局限**：数据集仅 2 个，场景类型偏少（以人物/物体运动为主）；消融仅在 D-NeRF 上进行，未在 Plenoptic 上重复；未报告多次运行的方差或显著性检验；对比方法的部分超参设置未详述。
- **公平性**：对比方法引用原始论文指标，训练/推理设置基本对齐；但 Deformable3DGS 在 D-NeRF 上 PSNR 更高（39.31 vs 35.24），论文以“交互式性能优先”作解释，属于合理但需读者自行权衡的取舍。

## 6. 主要结论与发现

- **Plenoptic Video**：达到 **33.84 dB PSNR / 0.965 SSIM / 0.07 LPIPS**，比最强基线高约 **+3.0 dB**；训练 35 分钟（比 K-Planes 快约 5.4×、比 HyperReel 快 15×+），推理 **120 FPS**（比 RealTime4DGS 快约 1.6×）。
- **D-NeRF**：**35.24 dB PSNR / 0.99 SSIM / 0.02 LPIPS**，比 TiNeuVox 高 +2.37 dB、比 K-Planes 高 +4.17 dB；训练 6 分钟、**300 FPS**。
- **消融关键发现**：
  - 仅启用源感知可压缩流（配置 b）即带来 **+3.53 dB PSNR、LPIPS 降低 74%**，且几乎无额外开销。
  - 仅启用流形/接触约束（配置 c）带来 **+1.33 dB PSNR、LPIPS 降低 63%**。
  - 两者同时启用（配置 d）达 **34.80 dB**；再加 GP（e）与 LL（f）分别提升至 35.00、35.24 dB，且训练时间从 13 分钟降至 8/6 分钟。
  - **LL 局部线性投影**优于 GP 逐基元投影，质量–效率权衡更佳。
- **总体结论**：源项显式建模、可控可压缩参数化与接触感知先验能在保持实时性的同时显著提升重建保真度与时序一致性，减少运动边界伪影。

## 7. 优点

- **建模创新**：
  - 引入**显式源项**分离运动驱动的密度变化与真实生成/消失，突破传统无源/不可压缩假设。
  - **Helmholtz + 仿射族**参数化将旋转、剪切、各向同性缩放解耦，参数少、鲁棒、可解释。
  - **隐式曲面 + 非穿透 + 库仑摩擦锥**统一粘着与滑动接触，提供闭式投影或小规模 SOCP 求解。
- **算法效率**：所有内层问题保持线性/凸结构，支持批量并行与闭式解，避免显式物理仿真；stop-gradient + Danskin 原理保证外层优化稳定。
- **可辨识性设计**：全局质量预算、零均值规范、边界感知基与渐进式课程（curriculum）逐步启用可压缩性与源项，缓解歧义。
- **实验表现**：在两大基准上同时取得 SOTA 保真度与显著领先的训练/推理速度，消融清晰、可复现性较好（单卡 RTX 3090 可复现）。

## 8. 不足与局限

- **实验覆盖**：
  - 仅 2 个数据集，场景多样性有限；未涉及大规模户外、多物体交互、强遮挡或极端光照变化场景。
  - 消融仅在 D-NeRF 上完成，未在 Plenoptic 上验证各模块的跨数据集泛化性。
  - 未报告运行方差、统计显著性或多随机种子结果。
- **方法与假设限制**
