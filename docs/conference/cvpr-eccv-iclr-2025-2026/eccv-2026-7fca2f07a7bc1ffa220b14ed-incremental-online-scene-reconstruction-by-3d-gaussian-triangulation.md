---
title: Incremental Online Scene Reconstruction by 3D Gaussian Triangulation
title_zh: 基于三维高斯三角化的增量在线场景重建
authors: "Yanjin Zhu, Shaofan Liu, Jianke Zhu"
date: 2026
publication_date: 2026
publication_date_precision: year
publication_date_source: conference year only; exact release date unverified
publication_date_kind: unknown
pdf: "https://media.eventhosts.cc/Conferences/ECCV2026/pdfs/472.pdf"
tags: ["query:dr"]
score: 5.0
evidence: 通过三维高斯三角化进行在线增量场景重建与网格更新
tldr: 增量场景重建对实际应用至关重要，但多数三维高斯泼溅方法需离线将优化后的高斯转换为隐式场再提取网格，难以与下游任务无缝集成。本文提出一种在线框架，直接对稠密几何高斯表示进行三角化，增量地重建并更新高保真显式网格，并设计了高效的直接网格化算法从高斯集合中提取与更新网格。该方法同时支持高质量渲染与增量表面重建，为在线重建提供了显式网格方案。
source: ECCV-2026-Accepted-Program
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-7fca2f07a7bc1ffa220b14ed/fig-001.webp\", \"caption\": \"\", \"page\": 2, \"index\": 1, \"width\": 443, \"height\": 346}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-7fca2f07a7bc1ffa220b14ed/fig-002.webp\", \"caption\": \"\", \"page\": 2, \"index\": 2, \"width\": 420, \"height\": 385}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-7fca2f07a7bc1ffa220b14ed/fig-003.webp\", \"caption\": \"\", \"page\": 2, \"index\": 3, \"width\": 463, \"height\": 346}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-7fca2f07a7bc1ffa220b14ed/fig-004.webp\", \"caption\": \"\", \"page\": 2, \"index\": 4, \"width\": 506, \"height\": 315}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-7fca2f07a7bc1ffa220b14ed/fig-005.webp\", \"caption\": \"\", \"page\": 2, \"index\": 5, \"width\": 377, \"height\": 354}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-7fca2f07a7bc1ffa220b14ed/fig-006.webp\", \"caption\": \"\", \"page\": 5, \"index\": 6, \"width\": 510, \"height\": 414}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-7fca2f07a7bc1ffa220b14ed/fig-007.webp\", \"caption\": \"\", \"page\": 5, \"index\": 7, \"width\": 499, \"height\": 294}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-7fca2f07a7bc1ffa220b14ed/fig-008.webp\", \"caption\": \"\", \"page\": 5, \"index\": 8, \"width\": 499, \"height\": 294}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-7fca2f07a7bc1ffa220b14ed/fig-009.webp\", \"caption\": \"\", \"page\": 10, \"index\": 9, \"width\": 698, \"height\": 385}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-7fca2f07a7bc1ffa220b14ed/fig-010.webp\", \"caption\": \"\", \"page\": 10, \"index\": 10, \"width\": 734, \"height\": 400}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-7fca2f07a7bc1ffa220b14ed/fig-011.webp\", \"caption\": \"\", \"page\": 10, \"index\": 11, \"width\": 666, \"height\": 551}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-7fca2f07a7bc1ffa220b14ed/fig-012.webp\", \"caption\": \"\", \"page\": 10, \"index\": 12, \"width\": 708, \"height\": 392}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-7fca2f07a7bc1ffa220b14ed/fig-013.webp\", \"caption\": \"\", \"page\": 10, \"index\": 13, \"width\": 665, \"height\": 550}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-7fca2f07a7bc1ffa220b14ed/fig-014.webp\", \"caption\": \"\", \"page\": 10, \"index\": 14, \"width\": 706, \"height\": 403}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-7fca2f07a7bc1ffa220b14ed/fig-015.webp\", \"caption\": \"\", \"page\": 10, \"index\": 15, \"width\": 688, \"height\": 402}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-7fca2f07a7bc1ffa220b14ed/fig-016.webp\", \"caption\": \"\", \"page\": 10, \"index\": 16, \"width\": 688, \"height\": 441}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-7fca2f07a7bc1ffa220b14ed/fig-017.webp\", \"caption\": \"\", \"page\": 11, \"index\": 17, \"width\": 1200, \"height\": 680}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-7fca2f07a7bc1ffa220b14ed/fig-018.webp\", \"caption\": \"\", \"page\": 11, \"index\": 18, \"width\": 1200, \"height\": 680}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-7fca2f07a7bc1ffa220b14ed/fig-019.webp\", \"caption\": \"\", \"page\": 11, \"index\": 19, \"width\": 1200, \"height\": 680}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-7fca2f07a7bc1ffa220b14ed/fig-020.webp\", \"caption\": \"\", \"page\": 11, \"index\": 20, \"width\": 1200, \"height\": 680}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-7fca2f07a7bc1ffa220b14ed/fig-021.webp\", \"caption\": \"\", \"page\": 11, \"index\": 21, \"width\": 590, \"height\": 393}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-7fca2f07a7bc1ffa220b14ed/fig-022.webp\", \"caption\": \"\", \"page\": 11, \"index\": 22, \"width\": 590, \"height\": 393}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-7fca2f07a7bc1ffa220b14ed/fig-023.webp\", \"caption\": \"\", \"page\": 11, \"index\": 23, \"width\": 590, \"height\": 393}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-7fca2f07a7bc1ffa220b14ed/fig-024.webp\", \"caption\": \"\", \"page\": 11, \"index\": 24, \"width\": 590, \"height\": 393}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-7fca2f07a7bc1ffa220b14ed/fig-025.webp\", \"caption\": \"\", \"page\": 14, \"index\": 25, \"width\": 788, \"height\": 591}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-7fca2f07a7bc1ffa220b14ed/fig-026.webp\", \"caption\": \"\", \"page\": 14, \"index\": 26, \"width\": 788, \"height\": 591}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-7fca2f07a7bc1ffa220b14ed/fig-027.webp\", \"caption\": \"\", \"page\": 14, \"index\": 27, \"width\": 788, \"height\": 591}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-7fca2f07a7bc1ffa220b14ed/fig-028.webp\", \"caption\": \"\", \"page\": 14, \"index\": 28, \"width\": 788, \"height\": 591}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-7fca2f07a7bc1ffa220b14ed/fig-029.webp\", \"caption\": \"\", \"page\": 14, \"index\": 29, \"width\": 614, \"height\": 369}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-7fca2f07a7bc1ffa220b14ed/fig-030.webp\", \"caption\": \"\", \"page\": 14, \"index\": 30, \"width\": 610, \"height\": 369}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-7fca2f07a7bc1ffa220b14ed/fig-031.webp\", \"caption\": \"\", \"page\": 14, \"index\": 31, \"width\": 614, \"height\": 369}, {\"url\": \"assets/figures/eccv-2026-accepted-program/eccv-2026-7fca2f07a7bc1ffa220b14ed/fig-032.webp\", \"caption\": \"\", \"page\": 14, \"index\": 32, \"width\": 613, \"height\": 369}]"
motivation: 现有三维高斯泼溅方法多需离线将高斯转为隐式场再提取网格，难以与下游任务集成。
method: 提出在线框架，直接对稠密几何高斯表示进行三角化，增量重建并更新显式网格，并设计直接网格化算法。
result: 同时支持高质量渲染与增量表面重建，实现网格的高效提取与更新。
conclusion: 为在线增量场景重建与下游任务集成提供了显式网格方案。
---

