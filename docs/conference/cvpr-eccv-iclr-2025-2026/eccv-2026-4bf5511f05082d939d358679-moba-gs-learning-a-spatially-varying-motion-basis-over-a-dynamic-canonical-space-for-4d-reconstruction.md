---
title: "MoBa-GS: Learning a Spatially-Varying Motion Basis over a Dynamic Canonical Space for 4D Reconstruction"
title_zh: MoBa-GS：在动态规范空间上学习空间变化运动基用于4D重建
authors: "Guan Yuan Tan, Arghya Pal, Sailaja Rajanala, Raphaël Phan, Chee-Ming Ting"
date: 2026
publication_date: 2026
publication_date_precision: year
publication_date_source: conference year only; exact release date unverified
publication_date_kind: unknown
pdf: "https://media.eventhosts.cc/Conferences/ECCV2026/pdfs/11735.pdf"
tags: ["query:dr"]
score: 9.0
evidence: 通过空间变化运动基实现动态场景4D重建
tldr: 针对现有4D重建方法依赖单体形变网络或全局时间基分解、难以刻画复杂非刚性拓扑变化的问题，本文提出MoBa-GS框架，通过空间因子化运动场与自适应几何优化，先学习低频动态规范空间表示粗运动，再将其分解为空间变化运动基。实验表明该方法能更忠实地捕捉运动与几何的耦合关系，显著提升复杂动态场景的4D重建质量，为解耦运动与几何提供了新思路。
source: ECCV-2026-Accepted-Program
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-4bf5511f05082d939d358679/fig-001.webp\", \"caption\": \"\", \"page\": 3, \"index\": 1, \"width\": 1882, \"height\": 1427}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-4bf5511f05082d939d358679/fig-002.webp\", \"caption\": \"\", \"page\": 3, \"index\": 2, \"width\": 1200, \"height\": 1200}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-4bf5511f05082d939d358679/fig-003.webp\", \"caption\": \"\", \"page\": 3, \"index\": 3, \"width\": 480, \"height\": 270}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-4bf5511f05082d939d358679/fig-004.webp\", \"caption\": \"\", \"page\": 3, \"index\": 4, \"width\": 480, \"height\": 270}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-4bf5511f05082d939d358679/fig-005.webp\", \"caption\": \"\", \"page\": 3, \"index\": 5, \"width\": 480, \"height\": 270}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-4bf5511f05082d939d358679/fig-006.webp\", \"caption\": \"\", \"page\": 3, \"index\": 6, \"width\": 1882, \"height\": 1427}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-4bf5511f05082d939d358679/fig-007.webp\", \"caption\": \"\", \"page\": 3, \"index\": 7, \"width\": 1882, \"height\": 1427}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-4bf5511f05082d939d358679/fig-008.webp\", \"caption\": \"\", \"page\": 6, \"index\": 8, \"width\": 752, \"height\": 588}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-4bf5511f05082d939d358679/fig-009.webp\", \"caption\": \"\", \"page\": 6, \"index\": 9, \"width\": 792, \"height\": 520}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-4bf5511f05082d939d358679/fig-010.webp\", \"caption\": \"\", \"page\": 6, \"index\": 10, \"width\": 1067, \"height\": 574}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-4bf5511f05082d939d358679/fig-011.webp\", \"caption\": \"\", \"page\": 6, \"index\": 11, \"width\": 678, \"height\": 520}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-4bf5511f05082d939d358679/fig-012.webp\", \"caption\": \"\", \"page\": 6, \"index\": 12, \"width\": 532, \"height\": 414}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-4bf5511f05082d939d358679/fig-013.webp\", \"caption\": \"\", \"page\": 7, \"index\": 13, \"width\": 5160, \"height\": 2670}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-4bf5511f05082d939d358679/fig-014.webp\", \"caption\": \"\", \"page\": 10, \"index\": 14, \"width\": 480, \"height\": 270}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-4bf5511f05082d939d358679/fig-015.webp\", \"caption\": \"\", \"page\": 10, \"index\": 15, \"width\": 480, \"height\": 270}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-4bf5511f05082d939d358679/fig-016.webp\", \"caption\": \"\", \"page\": 10, \"index\": 16, \"width\": 480, \"height\": 270}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-4bf5511f05082d939d358679/fig-017.webp\", \"caption\": \"\", \"page\": 10, \"index\": 17, \"width\": 480, \"height\": 270}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-4bf5511f05082d939d358679/fig-018.webp\", \"caption\": \"\", \"page\": 10, \"index\": 18, \"width\": 480, \"height\": 270}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-4bf5511f05082d939d358679/fig-019.webp\", \"caption\": \"\", \"page\": 10, \"index\": 19, \"width\": 480, \"height\": 270}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-4bf5511f05082d939d358679/fig-020.webp\", \"caption\": \"\", \"page\": 10, \"index\": 20, \"width\": 480, \"height\": 270}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-4bf5511f05082d939d358679/fig-021.webp\", \"caption\": \"\", \"page\": 10, \"index\": 21, \"width\": 480, \"height\": 270}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-4bf5511f05082d939d358679/fig-022.webp\", \"caption\": \"\", \"page\": 10, \"index\": 22, \"width\": 480, \"height\": 270}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-4bf5511f05082d939d358679/fig-023.webp\", \"caption\": \"\", \"page\": 10, \"index\": 23, \"width\": 480, \"height\": 270}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-4bf5511f05082d939d358679/fig-024.webp\", \"caption\": \"\", \"page\": 10, \"index\": 24, \"width\": 480, \"height\": 270}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-4bf5511f05082d939d358679/fig-025.webp\", \"caption\": \"\", \"page\": 10, \"index\": 25, \"width\": 480, \"height\": 270}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-4bf5511f05082d939d358679/fig-026.webp\", \"caption\": \"\", \"page\": 10, \"index\": 26, \"width\": 480, \"height\": 270}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-4bf5511f05082d939d358679/fig-027.webp\", \"caption\": \"\", \"page\": 10, \"index\": 27, \"width\": 480, \"height\": 270}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-4bf5511f05082d939d358679/fig-028.webp\", \"caption\": \"\", \"page\": 10, \"index\": 28, \"width\": 480, \"height\": 270}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-4bf5511f05082d939d358679/fig-029.webp\", \"caption\": \"\", \"page\": 10, \"index\": 29, \"width\": 480, \"height\": 270}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-4bf5511f05082d939d358679/fig-030.webp\", \"caption\": \"\", \"page\": 10, \"index\": 30, \"width\": 480, \"height\": 270}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-4bf5511f05082d939d358679/fig-031.webp\", \"caption\": \"\", \"page\": 10, \"index\": 31, \"width\": 480, \"height\": 270}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-4bf5511f05082d939d358679/fig-032.webp\", \"caption\": \"\", \"page\": 10, \"index\": 32, \"width\": 480, \"height\": 270}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-4bf5511f05082d939d358679/fig-033.webp\", \"caption\": \"\", \"page\": 10, \"index\": 33, \"width\": 480, \"height\": 270}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-4bf5511f05082d939d358679/fig-034.webp\", \"caption\": \"\", \"page\": 12, \"index\": 34, \"width\": 536, \"height\": 960}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-4bf5511f05082d939d358679/fig-035.webp\", \"caption\": \"\", \"page\": 12, \"index\": 35, \"width\": 536, \"height\": 960}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-4bf5511f05082d939d358679/fig-036.webp\", \"caption\": \"\", \"page\": 12, \"index\": 36, \"width\": 536, \"height\": 960}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-4bf5511f05082d939d358679/fig-037.webp\", \"caption\": \"\", \"page\": 12, \"index\": 37, \"width\": 536, \"height\": 960}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-4bf5511f05082d939d358679/fig-038.webp\", \"caption\": \"\", \"page\": 12, \"index\": 38, \"width\": 268, \"height\": 480}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-4bf5511f05082d939d358679/fig-039.webp\", \"caption\": \"\", \"page\": 12, \"index\": 39, \"width\": 536, \"height\": 960}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-4bf5511f05082d939d358679/fig-040.webp\", \"caption\": \"\", \"page\": 12, \"index\": 40, \"width\": 536, \"height\": 960}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-4bf5511f05082d939d358679/fig-041.webp\", \"caption\": \"\", \"page\": 12, \"index\": 41, \"width\": 536, \"height\": 960}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-4bf5511f05082d939d358679/fig-042.webp\", \"caption\": \"\", \"page\": 12, \"index\": 42, \"width\": 536, \"height\": 960}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-4bf5511f05082d939d358679/fig-043.webp\", \"caption\": \"\", \"page\": 12, \"index\": 43, \"width\": 268, \"height\": 480}]"
motivation: 现有4D重建方法依赖单体形变网络或全局时间基分解，难以表示复杂的非刚性拓扑变化。
method: 提出空间因子化运动场与自适应几何优化，先学习低频动态规范空间，再将非刚性运动分解为空间变化运动基。
result: 在动态场景中更忠实地捕捉运动与几何关系，提升复杂非刚性形变的4D重建质量。
conclusion: 为动态场景4D重建提供了分离运动与几何纠缠的新框架。
---

