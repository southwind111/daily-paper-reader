---
title: "MAPo: Motion-Aware Partitioning of Deformable 3D Gaussian Splatting for High-Fidelity Dynamic Scene Reconstruction"
title_zh: MAPo：面向高保真动态场景重建的运动感知可变形三维高斯泼溅划分
authors: "Jiao, Han, Sun, Jiakai, Xu, Yexing, Zhao, Lei, Xing, Wei, Lin, Huaizhong"
date: 2026
publication_date: 2026
publication_date_precision: year
publication_date_source: conference year only; exact release date unverified
publication_date_kind: unknown
pdf: "https://openaccess.thecvf.com/content/CVPR2026/papers/Jiao_MAPo_Motion-Aware_Partitioning_of_Deformable_3D_Gaussian_Splatting_for_High-Fidelity_CVPR_2026_paper.pdf"
tags: ["query:dr"]
score: 9.0
evidence: 对可变形三维高斯进行运动感知划分以重建动态场景
tldr: 基于形变场的动态高斯重建在高度动态区域常产生模糊渲染并丢失精细运动细节，根源在于单一统一模型难以表征多样运动模式。本文提出运动感知划分的可变形三维高斯泼溅框架MAPo，通过运动感知划分让多个模型分别表征不同运动模式，从而提升重建保真度。实验表明其在高动态区域实现高保真动态场景重建，优于统一形变模型，为动态场景高斯重建提供了更精细的运动建模思路。
source: CVPR-2026-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiao-mapo-motion-aware-partitioning-of-deformable-3d-gaussian-splatting-for-high-fidelity-cvpr-2026-paper/fig-001.webp\", \"caption\": \"\", \"page\": 4, \"index\": 1, \"width\": 1280, \"height\": 960}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiao-mapo-motion-aware-partitioning-of-deformable-3d-gaussian-splatting-for-high-fidelity-cvpr-2026-paper/fig-002.webp\", \"caption\": \"\", \"page\": 5, \"index\": 2, \"width\": 1511, \"height\": 1557}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiao-mapo-motion-aware-partitioning-of-deformable-3d-gaussian-splatting-for-high-fidelity-cvpr-2026-paper/fig-003.webp\", \"caption\": \"\", \"page\": 5, \"index\": 3, \"width\": 1511, \"height\": 1541}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiao-mapo-motion-aware-partitioning-of-deformable-3d-gaussian-splatting-for-high-fidelity-cvpr-2026-paper/fig-004.webp\", \"caption\": \"\", \"page\": 5, \"index\": 4, \"width\": 1511, \"height\": 1554}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiao-mapo-motion-aware-partitioning-of-deformable-3d-gaussian-splatting-for-high-fidelity-cvpr-2026-paper/fig-005.webp\", \"caption\": \"\", \"page\": 5, \"index\": 5, \"width\": 703, \"height\": 716}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiao-mapo-motion-aware-partitioning-of-deformable-3d-gaussian-splatting-for-high-fidelity-cvpr-2026-paper/fig-006.webp\", \"caption\": \"\", \"page\": 6, \"index\": 6, \"width\": 1280, \"height\": 720}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiao-mapo-motion-aware-partitioning-of-deformable-3d-gaussian-splatting-for-high-fidelity-cvpr-2026-paper/fig-007.webp\", \"caption\": \"\", \"page\": 6, \"index\": 7, \"width\": 1280, \"height\": 720}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiao-mapo-motion-aware-partitioning-of-deformable-3d-gaussian-splatting-for-high-fidelity-cvpr-2026-paper/fig-008.webp\", \"caption\": \"\", \"page\": 6, \"index\": 8, \"width\": 1280, \"height\": 720}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiao-mapo-motion-aware-partitioning-of-deformable-3d-gaussian-splatting-for-high-fidelity-cvpr-2026-paper/fig-009.webp\", \"caption\": \"\", \"page\": 6, \"index\": 9, \"width\": 1280, \"height\": 720}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiao-mapo-motion-aware-partitioning-of-deformable-3d-gaussian-splatting-for-high-fidelity-cvpr-2026-paper/fig-010.webp\", \"caption\": \"\", \"page\": 6, \"index\": 10, \"width\": 1280, \"height\": 720}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiao-mapo-motion-aware-partitioning-of-deformable-3d-gaussian-splatting-for-high-fidelity-cvpr-2026-paper/fig-011.webp\", \"caption\": \"\", \"page\": 6, \"index\": 11, \"width\": 1280, \"height\": 720}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiao-mapo-motion-aware-partitioning-of-deformable-3d-gaussian-splatting-for-high-fidelity-cvpr-2026-paper/fig-012.webp\", \"caption\": \"\", \"page\": 6, \"index\": 12, \"width\": 1280, \"height\": 720}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiao-mapo-motion-aware-partitioning-of-deformable-3d-gaussian-splatting-for-high-fidelity-cvpr-2026-paper/fig-013.webp\", \"caption\": \"\", \"page\": 6, \"index\": 13, \"width\": 1280, \"height\": 720}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiao-mapo-motion-aware-partitioning-of-deformable-3d-gaussian-splatting-for-high-fidelity-cvpr-2026-paper/fig-014.webp\", \"caption\": \"\", \"page\": 6, \"index\": 14, \"width\": 1280, \"height\": 720}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiao-mapo-motion-aware-partitioning-of-deformable-3d-gaussian-splatting-for-high-fidelity-cvpr-2026-paper/fig-015.webp\", \"caption\": \"\", \"page\": 6, \"index\": 15, \"width\": 1280, \"height\": 720}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiao-mapo-motion-aware-partitioning-of-deformable-3d-gaussian-splatting-for-high-fidelity-cvpr-2026-paper/fig-016.webp\", \"caption\": \"\", \"page\": 6, \"index\": 16, \"width\": 1280, \"height\": 720}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiao-mapo-motion-aware-partitioning-of-deformable-3d-gaussian-splatting-for-high-fidelity-cvpr-2026-paper/fig-017.webp\", \"caption\": \"\", \"page\": 6, \"index\": 17, \"width\": 1280, \"height\": 720}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiao-mapo-motion-aware-partitioning-of-deformable-3d-gaussian-splatting-for-high-fidelity-cvpr-2026-paper/fig-018.webp\", \"caption\": \"\", \"page\": 6, \"index\": 18, \"width\": 1352, \"height\": 1014}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiao-mapo-motion-aware-partitioning-of-deformable-3d-gaussian-splatting-for-high-fidelity-cvpr-2026-paper/fig-019.webp\", \"caption\": \"\", \"page\": 6, \"index\": 19, \"width\": 1352, \"height\": 1014}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiao-mapo-motion-aware-partitioning-of-deformable-3d-gaussian-splatting-for-high-fidelity-cvpr-2026-paper/fig-020.webp\", \"caption\": \"\", \"page\": 6, \"index\": 20, \"width\": 1352, \"height\": 1014}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiao-mapo-motion-aware-partitioning-of-deformable-3d-gaussian-splatting-for-high-fidelity-cvpr-2026-paper/fig-021.webp\", \"caption\": \"\", \"page\": 6, \"index\": 21, \"width\": 1352, \"height\": 1014}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiao-mapo-motion-aware-partitioning-of-deformable-3d-gaussian-splatting-for-high-fidelity-cvpr-2026-paper/fig-022.webp\", \"caption\": \"\", \"page\": 6, \"index\": 22, \"width\": 1352, \"height\": 1014}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiao-mapo-motion-aware-partitioning-of-deformable-3d-gaussian-splatting-for-high-fidelity-cvpr-2026-paper/fig-023.webp\", \"caption\": \"\", \"page\": 6, \"index\": 23, \"width\": 1352, \"height\": 1014}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiao-mapo-motion-aware-partitioning-of-deformable-3d-gaussian-splatting-for-high-fidelity-cvpr-2026-paper/fig-024.webp\", \"caption\": \"\", \"page\": 6, \"index\": 24, \"width\": 1352, \"height\": 1014}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiao-mapo-motion-aware-partitioning-of-deformable-3d-gaussian-splatting-for-high-fidelity-cvpr-2026-paper/fig-025.webp\", \"caption\": \"\", \"page\": 6, \"index\": 25, \"width\": 1352, \"height\": 1014}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiao-mapo-motion-aware-partitioning-of-deformable-3d-gaussian-splatting-for-high-fidelity-cvpr-2026-paper/fig-026.webp\", \"caption\": \"\", \"page\": 6, \"index\": 26, \"width\": 1352, \"height\": 1014}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiao-mapo-motion-aware-partitioning-of-deformable-3d-gaussian-splatting-for-high-fidelity-cvpr-2026-paper/fig-027.webp\", \"caption\": \"\", \"page\": 6, \"index\": 27, \"width\": 1352, \"height\": 1014}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiao-mapo-motion-aware-partitioning-of-deformable-3d-gaussian-splatting-for-high-fidelity-cvpr-2026-paper/fig-028.webp\", \"caption\": \"\", \"page\": 6, \"index\": 28, \"width\": 1352, \"height\": 1014}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiao-mapo-motion-aware-partitioning-of-deformable-3d-gaussian-splatting-for-high-fidelity-cvpr-2026-paper/fig-029.webp\", \"caption\": \"\", \"page\": 6, \"index\": 29, \"width\": 1352, \"height\": 1014}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiao-mapo-motion-aware-partitioning-of-deformable-3d-gaussian-splatting-for-high-fidelity-cvpr-2026-paper/fig-030.webp\", \"caption\": \"\", \"page\": 6, \"index\": 30, \"width\": 1352, \"height\": 1014}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiao-mapo-motion-aware-partitioning-of-deformable-3d-gaussian-splatting-for-high-fidelity-cvpr-2026-paper/fig-031.webp\", \"caption\": \"\", \"page\": 6, \"index\": 31, \"width\": 1352, \"height\": 1014}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiao-mapo-motion-aware-partitioning-of-deformable-3d-gaussian-splatting-for-high-fidelity-cvpr-2026-paper/fig-032.webp\", \"caption\": \"\", \"page\": 6, \"index\": 32, \"width\": 1352, \"height\": 1014}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiao-mapo-motion-aware-partitioning-of-deformable-3d-gaussian-splatting-for-high-fidelity-cvpr-2026-paper/fig-033.webp\", \"caption\": \"\", \"page\": 6, \"index\": 33, \"width\": 1352, \"height\": 1014}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiao-mapo-motion-aware-partitioning-of-deformable-3d-gaussian-splatting-for-high-fidelity-cvpr-2026-paper/fig-034.webp\", \"caption\": \"\", \"page\": 6, \"index\": 34, \"width\": 1352, \"height\": 1014}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiao-mapo-motion-aware-partitioning-of-deformable-3d-gaussian-splatting-for-high-fidelity-cvpr-2026-paper/fig-035.webp\", \"caption\": \"\", \"page\": 6, \"index\": 35, \"width\": 1352, \"height\": 1014}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiao-mapo-motion-aware-partitioning-of-deformable-3d-gaussian-splatting-for-high-fidelity-cvpr-2026-paper/fig-036.webp\", \"caption\": \"\", \"page\": 7, \"index\": 36, \"width\": 1352, \"height\": 1014}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiao-mapo-motion-aware-partitioning-of-deformable-3d-gaussian-splatting-for-high-fidelity-cvpr-2026-paper/fig-037.webp\", \"caption\": \"\", \"page\": 7, \"index\": 37, \"width\": 1352, \"height\": 1014}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jiao-mapo-motion-aware-partitioning-of-deformable-3d-gaussian-splatting-for-high-fidelity-cvpr-2026-paper/fig-038.webp\", \"caption\": \"\", \"page\": 7, \"index\": 38, \"width\": 1352, \"height\": 1014}]"
motivation: 基于形变场的动态高斯重建在高度动态区域易产生模糊渲染并丢失精细运动细节。
method: 提出MAPo框架，对可变形三维高斯进行运动感知划分，以多个模型表征多样运动模式。
result: 在高动态区域实现高保真动态场景重建，优于统一形变模型。
conclusion: 为动态场景高斯重建提供更精细的运动建模思路。
---