## Abstract
Incremental scene reconstruction is essential for real-worldapplications. Although 3D Gaussian Splatting shows strong potential,most existing approaches require offline conversion of the optimized Gaus-sians into an intermediate implicit field for explicit mesh extraction,which hinders seamless integration with downstream tasks. To addressthis limitation, we propose a novel online framework that incrementallyreconstructs and updates high-fidelity explicit meshes by directly trian-gulating a dense geometric Gaussian representation, which supports bothhigh-quality rendering and incremental surface reconstruction. More-over, we present a direct meshing algorithm that efficiently extractsand updates the mesh from the Gaussian set. To ensure mesh accu-racy, we enforce a plane-based pulling constraint that dynamically aligns3D Gaussian primitives to the approximated local surface. Furthermore,our framework significantly reduces memory and computational overheadduring long-sequence processing by dynamically freezing fully optimizedhistorical regions. Experiments on public datasets demonstrate that ourmethod outperforms conventional Gaussian-based methods on both ren-dering quality and reconstruction accuracy.

---

## 论文详细总结（自动生成）

# 论文总结：基于三维高斯三角化的增量在线场景重建

## 1. 核心问题与研究动机

- **背景**：三维场景重建是计算机视觉与机器人领域的核心任务，广泛应用于增强现实（AR）与场景感知。现有方法主要分为隐式方法（如 NeRF）与显式方法（如 KinectFusion 的 TSDF 体素融合）。
- **核心痛点**：
  - 多数高保真重建方法需**离线处理完整场景**后才能生成网格，无法满足实时决策需求；
  - 传统 TSDF 方法受限于固定体素分辨率与高内存消耗，难以进行细节捕获和大规模重建；
  - NeRF 类隐式方法训练/渲染计算量大，无界场景可扩展性差，提取显式网格仍需稠密采样与离线后处理；
  - 现有 3DGS 网格重建方法（如 SuGaR、2D GS）通常**解耦网格提取与高斯表示**，依赖全局 Poisson 重建或 Marching Cubes，需对完全优化的高斯集合进行离线处理，难以与下游任务无缝集成。