## Abstract
Faithfully capturing the intricate relationship between motion and geometry in dynamic scenes is essential for 4D reconstruction. Recent state-of-the-art methods rely on monolithic deformation networks or global time-basis factorizations that struggle to represent complex, non-rigid topological changes. We propose MoBa-GS, a framework that resolves this entanglement by introducing a structural inversion: a spatially-factorized motion field coupled with adaptive geometric optimization. First, our model learns a low-frequency dynamic canonical space to represent coarse scene motion. Next, it decomposes complex, non-rigid motion into a Spatially-Varying Motion Basis of local kinematics, predicted from the canonical geometry, which is then linearly combined using dynamic blending weights. This formulation directly acts as an implicit neural scaffold, recovering both geometry and motion from random initialization, thereby removing the dependency on SfM point cloud priors. This design is further augmented with motion-guided densification and positional annealing to reduce geometry overfitting. Extensive experiments show that our framework surpasses prior state-of-theart methods in reconstruction fidelity. Enabled by time-invariant caching, MoBa-GS requires an order-of-magnitude shorter training time (<18 minutes), a compact storage (∼ 11 MB), and achieves real-time rendering speeds (>163 FPS). Our work establishes a new foundation for highfidelity, efficient 4D representations without relying on explicit geometric priors. Code is available at https://github.com/tgy1221/MoBa-GS.

