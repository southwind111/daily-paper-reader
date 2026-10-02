---
title: "LumiMotion: Improving Gaussian Relighting with Scene Dynamics"
title_zh: LumiMotion：利用场景动态改进高斯重光照
authors: "Kaleta, Joanna, Wójcik, Piotr, Marzol, Kacper, Trzcinski, Tomasz, Kania, Kacper, Kowalski, Marek"
date: 2026
publication_date: 2026
publication_date_precision: year
publication_date_source: conference year only; exact release date unverified
publication_date_kind: unknown
pdf: "https://openaccess.thecvf.com/content/CVPR2026/papers/Kaleta_LumiMotion_Improving_Gaussian_Relighting_with_Scene_Dynamics_CVPR_2026_paper.pdf"
tags: ["query:dr"]
score: 5.0
evidence: 利用场景动态改进高斯重光照
tldr: 针对现有高斯泼溅逆渲染方法多面向静态场景、难以在真实条件下分离材质与光照的问题，本文提出LumiMotion。它把场景中发生运动的区域作为逆渲染的监督信号，因为运动让同一表面在不同光照下被观测，从而提供更强的解耦线索。实验表明该方法提升了材质与光照分离的准确性并改善重光照效果，说明场景动态可反哺逆渲染。
source: CVPR-2026-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-kaleta-lumimotion-improving-gaussian-relighting-with-scene-dynamics-cvpr-2026-paper/fig-001.webp\", \"caption\": \"\", \"page\": 1, \"index\": 1, \"width\": 1131, \"height\": 1588}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-kaleta-lumimotion-improving-gaussian-relighting-with-scene-dynamics-cvpr-2026-paper/fig-002.webp\", \"caption\": \"\", \"page\": 4, \"index\": 2, \"width\": 2958, \"height\": 1539}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-kaleta-lumimotion-improving-gaussian-relighting-with-scene-dynamics-cvpr-2026-paper/fig-003.webp\", \"caption\": \"\", \"page\": 5, \"index\": 3, \"width\": 6405, \"height\": 5064}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-kaleta-lumimotion-improving-gaussian-relighting-with-scene-dynamics-cvpr-2026-paper/fig-004.webp\", \"caption\": \"\", \"page\": 6, \"index\": 4, \"width\": 5284, \"height\": 1340}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-kaleta-lumimotion-improving-gaussian-relighting-with-scene-dynamics-cvpr-2026-paper/fig-005.webp\", \"caption\": \"\", \"page\": 6, \"index\": 5, \"width\": 3496, \"height\": 2010}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-kaleta-lumimotion-improving-gaussian-relighting-with-scene-dynamics-cvpr-2026-paper/fig-006.webp\", \"caption\": \"\", \"page\": 8, \"index\": 6, \"width\": 1853, \"height\": 832}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-kaleta-lumimotion-improving-gaussian-relighting-with-scene-dynamics-cvpr-2026-paper/fig-007.webp\", \"caption\": \"\", \"page\": 8, \"index\": 7, \"width\": 3274, \"height\": 1864}]"
motivation: 现有高斯泼溅逆渲染方法多针对静态场景，难以在真实光照条件下分离材质与光照。
method: 提出利用场景中运动区域作为逆渲染的监督信号，借助同一表面在不同光照下的观测解耦材质与光照。
result: 该方法提升了材质与光照分离的准确性，改善重光照效果。
conclusion: 表明动态元素可作为有用监督信号服务于逆渲染，拓展了高斯泼溅的应用。
---