- **研究目标**：提出一种**增量在线场景重建框架**，将优化后的 3D 高斯视为面元基元直接进行三角化，实现在线、增量地重建并更新高保真显式网格，同时支持高质量渲染。

## 2. 方法论

### 2.1 核心思想
- 将 3D 高斯泼溅的显式表示与增量网格重建统一：把优化后的 3D 高斯当作**平面椭圆面元（Planar Elliptical Surfels）**，直接从高斯集合三角化生成水密网格，避免构建中间隐式场。

### 2.2 关键技术细节

- **稠密几何高斯表示**：
  - 每个高斯包含均值 $\mu_i$、不透明度 $\alpha_i$、颜色 $c_i$、尺度 $s_i$、旋转 $R_i$；
  - **平面约束**：强制第三尺度分量 $s_i^3 \to 0$，使高斯扁平化为局部切平面；
  - **不透明度约束**：强制 $\alpha_i \approx 1$，逼近硬物理几何。

- **高斯初始化**：
  - 从 RGB-D 流增量构建的有向点云初始化，均值 $\mu_i$ 继承点位置 $p_i$；
  - 旋转矩阵第三列 $r_i^3$ 对齐法向量 $n_i$；
  - 切向尺度由局部点间距决定：$s_i^1 = s_i^2 = \lambda \cdot \max_{j \in \mathcal{N}(i)} \|p_i - p_j\|_2$（$k=4$，$\lambda=1.5$），$s_i^3 = 10^{-6}$，$\alpha_i = 0.99$。

- **几何感知可微渲染**：
  - RGB 渲染采用标准 alpha 混合；
  - 深度渲染通过计算视线与**前向不透明高斯**的交点得到，而非 alpha 混合深度，以建模局部几何平面。

- **在线建图**：
  - **高斯添加**：基于新到有向点云添加高斯；对深度差异显著区域添加不透明高斯补全几何，对 RGB 差异区域添加透明高斯（$\alpha_i=0.1$）增强渲染。
  - **高斯剪枝**：剪除不参与深度渲染的不透明高斯及对光度贡献极小的透明高斯。
  - **高斯优化**：随机采样单帧迭代优化，损失函数为：
    $$\mathcal{L} = \lambda_c \mathcal{L}_{color} + \lambda_d \mathcal{L}_{depth} + \lambda_p \mathcal{L}_{plane} + \lambda_n \mathcal{L}_n + \lambda_s \mathcal{L}_{sparse}$$
    其中 $\mathcal{L}_{plane}$ 为局部平面拉近损失，$\mathcal{L}_n$ 为法向一致性损失，$\mathcal{L}_{sparse}$ 为稀疏损失。