---

## 论文详细总结（自动生成）

## 1. 核心问题与研究背景

- **研究动机**：动态场景的4D重建需要同时建模几何与运动，并忠实捕捉二者耦合关系。现有动态3DGS方法主要依赖两类范式：
  - **单体形变网络**：用单个MLP预测规范高斯随时间的形变，易导致几何与运动纠缠，产生“移动目标”问题，训练不稳定且几何过拟合严重。
  - **全局时间基分解**：假设场景由有限全局轨迹基组成，难以表示高度异质、局部的非刚性运动，如布料褶皱、流体等；若强行表示，会导致基秩爆炸。
- **共同瓶颈**：上述方法通常依赖COLMAP等SfM点云初始化。动态主体上SfM特征匹配易失败，导致方法在缺少高质量几何先验时崩溃或产生严重伪影。
- **整体含义**：论文提出MoBa-GS，通过“结构反转”——从全局时间基转向**空间变化运动基**，将运动能力绑定到空间位置，从而在随机初始化下恢复高质量几何与运动，并兼顾效率与实时渲染。

## 2. 方法论

### 2.1 核心思想

- 将4D形变场分解为：
  - **低频基础运动**：学习一个动态规范空间，作为粗运动先验。
  - **高频残差运动**：用空间变化的局部运动基表示，并通过动态混合权重线性组合。
- 该设计相当于一种**隐式神经支架**：将每个点的运动约束在局部低维流形上，减少对SfM点云先验的依赖。
- 由于基预测器仅依赖静态规范坐标，可实现**时间不变缓存**，推理时跳过MLP开销，将形变计算退化为轻量点积。

### 2.2 关键技术细节

- **动态规范空间**：
  - 基础运动网络 \(\mathcal{D}_{\text{base}}\) 是一个轻量MLP，使用低频时间位置编码 \(L=4\)。
  - 输出基础位移 \(\Delta p_{\text{base}}\)，将规范位置 \(p_{\text{canon}}\) 变形为动态规范空间：
    \[
    p'(t)=p_{\text{canon}}+\Delta p_{\text{base}}(p_{\text{canon}},\gamma_{t,L=4}(t))
    \]
  - 作用：吸收全局平移、相机自运动等低频信号，减轻残差网络负担。