## Abstract
In 3D reconstruction, the problem of inverse rendering, namely recovering the illumination of the scene and the material properties, is fundamental. Existing Gaussian Splatting-based methods primarily target static scenes and often assume simplified or moderate lighting to avoid entan- gling shadows with surface appearance. This limits their ability to accurately separate lighting effects from mate- rial properties, particularly in real-world conditions. We address this limitation by leveraging dynamic elements-- regions of the scene that undergo motion--as a supervisory signal for inverse rendering. Motion reveals the same sur- faces under varying lighting conditions, providing stronger cues for disentangling material and illumination. This the- sis is supported by our experimental results which show we improve LPIPS by 23% for albedo estimation and by 15% for scene relighting relative to next-best baseline. To this end, we introduce LumiMotion, the first Gaussian-based approach that leverages dynamics for inverse rendering and operates in arbitrary dynamic scenes. Our method learns a dynamic 2D Gaussian Splatting representation that em- ploys a set of novel constraints which encourage the dy- namic regions of the scene to deform, while keeping static regions stable. As we demonstrate, this separation is crucial for correct optimization of the albedo. Finally, we release a new synthetic benchmark comprising five scenes under four lighting conditions, each in both static and dynamic variants, for the first time enabling systematic evaluation of inverse rendering methods in dynamic environments and challenging lighting.

---

## 论文详细总结（自动生成）

# LumiMotion 论文总结

## 1. 核心问题与整体含义

- **研究背景**：逆渲染（inverse rendering）旨在从图像中恢复场景的几何、材质（反照率 albedo、粗糙度 roughness）与光照，是计算机视觉与图形学的基础问题。NeRF、Gaussian Splatting 等方法虽能高质量重建几何与视角合成，但把阴影等光照效应"烘焙"进了颜色中，导致场景无法在新光照下重新渲染（relighting）。
- **核心痛点**：现有基于高斯泼溅的逆渲染方法（如 IRGS、GI-GS、R-3DGS）几乎都面向**静态场景**，且常假设光照简化或适中，以回避"阴影与表面外观纠缠"的难题。在强方向光、显著阴影的真实场景中，这些方法难以正确分离材质与光照，反照率中会残留阴影，镜面分量优化不佳。
- **核心洞察（假设）**：静态场景下难以判断某区域变暗是因为被阴影遮挡还是材质本身偏暗。而**动态元素**（发生运动的区域）会让同一表面在不同时刻、不同光照下被观测，为解耦材质与光照提供更强的监督信号。
- **整体含义**：本文提出 **LumiMotion**——首个利用场景动态进行逆渲染、并适用于任意动态场景的高斯类方法，同时发布了一个新的合成基准，首次支持在动态环境与挑战性光照下系统评估逆渲染方法。

## 2. 方法论

### 2.1 核心思想
- 两阶段框架：
  - **Stage 1**：联合学习静态场景几何与形变网络（建模动态），显式分离静态/动态区域。
  - **Stage 2**：冻结几何与形变网络，改为通过光线追踪按渲染方程计算每个高斯的颜色，联合优化材质（albedo + roughness）与环境光照。
- 基座选用 **2D Gaussian Splatting (2DGS)**，因其能提供平滑准确的**表面法线**，这是逆渲染分离光照与材质的关键。

### 2.2 Stage 1：面向重光照的动态几何学习
- **形变建模**：MLP 根据位置编码的时间 $t$ 与高斯位置 $\mu$ 预测位置增量 $\Delta\mu$、旋转增量 $\Delta r$、颜色增量 $\Delta c$：
  $(\Delta\mu, \Delta r, \Delta c) = \text{MLP}(\text{enc}(t), \text{enc}(\mu))$
  刻意**不建模不透明度与尺度变化**，避免物体"凭空出现/消失"而非真实移动。
- **静态-动态模糊分离**：为每个高斯引入辅助变量 $P$（指示静态/动态），用 **Binary Concrete 分布**（Bernoulli 的连续松弛）采样得到 $\tilde P$，温度 $T=0.5$ 使其接近二值；推理时固定 $U=0.5$ 确定性取值。最终位置与旋转：
  $\mu' = \mu + \tilde P \Delta\mu,\quad r' = r + \tilde P \Delta r$
  这样动态变化被选择性施加，避免"移动阴影"被错误地建模为移动高斯。