- **高斯三角化**：
  - **几何高斯集选择**：依据不透明度（$\alpha_g > 0.9$）与深度保真度（$|(T_{cw}\mu_g)_z - D| < \tau$）筛选，去除仅用于渲染的透明高斯与几何不准基元。
  - **快速三角化**：使用压缩八叉树加速邻居搜索；基于切平面相互可见性与法向一致性（$\langle n_i, n_j \rangle > 0.9$）筛选有效邻居；加权融合精化高斯位置后二次搜索；在切平面上按极角排序，采用角度贪心策略连接三角形，限制最小张角 $10°$ 避免狭长三角形。

- **局部重网格化与冻结**：
  - 局部网格融合时采用各向同性网格优化（边分裂、边折叠、边翻转、Laplacian 平滑，迭代 3 次）消除拓扑冲突；
  - **冻结策略**：当局部区域累计有效观测数超过 $N_{obs}$ 且损失收敛至 $\epsilon_{gs}$ 时，将该区域高斯与网格移出活动优化计算图并冻结，实现长序列处理的内存高效性。

## 3. 实验设计

- **数据集**：
  - **Replica**：8 个序列（客厅与办公室场景）；
  - **ScanNet++**：2 个 DSLR 采集场景（8b5caf3398 记为 S1，b20a261fdf 记为 S2）。
- **Benchmark 与评价指标**：
  - 重建质量：Accuracy（cm）、Accuracy Ratio（<5cm）、Completion Ratio（<5cm）；
  - 渲染质量：PSNR、SSIM、LPIPS；
  - 效率：FPS、峰值内存（MB）、网格大小（MB）、网格提取时间（s）。
- **对比方法**：
  - 体素 TSDF 方法 KinectFusion；
  - NeRF RGB-D SLAM 方法 NICE-SLAM、Point-SLAM；
  - 高斯 SLAM 方法 MonoGS、RTG-SLAM；
  - 网格提取效率对比方法 Gaussian Opacity Fields（GOF，含 MC 与 PSR 两种后端）。
- **实现细节**：Python 实现，高斯三角化与有向点云生成封装为 C++ 模块，CUDA 加速；损失权重 $\lambda_c=0.8, \lambda_d=1.0, \lambda_p=0.05, \lambda_n=0.2, \lambda_s=0.001$；$\tau=0.001$，$N_{obs}=10$，$\epsilon_{gs}=0.1$；Replica 活动窗口 6、迭代 50 次，ScanNet++ 活动窗口 3、迭代 75 次；所有基线使用真值位姿以保证公平。

## 4. 资源与算力

- 论文明确提到实验在**单张 NVIDIA RTX 3090 GPU** 的 PC 上进行。
- **未明确说明**：GPU 数量、总训练时长、具体能耗等细节；也未提供不同硬件配置下的对比数据。

## 5. 实验数量与充分性

- **实验组数概览**：
  - Replica 重建精度对比（Tab. 1，8 个序列 × 5 种方法）；
  - Replica 渲染质量对比（Tab. 2，8 个序列 × 5 种方法）；
  - ScanNet++ 新视角与训练视角渲染对比（Tab. 3，2 个场景 × 3 种方法）；
  - 效率对比：映射 FPS 与峰值内存（Tab. 4，3 种方法）；
  - 网格提取效率对比（Tab. 5，GOF-MC / GOF-PSR / Ours）；
  - 消融实验（Tab. 6）：核心模块（平面约束、邻域选择、直接三角化、局部重网格化、冻结）与损失项（$\mathcal{L}_{sparse}$、$\mathcal{L}_n$、$\mathcal{L}_{plane}$ 等组合）；
  - 参数 $\tau$ 的敏感性分析（Fig. 7，4 个量级）。