## Abstract
3D Gaussian Splatting, known for enabling high-quality static scene reconstruction with fast rendering, is increasingly being applied to multi-view dynamic scene reconstruction. A common strategy involves learning a deformation field to model the temporal changes of a canonical set of 3D Gaussians. However, these deformation-based methods often produce blurred renderings and lose fine motion details in highly dynamic regions due to the inherent limitations of a single, unified model in representing diverse motion patterns. To address these challenges, we introduce Motion-Aware Partitioning of Deformable 3D Gaussian Splatting (MAPo), a novel framework for high-fidelity dynamic scene reconstruction. Its core is a dynamic score-based partitioning strategy that distinguishes between high- and low-dynamic 3D Gaussians. For high-dynamic 3D Gaussians, we recursively partition them temporally and duplicate their deformation networks for each new temporal segment, enabling specialized modeling to capture intricate motion details. Concurrently, low-dynamic 3DGs are treated as static to reduce computational costs. However, this temporal partitioning strategy for high-dynamic 3DGs can introduce visual discontinuities across frames at the partition boundaries. To address this, we introduce a cross-frame consistency loss, which not only ensures visual continuity but also further enhances rendering quality. Extensive experiments demonstrate that MAPo achieves superior rendering quality compared to baselines while maintaining comparable computational costs, particularly in regions with complex or rapid motions.