- **时间颜色变化建模**：颜色用**乘法形式** $c' = c(1-\Delta c)$，模拟光照对表面的影响（移动阴影、动态元素受光变化），其中 $c$ 作为**伪反照率**，为 Stage 2 的材质分解提供初值。
- **损失函数**（总损失 $L_1$）：
  - 重建损失 $L_c$、法线一致性损失 $L_n$、深度畸变损失 $L_d$（沿用 2DGS）；
  - 前景掩码的二元交叉熵 $L_o$（处理漂浮高斯）；
  - **静态-动态分离损失** $L_P = \frac{1}{N}\sum |P_i|$（L1，鼓励高斯尽量保持静态）；
  - **颜色与位置变化正则** $L_{\Delta c}$、$L_{\Delta\mu}$（L2，抑制不必要的变化）。

### 2.3 Stage 2：逆渲染
- 每个 2D 高斯被赋予 **albedo $\rho$**（由 Stage 1 的规范颜色初始化）与 **roughness $\alpha$**，两者在时间上保持不变；此阶段不再使用 MLP 的 $\Delta c$，颜色变化仅来自渲染方程。
- 环境光照 $L_{env}$ 用一张图像建模（每像素对应一个方向的光强与颜色），与 $\rho$、$\alpha$ 联合优化。
- **着色方式**：采用 **deferred shading**——先光栅化得到 albedo / roughness / normal 的 G-buffer，再在像素级应用完整渲染方程，使阴影以像素粒度呈现。
- **渲染方程**采用 Disney BRDF（式 3），组合漫反射与镜面项；入射辐射由 $V(\omega_i,x)L_{env}(\omega_i) + L_{ind}(\omega_i,x)$ 给出，可见性 $V$ 通过 2D 高斯光线追踪求得，间接项 $L_{ind}$ 参照 IRGS 方式追踪。用**蒙特卡洛均匀分层采样** $N_r$ 个方向做积分（式 12）。
- **Stage 2 损失**：(1) Stage 1 的 $L_c$（约束高斯参数不过度偏离）；(2) 渲染结果对 GT 像素的 $L_1$；(3) 对 $L_{env}$ 低区高值的 $L_2$ 正则（权重 $\lambda_{env}$ 很小）。

## 3. 实验设计

- **新合成基准**：5 个不同场景 × 4 种光照环境（'Harbour Sunset'、'Dam Wall'、'Golden Bay'、'Chapel Day'）= 20 个变体；每个场景同时提供**静态与动态**两个版本，动态版采用 D-NeRF 式采集（每时间步一视图），静态版取同一相机位姿下的单时间步，测试集为**新视角**。场景在物体类型、运动模式、镜面程度上各异。
- **真实数据**：ENeRF 数据集的两个场景（室外、动态人物投射显著阴影、18 相机多视角），支持静态/动态模型训练评估，可与 IRGS 对比。
- **对比方法**：R-3DGS、GI-GS、IR-GS（均为静态方法，仅用单时间步多视角训练）。
- **评估指标**：PSNR、SSIM、LPIPS。
- **评估任务**：反照率估计与重光照质量；合成数据上采用 3 种训练/测试光照配置（如 Dam Wall→Harbour Sunset、Chapel Day→Golden Bay、Golden Bay→Dam Wall）。

## 4. 资源与算力

- 文中明确提到：所有实验在 **NVIDIA RTX 3090** 上进行，两个阶段训练每个合成场景约 **1.2 小时**。
- **未明确说明 GPU 数量**、总 GPU 时数或显存配置等细节；也未给出真实数据集 ENeRF 场景的具体训练时长。

## 5. 实验数量与充分性