- **空间变化运动基分解**：
  - **基场**：基预测器 \(\mathcal{B}\) 仅以静态规范位置为输入，为每个点生成 \(K\) 个基向量：
    \[
    \mathbf{V}(p_{\text{canon}})=\{\mathbf{b}_1,\dots,\mathbf{b}_K\}=\mathcal{B}(\gamma_{\text{pos}}(p_{\text{canon}}))
    \]
  - **系数场**：权重预测器 \(\mathcal{W}\) 以动态规范位置 \(p'(t)\) 和高频时间编码 \(L=10\) 为输入，输出 \(K\) 个动态混合权重：
    \[
    \mathbf{w}(p',t)=\{w_1,\dots,w_K\}=\mathcal{W}(p'(t),\gamma_{t,L=10}(t))
    \]
  - **运动合成**：残差位移通过基向量线性组合得到：
    \[
    \Delta p_{\text{res}}=\mathbf{V}(p_{\text{canon}})\mathbf{w}(p',t)=\sum_{k=1}^{K}w_k(p',t)\cdot \mathbf{b}_k(p_{\text{canon}})
    \]
  - 最终位置为 \(p(t)=p'(t)+\Delta p_{\text{res}}\)，旋转与尺度也有独立输出头。

- **内在结构先验**：
  - 强制4D轨迹落在学习到的空间基的稀疏组合上，形成局部低维运动流形。
  - 引入动态加速度惩罚：对运动点指数衰减，保证静态区域刚性、动态区域保留运动自由度。

- **运动引导致密化**：
  - 高斯点仅在同时满足视图空间梯度大和预测运动幅度大时才可致密化：
    \[
    \text{Densify}(G_i)\ \text{if}\ \|\nabla_{\mathbf{xyz}}(G_i)\|>\tau_{\text{grad}}\ \land\ \|\Delta p_i(t)\|>\tau_{\text{motion}}
    \]
  - 将几何容量优先分配给外观复杂且动态显著的区域，避免静态背景浪费容量。

- **位置退火**：
  - 两阶段学习率调度：训练前期正常更新规范位置，后期降低/冻结规范位置学习率。
  - 目的：缓解几何过拟合，迫使运动网络吸收剩余时空变化，提升泛化。

- **解耦交替优化**：
  - **形变聚焦阶段**：冻结规范高斯参数，训练形变网络 \(N_{\text{def}}=2\) 次。
  - **几何聚焦阶段**：冻结形变网络，训练规范高斯参数 \(N_{\text{geo}}=1\) 次。
  - **位置退火阶段**：达到阈值后逐步冻结规范空间。
  - 该策略打破几何与运动互为“移动目标”的不稳定反馈环。

- **损失函数**：
  \[
  \mathcal{L}=(1-\lambda_{\text{dssim}})\cdot\mathcal{L}_1+\lambda_{\text{dssim}}\cdot\mathcal{L}_{\text{dssim}}
  \]
  使用L1与D-SSIM组合损失进行端到端训练。

## 3. 实验设计

- **数据集/场景**：
  - **NeRF-DS**：单目真实世界动态场景，共7个场景：As、Basin、Bell、Cup、Plate、Press、Sieve。
  - **HyperNeRF**：包含更极端形变的单目动态场景，评估4个场景：3D Printer、Chicken、Broom、Banana。
- **评价指标**：
  - NeRF-DS：PSNR、SSIM、LPIPS。
  - HyperNeRF：PSNR、SSIM；按文献[56]惯例省略LPIPS，因剧烈相机运动使LPIPS不稳定。
- **对比方法**：
  - 3DGS、Deformable-GS、4DGS、SC-GS、D-MiSo、Motion-GS。
  - 未与DynMF比较，原因是官方代码未公开。
- **实验类型**：
  - NeRF-DS定量与定性比较。
  - HyperNeRF定量与定性比较。
  - 计算成本分析：训练时间、推理FPS、高斯数量、存储大小。
  - 消融实验：移除位置退火、运动引导致密化、空间变化运动基；变化基数量 \(K\in\{2,4,8,16,32\}\)。
- **实现细节**：
  - PyTorch实现；基础运动网络为4层MLP，隐藏维度128，时间编码 \(L=4\)。
  - 残差形变网络包含2层基预测器和8层主干，隐藏维度256。
  - 运动基数量默认 \(K=8\)。
  - 单张NVIDIA A100 GPU训练。

## 4. 资源与算力

- 文中明确说明所有实验在**单张NVIDIA A100 GPU**上完成。
- 训练时长：
  - MoBa-GS平均约 **13.3分钟** 收敛，最长约18分钟，最短约9分钟。
  - 相比领先基线D-MiSo平均约3小时27分钟，实现**超过16倍加速**。
- 推理与存储：
  - 平均渲染速度 **163 FPS**，Sieve场景最高 **237 FPS**。
  - 平均约 **39K高斯/场景**，总框架存储约 **11.3 MB**。
- **未明确说明**：
  - GPU数量、总训练卡时、能耗、是否使用混合精度、CPU/内存占用等。
  - 对比方法的训练资源是否完全一致，仅说明使用官方公开代码和默认配置。

## 5. 实验数量与充分性

- **实验数量概览**：
  - 两个数据集，共11个场景的定量比较。
  - 与6个动态3DGS/相关基线方法对比。
  - 训练时间对比覆盖NeRF-DS全部7个场景。
  - 推理速度、高斯数量、存储大小覆盖7个场景。
  - 消融实验包括3个组件移除和5个基数量设置，共8组主要消融配置。
  - 多组定性可视化，包括NeRF-DS与HyperNeRF。
- **充分性评价**：
  - 整体较充分，覆盖主流动态场景基准、效率分析和核心模块消融。
  - 基数量 \(K\) 的U形曲线分析增强了方法可解释性。
  - 但未与DynMF对比，削弱了与最相关全局时间基方法的直接比较。
  - HyperNeRF省略LPIPS，评价维度略少。
  - 缺少多视角、多相机、大规模场景或跨数据集泛化实验。
  - 未报告统计显著性、误差棒或多次运行方差。
- **客观性与公平性**：
  - 使用官方代码默认配置进行公平比较，是合理做法。
  - 但不同方法的训练时间、超参调优程度、是否共享相同相机位姿和初始化条件未完全披露。
  - LPIPS低于D-MiSo，作者引用文献解释VGG感知指标可能偏好过度平滑，但该解释仍需更多独立验证。

## 6. 主要结论与发现

- MoBa-GS在NeRF-DS和HyperNeRF上均取得最高的平均PSNR和SSIM，重建保真度优于现有SOTA动态3DGS方法。
- 空间变化运动基是性能提升的核心：移除后PSNR下降0.66 dB，降幅最大。
- 运动引导致密化和位置退火分别带来约0.31 dB和0.27 dB的PSNR提升，证明二者有效。
- 基数量 \(K=8\) 为最优结构正则化点；过低欠拟合，过高过拟合，呈对称U形容量曲线。
- 时间不变缓存使推理退化为轻量点积，实现实时渲染；训练时间、存储和高斯数量均显著优于基线。
- 方法可在随机初始化下恢复几何与运动，无需SfM点云先验，降低对COLMAP初始化的依赖。
- 学习到的运动基具有可解释性：刚性点基分布更广，非刚性点基方向更集中，体现空间变化的运动字典。

## 7. 优点

- **结构创新明确**：从全局时间基反转为空间变化运动基，直接针对全局基秩爆炸和异质非刚性运动问题。
- **无SfM依赖**：隐式神经支架使随机初始化成为可行，提升在动态主体上SfM失败场景的鲁棒性。
- **效率突出**：
  - 时间不变缓存显著降低推理开销。
  - 训练时间短、模型紧凑、渲染速度快。
- **训练策略协同**：
  - 运动引导致密化将容量分配到动态复杂区域。
  - 位置退火和交替优化缓解几何过拟合与“移动目标”问题。
- **可解释性较好**：可视化基向量与动态权重，展示运动基确实学习到局部运动原语。
- **实验覆盖较广**：两个挑战性单目动态数据集、多基线、效率分析和消融实验，结论支撑较完整。

## 8. 不足与局限

- **实验覆盖有限**：
  - 仅评估单目真实世界数据集，未涉及多视角、合成大规模或户外开放场景。
  - 未与DynMF直接比较，而DynMF是最相关的全局时间基分解方法。
  - HyperNeRF省略LPIPS，指标完整性不足。
- **评价偏差风险**：
  - LPIPS低于D-MiSo，作者以VGG感知指标偏好平滑解释，但缺乏更深入的用户研究或替代感知指标验证。
  - 未报告多次运行方差、误差棒或统计显著性。
- **方法假设限制**：
  - 仍假设残差运动在局部低维，对极端拓扑变化、流体、碎裂等可能不适用。
  - 基数量 \(K\) 是敏感超参，需逐场景或逐数据集选择。
  - 虽不依赖SfM点云，但仍依赖相机位姿等标定信息，未讨论位姿误差影响。
- **资源与扩展性**：
  - 仅说明单张A100训练，未报告GPU数量、总卡时和能耗。
  - 每个场景需单独优化，不是前馈泛化模型；测试时优化虽快，但仍需训练过程。
  - 与feed-forward模型相比，缺少跨场景先验和泛化能力。
- **应用限制**：
  - 实时渲染和紧凑存储在A100上测得，消费级GPU上的实际表现未验证。
  - 对长序列、边界连续性、动态拓扑变化等未做专门压力测试。

（完）