---

## 论文详细总结（自动生成）

# MAPo 论文中文总结

## 1. 核心问题与整体含义（研究动机与背景）

- **背景**：3D Gaussian Splatting（3DGS）在静态场景重建中实现实时、照片级渲染，近年被广泛扩展到多视角动态场景重建。主流策略是学习一个**形变场（deformation field）**，将一组规范（canonical）3D 高斯映射到随时间变化的状态。
- **核心问题**：这类基于形变的方法在**高度动态区域**常产生模糊渲染并丢失精细运动细节，根源在于**单一统一模型**难以表征多样化的运动模式。
- **两大固有局限**：
  - **运动建模能力瓶颈**：单一规范 3DGS 集合 + 全局共享形变网络，被迫用一套参数拟合所有冲突运动模式，导致收敛到**时间平均表示（temporal averaging）**，无法准确捕捉突发变化与细粒度时序细节。
  - **冗余计算**：静态区域的 3DGS 仍反复参与形变网络计算，浪费算力、拖慢训练与渲染。
- **整体含义**：论文提出 MAPo，用运动感知的划分策略让多个模型分别负责不同运动模式，同时把低动态高斯视为静态以节省计算，从而在高动态区域实现高保真重建。

## 2. 方法论

### 2.1 核心思想
- 基于每个 3DG 的**动态分数**区分高/低动态高斯：高动态者**递归时序划分**并复制形变网络；低动态者**视为静态**跳过形变计算。引入**跨帧一致性损失**缓解划分边界处的视觉不连续。