- **充分性与公平性评估**：
  - 实验覆盖两个公开数据集，包含重建、渲染、效率、消融多个维度，较为全面；
  - 所有基线使用真值位姿，对比条件相对公平；
  - 效率对比在同一工作站上进行，控制硬件变量；
  - **局限**：ScanNet++ 仅使用 2 个场景，规模偏小；消融实验仅在 Replica 的 Office1 序列上进行，未在多数据集上验证；与 GOF 的效率对比仅限小范围子集，因 GOF 全局隐式场内存开销过大而无法全场景比较。

## 6. 主要结论与发现

- 在 Replica 数据集上，本方法在**所有序列上均取得最低 Accuracy**（平均 1.34 cm，优于 RTG-SLAM 的 1.41 cm），并取得最佳平均 Accuracy Ratio（99.70%）与 Completion Ratio（85.95%）；
- 渲染质量上，本方法在 Replica 上几乎全部序列取得最优 PSNR/SSIM/LPIPS（平均 PSNR 37.85，SSIM 0.99，LPIPS 0.03），在 ScanNet++ 上也优于 Point-SLAM 与 RTG-SLAM；
- 效率上，映射速度达 **10.34 FPS**（MonoGS 1.48、RTG-SLAM 3.65），峰值内存最低 **2325 MB**（MonoGS 5434、RTG-SLAM 2751）；
- 网格提取仅需 **5.34 秒**，远快于 GOF-MC（444.26 s）与 GOF-PSR（415.27 s），且网格大小仅 3.32 MB，远小于 GOF-MC 的 964.95 MB；
- 消融表明各模块与损失项均有正向贡献，完整模型将 Accuracy 误差从 1.13 cm 降至 0.88 cm，Completion Ratio 从 86.34% 提升至 88.32%；
- 几何约束（$\mathcal{L}_{plane}+\mathcal{L}_n$）能显著提升表面平滑度与保真度；$\tau=0.001$ 为精度与完整性的最佳平衡点。

## 7. 优点

- **方法创新性强**：首次提出直接对高斯面元进行三角化的在线增量网格重建框架，绕开传统隐式场构建与全局后处理，实现渲染与重建的统一；
- **显式网格输出**：直接生成水密三角形网格，便于与下游任务（如 AR、机器人导航）无缝集成；
- **内存与计算高效**：通过动态冻结已优化历史区域，将优化限制在局部窗口，显著降低长序列处理的内存与计算开销；
- **几何约束设计巧妙**：平面拉近损失与法向一致性损失有效引导高斯贴合真实表面，抑制输入噪声；
- **三角化算法高效**：基于八叉树与切平面角度贪心策略，避免稠密体素网格构建，网格提取速度比 GOF 快约 80 倍，网格体积小两个数量级；
- **实验对比全面**：涵盖重建精度、渲染质量、映射效率、网格提取效率与多组消融，对比方法覆盖 TSDF、NeRF-SLAM 与 3DGS-SLAM 三大类。

## 8. 不足与局限

- **依赖深度信息**：方法需要 RGB-D 输入，无法仅从 RGB 图像重建，限制了在纯视觉场景中的应用；
- **无法重建未观测区域**：对未扫描到的区域无法补全，场景完整性受限于传感器覆盖范围；
- **数据集覆盖有限**：ScanNet++ 仅使用 2 个场景，消融实验仅在单一序列上进行，泛化性验证不够充分；
- **算力报告不完整**：仅说明使用单张 RTX 3090，未提供 GPU 数量、训练时长、能耗等细节，可复现性信息有限；
- **与 GOF 的效率对比不完整**：因 GOF 内存限制，仅在 Office0 的小子集上对比，未在全场景范围内验证；
- **实时性仍有提升空间**：10.34 FPS 虽优于基线，但距离严格实时（如 30 FPS）仍有差距；
- **长序列冻结策略的阈值敏感性**：$N_{obs}$ 与 $\epsilon_{gs}$ 的设定对性能有影响，论文未对此进行充分消融分析。

（完）