- **定量实验**：表 2 覆盖 3 组训练-测试光照配置，每组在反照率与重光照两个任务上对比 3 个基线 + 本文方法，共 6 项指标。
- **消融实验**：表 3 在 Golden Bay→Dam Wall 配置下做 4 组对比（w/o Stage 2、w/o Δc、w/o P、完整模型）；图 6 研究了分离损失的权重与启动时机对动态元素识别的影响；图 7 单独展示静态-动态分离的作用。
- **定性实验**：图 3（新视角、重光照、分解分量、估计光照）、图 4（跨时间步一致性与法线稳定性）、图 1 与图 5（ENeRF 真实数据对比 IRGS）。
- **充分性与公平性评价**：
  - 优点：合成数据提供真值光照与材质，静态/动态版本配对使对比公平；静态基线使用相同相机位姿与单时间步，评测条件可比；消融覆盖了关键组件。
  - 局限：消融只在**单一场景配置**上进行，结论的泛化性有限；真实数据仅做**定性**对比（因无真值），缺乏定量指标；合成数据规模较小（5 场景），且真值来自渲染，可能无法完全反映真实光照复杂度。

## 6. 主要结论与发现

- 利用场景动态作为监督信号可显著改善材质与光照的分离：相对次优基线，**反照率 LPIPS 提升 23%，重光照 LPIPS 提升 15%**。
- 反照率估计在所有指标上大幅超越基线；重光照在多数情况下占优，且 LPIPS（最贴合感知质量）在所有情形下最佳。
- 显式的静态-动态分离至关重要：若不分离，高斯会通过移动来"模拟"阴影，导致反照率优化退化（图 7、表 3 中 w/o P 明显变差）。
- 动态建模有助于更准确估计光照方向，并防止阴影被"烘焙"进基础色；模型能生成跨时间步一致的法线与重光照结果。
- 结论：动态元素可作为逆渲染的有用监督信号，拓展了高斯泼溅在可重光照重建中的应用。

## 7. 优点

- **思想新颖**：首次将"场景动态"作为逆渲染的监督信号，用运动揭示同一表面在不同光照下的观测，为解耦材质/光照提供了物理上合理的线索。
- **方法设计巧妙**：
  - 用 Binary Concrete 分布实现可微的静态-动态软分离，并配合 $L_P$、$L_{\Delta c}$、$L_{\Delta\mu}$ 等正则，避免"移动阴影"污染反照率。
  - 颜色采用乘法式时间变化 $c(1-\Delta c)$，与光照物理更契合，同时规范颜色充当伪反照率初值，形成 Stage 1→Stage 2 的合理衔接。
  - 选用 2DGS 以获得可靠法线，deferred shading 让阴影以像素粒度呈现。
- **基准贡献**：发布的合成基准首次提供静态/动态配对 + 多种光照 + 真值材质/光照，便于公平、系统地评估动态逆渲染。
- **实用性强**：支持任意动态场景、物体类别无关、训练光照未知且为自然光照，突破了此前方法对静态场景或人体先验/已知光照的依赖。
- **实验对照充分**：同时做了合成定量、真实定性、消融与参数敏感性分析。

## 8. 不足与局限

- **作者自述局限**：
  - 性能高度依赖**准确的法线估计与形变质量**；在复杂动态场景中，时序一致且物理准确的运动与法线估计仍是开放难题，重建质量受限。
  - 简单的分离策略在**复杂动态**下可能产生伪影，可能需要光流等更强的监督。
  - 对**相机位姿估计误差、稀疏相机设置、初始化不准确**较为敏感。
- **实验覆盖**：
  - 真实数据（ENeRF）仅做定性对比，缺少定量评估；合成基准仅 5 个场景，规模偏小。
  - 消融实验仅在单一配置上完成，泛化性证据不足。
- **偏差风险**：合成数据的真值来自渲染，光照分布相对受控，可能低估真实世界中复杂/高频光照的难度；动态场景训练本身更难（重光照尤其依赖法线），可能掩盖部分方法的真实能力。
- **应用限制**：依赖视频序列且要求光照在采集期间基本静态；对拍摄条件（位姿精度、相机密度）要求较高，限制了在随意拍摄场景中的直接应用。
- **算力说明不完整**：未报告 GPU 数量与总训练开销，复现与成本评估的透明度有限。

（完）