### 2.2 关键技术细节与公式

- **动态分数计算**：
  - 记录每个 3DG 的历史位置 $\mu_{ij}$（$m$ 个，文中取 300）。
  - 最大位移：$r_i = \|\max_j \mu_{ij} - \min_j \mu_{ij}\|$（捕捉运动峰值幅度）。
  - 位置方差：$v_i = \sum_{j=1}^{m} \|\mu_{ij} - \bar{\mu}_i\|^2 / m$（衡量围绕均值的离散度）。
  - 两者经**百分位归一化**映射到 $[0,1]$，再用**调和平均**融合，得到动态分数 $S_i = \frac{2}{\frac{1}{\tilde r_i + \varepsilon} + \frac{1}{\tilde v_i + \varepsilon}}$（$\varepsilon=10^{-6}$）。调和平均要求两项都高才输出高，避免单指标偏置（如"短暂高速+长期静止"与"持续小幅振荡"的区分）。

- **基于动态分数的时序划分**：
  - 每个 3DG 维护划分层级 $l$（初始 0）与时间区间 $[t_{start}, t_{end}]$（初始 $[0,T]$）。
  - 当某 3DG 动态分数超过当前层级阈值 $\tau_l$，在**时间中点** $t_{mid}=(t_{start}+t_{end})/2$ 划分：原 3DG 保留前半段并升到 $l+1$，复制出具有相同属性的新 3DG 负责后半段；对应形变网络 $F_{[t_{start},t_{end}]}$ 复制为 $F_{[t_{start},t_{mid}]}$ 与 $F_{[t_{mid},t_{end}]}$，递归进行。
  - 效果：多个网络+对应 3DGs 分别建模不同时间段，缓解"时间平均"效应。

- **静态 3DGS 划分**：
  - 动态分数低于阈值 $\tau_{static}$ 的 3DG 被识别为静态，用其形变网络在随机时间步的输出初始化属性，之后**跳过形变网络计算**（属性仍可优化），显著降低计算成本。

- **跨帧一致性损失 $L_{cross}$**（仅对划分边界 5 帧内的训练视角施加）：
  - $L_{current} = \|I_t(G_t,V) - I_t(G_{t'},V)\|_1$：同一帧在相邻时间段下渲染应一致（边界平滑）。
  - $L_{gt} = \|I_t(G_{t'},V) - I^{GT}\|_1$：相邻段 3DGs 的渲染应与当前帧真值对齐，防止 $L_{current}$ 单独优化导致**过度平滑/模糊**。
  - 总损失：$L_{cross} = 0.5 \cdot L_{current} + L_{gt}$。

### 2.3 算法流程（文字说明）
1. 以 E-D3DGS 的双形变范式为基础（粗/细时间嵌入 + 粗/细形变网络，形变预测相加）。
2. 训练中记录历史位置 → 计算动态分数。
3. 高动态 3DGs 递归时序划分并复制形变网络；低动态 3DGs 转为静态。
4. 静态与动态 3DGs 融合后光栅化渲染。
5. 在边界附近施加 $L_{cross}$ 保证时序平滑与细节保真。

## 3. 实验设计

- **数据集 / 场景**：
  - **N3DV**：30 FPS、20 相机，图像下采样至 1352×1014；较长序列 flame salmon 切成 4 个 10s 片段。
  - **Meet Room**：1280×720、30 FPS、13 相机。
- **评价指标（benchmark）**：PSNR、SSIM、LPIPS，以及存储、训练时间、FPS；额外用 **tOF**（时序一致性，越低越好）评估边界平滑度。
- **对比方法**：DyNeRF、NeRFPlayer、Mix Voxels、K-Planes、HyperReel、D3DGS、4DGS、4DGaussians、Ex4DGS、Swift4D、4DGC、LocalDyGS、E-D3DGS，以及自建的分段基线 **E-D3DGS (seg)**（将序列均分为三段各自训练独立模型）。
- **公平性设置**：所有 3DGS 基线使用相同点云初始化；无公开代码或协议差异大的方法（如 SWinGS、ST-GS）放到附录。
- **消融实验**：
  - 组件渐进消融：基线 → +Max Dis → +Var → +Static → +L_current → +L_gt。
  - 最大划分层级消融（0–4，在 flame salmon frag3 上）。
  - 定性分析：动态划分可视化（Vrheadset）、静态划分可视化（Salmon）、边界不连续可视化（图 8、图 9）。

## 4. 资源与算力

- 文中说明计算成本（训练时间、渲染速度、存储）"calculated on an **NVIDIA RTX A6000** unless otherwise specified"，但**未明确给出 GPU 数量**。
- 训练时长示例：N3DV 上 MAPo 为 **1 小时 52 分**（flame salmon frag1），Meet Room 为 **1 小时 19 分**；对比 E-D3DGS 分别为 2h41m 和 1h36m。
- 表格注脚提到 DyNeRF "was trained on 8 GPUs"（属于对比方法的算力信息，非本文方法）。
- 总体：**GPU 型号有说明，具体卡数与总机时未充分披露**。

## 5. 实验数量与充分性

- **实验规模**：2 个真实数据集（N3DV、Meet Room）× 13+ 个对比方法；1 组组件渐进消融；1 组划分层级消融（5 档）；多组定性可视化（动态/静态划分、边界不连续、帧序列）。
- **充分性**：
  - 覆盖了渲染质量、存储、训练时间、FPS 与 tOF 时序一致性，维度较全。
  - 消融**逐组件递增**，能清晰定位各模块贡献。
  - 引入 E-D3DGS (seg) 作为朴素分段基线，凸显动态分数引导划分优于固定窗口切分。
- **客观/公平性**：
  - 统一点云初始化，指标在相同硬件测量，较为公平。
  - 部分强基线（SWinGS、ST-GS）因无公开代码或协议差异被放到附录，正文未直接对比，存在一定的对比覆盖缺口。
  - tOF 等指标为论文自报，未见多随机种子/方差统计。

## 6. 主要结论与发现

- MAPo 在 **N3DV**（PSNR 31.33 / SSIM 0.944 / LPIPS 0.044）与 **Meet Room**（PSNR 26.72 / SSIM 0.903 / LPIPS 0.066）上均取得 **SOTA 渲染质量**，同时保持可比的计算成本。
- 在**复杂或快速运动区域**（如快速移动的手、细节丰富的面部表情、快速移动的喷枪）明显优于基线，显著减少运动模糊、保留精细细节。
- **时序划分**有效缓解"时间平均"效应；**静态划分**在不降低质量的前提下大幅降低训练时间与存储、提升 FPS。
- **跨帧一致性损失**：仅加时序划分会使边界 tOF 显著升高（视觉不连续）；逐步加入 $L_{current}$、$L_{gt}$ 后边界 tOF 被压到基线水平以下，且 $L_{gt}$ 还能带来额外质量增益（避免过平滑）。
- **最大划分层级**：从 0→4 质量总体提升，但**层级 3 后收益递减**，故主实验取 3；成本增长可控（层级 4 存储仅约为层级 0 的两倍）。

## 7. 优点（亮点）

- **细粒度、per-3DG 级别的划分**：不同于窗口级（如 SWinGS）粗划分，划分直接由 3D 运动引导而非 2D 光流先验，且集成在**单一端到端训练框架**中，避免繁琐的前/后处理。
- **双指标动态分数设计**：最大位移 + 位置方差，调和平均融合，能区分不同类型的运动行为，设计有洞察力。
- **"动态建模增强 + 静态计算节省"双管齐下**：既提升高动态区域质量，又通过静态化降低计算与存储，兼顾质量与效率。
- **一致性损失的双重约束**：$L_{current}$ 保证段间自洽，$L_{gt}$ 用真值锚定防止过平滑，二者互补，并用 tOF 定量验证。
- **实验验证较扎实**：多数据集、多基线、渐进式消融、层级敏感性分析、定性可视化齐全。

## 8. 不足与局限

- **算力信息披露不足**：仅给出 GPU 型号（RTX A6000），未说明 GPU 数量、总训练机时，复现成本难以精确评估。
- **对比覆盖缺口**：SWinGS、ST-GS 等强相关方法未在正文直接对比（推至附录），削弱了"全面 SOTA"的说服力。
- **超参数敏感性**：动态分数阈值 $\tau_l$、$\tau_{static}$、最大划分层级、记录位置数 $m$、边界 5 帧窗口等均需人工设定，论文未充分讨论阈值选取对质量/成本的影响与鲁棒性。
- **边界依赖一致性损失**：划分天然引入边界不连续，需额外损失修补；损失只在边界附近 5 帧生效，极端快速运动下窗口是否足够未验证。
- **场景与规模限制**：仅在 N3DV、Meet Room 两个多视角室内数据集验证，未涉及大规模户外、单目、长时间流式等场景；per-frame 训练类方法的在线重建能力也不是本文目标。
- **统计严谨性**：未见多次随机种子/误差棒报告，LPIPS 等指标的微小差异（如 0.044 vs 0.049）显著性未讨论。
- **偏差风险**：tOF、可视化均来自作者自评，缺少第三方复现；"动态分数"启发式指标的普适性尚待更多场景检验。

（完）
