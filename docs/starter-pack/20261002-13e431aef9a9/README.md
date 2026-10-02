<div class="dpr-topic-result-actions"><button type="button" data-topic-copy="docs/starter-pack/20261002-13e431aef9a9/papers.md">复制论文清单</button> <a href="docs/starter-pack/20261002-13e431aef9a9/papers.md" download data-no-router>下载 Markdown</a> <a href="docs/starter-pack/20261002-13e431aef9a9/papers.json" download data-no-router>下载 JSON</a> <button type="button" data-topic-continue="20261002-13e431aef9a9">继续生成阅读内容</button></div>

# d-world · 入门导读

> 本导读基于所列论文的标题、摘要和已有速览，不代表已阅读全部全文。近期窗口不是完整领域史；检索不保证覆盖全部相关论文。模型导读需结合原文核验。

检索窗口：arXiv &#91;2025-10-02, 2026-10-02&#41;；会议 &#91;2024-10-02, 2026-10-02&#41;（UTC，结束日不含）

## 方向概览

本导读围绕3D视觉与世界模型（World Models）的交叉方向，覆盖近期检索窗口内的论文。核心研究问题包括：如何学习可预测环境动态的内部模型以支持规划与决策；如何在3D空间中构建可探索、可控制、物理一致的世界表示；以及如何将世界模型与强化学习、机器人操作、自动驾驶等下游任务耦合。输入论文显示，当前研究可大致分为几个子方向：面向决策的世界模型（含模型基强化学习与规划）、3D场景生成与重建型世界模型、面向具身智能与机器人操作的世界-动作模型、自动驾驶中的占用与视频世界模型、以及评测与综述。证据主要来自标题与摘要，部分论文缺少TLDR，导读不补写未提供的经典文献、实验数字或外部链接。

依据：A Comprehensive Survey on World Models for Embodied AI；World Action Models: The Next Frontier in Embodied AI；A Step Toward World Models: A Survey on Robotic Manipulation；World-Action Models for Robot Learning and Control: A Survey；World Models for Embodied Intelligence: From Plausible to Controllable to Actionable；HaM-World: Soft-Hamiltonian World Models with Selective Memory for Planning；Parallel Stochastic Gradient-Based Planning for World Models；Optimistic World Models: Efficient Exploration in Model-Based Deep Reinforcement Learning；OrbiSim: World Models as Differentiable Physics Engines for Embodied Intelligence；ABot-3DWorld 0: A Universal World Model to Explore Any 3D Space；3D-Belief: Embodied Belief Inference via Generative 3D World Modeling；Semi-Supervised Vision-Centric 3D Occupancy World Model for Autonomous Driving；GaussianWorld: Gaussian World Model for Streaming 3D Occupancy Prediction；Future Dynamic 3D Reconstruction: Toward 3D World Modeling with Disentangled Ego-Motion

## 世界模型与模型基强化学习：规划、探索与策略优化

该子方向关注如何用学习到的世界模型支持决策。输入论文覆盖了规划算法、探索机制、策略优化与理论分析。例如，HaM-World提出软哈密顿世界模型与选择性记忆以稳定长时程规划；GRASP利用可微世界模型进行并行随机梯度规划；Optimistic World Models将乐观探索引入模型学习；Q-Learning With World Models在Q学习之上利用世界模型进行测试时搜索；World Models as an Intermediary between Agents and the Real World则从高成本交互域出发论证世界模型作为中介的必要性。此外，Representation World Model、Hierarchical Planning with Latent World Models、Reinforced Planning with Latent World Models、FlexiWorld等探索在表示空间或潜空间中直接规划。该方向论文普遍强调长时程稳定性、样本效率与模型偏差问题，但各方法的具体实验设置与基准不同，需结合原文判断适用性。

依据：HaM-World: Soft-Hamiltonian World Models with Selective Memory for Planning；Parallel Stochastic Gradient-Based Planning for World Models；Optimistic World Models: Efficient Exploration in Model-Based Deep Reinforcement Learning；Q-Learning With World Models；World Models as an Intermediary between Agents and the Real World；Representation World Model: Learning States, Transition and Executable Plans in Representation；Hierarchical Planning with Latent World Models；Reinforced Planning with Latent World Models；FlexiWorld: Learning and Planning via Flexible Action Chunks Across Multiple Time Scales；Latent Action World Models for Control with Unlabeled Trajectories；Amortized Low-Rank Adaptation for Model-Based Reinforcement Learning；Inverting the Bellman Equation: From &#36;Q&#36;-Values to World Models；WIMLE: Uncertainty-Aware World Models with IMLE for Sample-Efficient Continuous Control；Deep SPI: Safe Policy Improvement via World Models

## 3D场景生成、重建与可探索世界模型

该子方向聚焦于从图像、文本或视频构建3D世界表示，并支持探索与渲染。ABot-3DWorld 0提出统一空间生成原语，将多模态输入提升为全景与点云，再生成可探索3DGS世界；WorldFlow3D利用流匹配生成无界3D世界；P3Sim结合物理世界模型与几何条件进行感知3D模拟；Future Dynamic 3D Reconstruction提出FR3D，解耦自运动与环境动态以预测未来动态3D表示；3D-Belief将世界建模视为具身信念推断，在3D空间显式表示不确定性。这些工作共同关注几何一致性、长时程稳定性与可控生成，但评测协议与场景域差异较大，部分论文声称的SOTA需结合其基准理解。

依据：ABot-3DWorld 0: A Universal World Model to Explore Any 3D Space；WorldFlow3D: Flowing Through 3D Distributions for Unbounded World Generation；Perceptual 3D Simulation With Physical World Modeling；Future Dynamic 3D Reconstruction: Toward 3D World Modeling with Disentangled Ego-Motion；3D-Belief: Embodied Belief Inference via Generative 3D World Modeling；Geometry-Aware Rotary Position Embedding for Consistent Video World Model；Physical Object Understanding with a Physically Controllable World Model

## 具身智能与机器人操作中的世界-动作模型

该子方向将世界模型与动作生成耦合，形成World-Action Models（WAMs）或世界模型驱动的策略学习。两篇综述（World Action Models: The Next Frontier in Embodied AI；World-Action Models for Robot Learning and Control: A Survey）给出了WAMs的定义、分类与评测概览。具体方法包括：DexWorldModel提出因果潜世界模型与双状态测试时记忆；OrbiSim将世界模型视为可微物理引擎；STORM结合扩散策略、视频世界模型与MCTS；RoboStereo提出双塔4D具身世界模型与统一策略优化；World-Gymnast在动作条件视频世界模型中对VLA策略进行RL微调；WoVR、WMPO、World-VLA-Loop、VLA-MBPO等探索用世界模型后训练VLA策略。该方向的核心挑战包括动作对齐、多视图一致性、长时程误差累积与仿真到现实迁移。

依据：World Action Models: The Next Frontier in Embodied AI；World-Action Models for Robot Learning and Control: A Survey；DexWorldModel: Causal Latent World Modeling towards Automated Learning of Embodied Tasks；OrbiSim: World Models as Differentiable Physics Engines for Embodied Intelligence；STORM: Search-Guided Generative World Models for Robotic Manipulation；RoboStereo: Dual-Tower 4D Embodied World Models for Unified Policy Optimization；World-Gymnast: Training Robots with Reinforcement Learning in a World Model；WoVR: World Models as Reliable Simulators for Post-Training VLA Policies with RL；WMPO: World Model-based Policy Optimization for Vision-Language-Action Models；World-VLA-Loop: Closed-Loop Learning of Video World Model and VLA Policy；Towards Practical World Model-based Reinforcement Learning for Vision-Language-Action Models；Learning Interactive World Model for Object-Centric Reinforcement Learning；Object-Centric World Models for Causality-Aware Reinforcement Learning；Object-Centric World Models Meet Monte Carlo Tree Search；When Object-Centric World Models Meet Policy Learning: From Pixels to Policies, and Where It Breaks；Mixture-of-World Models: Scaling Multi-Task Reinforcement Learning with Modular Latent Dynamics；Learning Massively Multitask World Models for Continuous Control

## 自动驾驶中的世界模型：占用预测、场景生成与规划

该子方向面向自动驾驶，涵盖3D占用预测、未来场景生成与端到端规划。PreWorld提出半监督视觉中心3D占用世界模型；GaussianWorld将占用预测重构为4D占用预测问题，在3D高斯空间分解场景演化；MaskGWM结合视频掩码重建提升驾驶世界模型泛化；WorldRFT、WALT、WorldDrive、LAW等探索潜世界模型与规划的结合；DriveDreamer4D与ReconDreamer利用世界模型增强4D驾驶场景重建。这些工作共同关注时空一致性、几何保真与规划安全性，但多数评测集中在nuScenes、NAVSIM等基准，跨数据集泛化仍需验证。

依据：Semi-Supervised Vision-Centric 3D Occupancy World Model for Autonomous Driving；GaussianWorld: Gaussian World Model for Streaming 3D Occupancy Prediction；MaskGWM: A Generalizable Driving World Model with Video Mask Reconstruction；WorldRFT: Latent World Model Planning with Reinforcement Fine-Tuning for Autonomous Driving；WALT: Learning World-Model-Aligned Latent Trajectories for Autonomous Driving；Bridging Scene Generation and Planning: Driving with World Model via Unifying Vision and Motion Representation；Enhancing End-to-End Autonomous Driving with Latent World Model；DriveDreamer4D: World Models Are Effective Data Machines for 4D Driving Scene Representation；ReconDreamer: Crafting World Models for Driving Scene Reconstruction via Online Restoration；GEM: A Generalizable Ego-Vision Multimodal World Model for Fine-Grained Ego-Motion, Object Dynamics, and Scene Composition Control

## 评测、基准与综述：从视觉保真到任务效用

该子方向关注世界模型的评测协议与领域综述。World-in-World提出闭环世界基准，强调任务成功而非视觉质量，并报告数据缩放规律；What Drives Success in Physical Planning with Joint-Embedding Predictive World Models?系统研究JEPA世界模型的设计选择；Benchmarking World Models for Continual Learning on Compositional Tasks提出组合持续学习基准；Reconstruction or Semantics? What Makes a Latent Space Useful for Robotic World Models比较重建型与语义型潜空间对策略性能的影响。综述方面，A Comprehensive Survey on World Models for Embodied AI提出三轴分类；A Step Toward World Models: A Survey on Robotic Manipulation从能力角度审视世界模型；World Models for Embodied Intelligence: From Plausible to Controllable to Actionable提出能力层级框架。这些工作共同指出：视觉保真度不足以衡量世界模型效用，物理一致性、可控性与闭环任务性能更关键。

依据：World-in-World: World Models in a Closed-Loop World；What Drives Success in Physical Planning with Joint-Embedding Predictive World Models?；Benchmarking World Models for Continual Learning on Compositional Tasks；Reconstruction or Semantics? What Makes a Latent Space Useful for Robotic World Models；A Comprehensive Survey on World Models for Embodied AI；A Step Toward World Models: A Survey on Robotic Manipulation；World Models for Embodied Intelligence: From Plausible to Controllable to Actionable；Research on World Models Is Not Merely Injecting World Knowledge into Specific Tasks；Foundation World Models for Agents that Learn, Verify, and Adapt Reliably Beyond Static Environments

## 建议阅读顺序

以下为建议学习顺序，不是公布时间排序。

1. A Comprehensive Survey on World Models for Embodied AI · 入门
   - 阅读理由：面向具身AI的世界模型综述，提供统一问题定义、三轴分类与评测资源梳理，适合作为入门起点。
   - 公布时间：2025-10-19（日精度）
   - arxiv · 2025-10-19（日精度）：[原文](https://arxiv.org/pdf/2510.16732v3) / [PDF](https://arxiv.org/pdf/2510.16732v3)

2. World Models for Embodied Intelligence: From Plausible to Controllable to Actionable · 入门
   - 阅读理由：提出Plausible-Controllable-Actionable能力层级，帮助建立以行为效用为核心的评价视角。
   - 公布时间：2026-09-15（日精度）
   - arxiv · 2026-09-15（日精度）：[原文](https://arxiv.org/pdf/2609.16697v1)

3. A Step Toward World Models: A Survey on Robotic Manipulation · 入门
   - 阅读理由：从机器人操作角度梳理世界模型的核心能力与挑战，适合理解应用侧需求。
   - 公布时间：2025-10-31（日精度）
   - arxiv · 2025-10-31（日精度）：[原文](https://arxiv.org/pdf/2511.02097v2) / [PDF](https://arxiv.org/pdf/2511.02097v2)

4. World Action Models: The Next Frontier in Embodied AI · 入门
   - 阅读理由：系统定义World Action Models并给出分类，适合理解世界模型与动作生成融合的范式。
   - 公布时间：2026-05-12（日精度）
   - arxiv · 2026-05-12（日精度）：[原文](https://arxiv.org/pdf/2605.12090v1) / [PDF](https://arxiv.org/pdf/2605.12090v1)

5. World-Action Models for Robot Learning and Control: A Survey · 入门
   - 阅读理由：面向机器人学习与控制的世界-动作模型综述，补充架构、数据与评测的系统视角。
   - 公布时间：2026-09-13（日精度）
   - arxiv · 2026-09-13（日精度）：[原文](https://arxiv.org/pdf/2609.16074v1)

6. HaM-World: Soft-Hamiltonian World Models with Selective Memory for Planning · 进阶
   - 阅读理由：提出软哈密顿世界模型与选择性记忆，是长时程规划稳定性的代表性方法，适合作为规划方向进阶阅读。
   - 公布时间：2026-05-07（日精度）
   - arxiv · 2026-05-07（日精度）：[原文](https://arxiv.org/pdf/2605.05951v1) / [PDF](https://arxiv.org/pdf/2605.05951v1)

7. Parallel Stochastic Gradient-Based Planning for World Models · 进阶
   - 阅读理由：提出可并行随机梯度规划器GRASP，展示可微世界模型在长时程控制中的规划优化。
   - 公布时间：2026-01-31（日精度）
   - arxiv · 2026-01-31（日精度）：[原文](https://arxiv.org/pdf/2602.00475v1) / [PDF](https://arxiv.org/pdf/2602.00475v1)

8. Optimistic World Models: Efficient Exploration in Model-Based Deep Reinforcement Learning · 进阶
   - 阅读理由：将乐观探索引入世界模型学习，适合理解稀疏奖励下的探索机制。
   - 公布时间：2026-02-10（日精度）
   - arxiv · 2026-02-10（日精度）：[原文](https://arxiv.org/pdf/2602.10044v1) / [PDF](https://arxiv.org/pdf/2602.10044v1)

9. Q-Learning With World Models · 进阶
   - 阅读理由：在Q学习之上利用世界模型进行测试时搜索，连接模型基与无模型方法。
   - 公布时间：2026-08-17（日精度）
   - arxiv · 2026-08-17（日精度）：[原文](https://arxiv.org/pdf/2608.17163v1)

10. ABot-3DWorld 0: A Universal World Model to Explore Any 3D Space · 进阶
   - 阅读理由：提出统一空间生成原语与可探索3D世界生成管线，是3D生成与世界模型结合的代表工作。
   - 公布时间：2026-07-13（日精度）
   - arxiv · 2026-07-13（日精度）：[原文](https://arxiv.org/pdf/2607.11673v2) / [PDF](https://arxiv.org/pdf/2607.11673v2)

11. 3D-Belief: Embodied Belief Inference via Generative 3D World Modeling · 进阶
   - 阅读理由：将世界建模视为3D空间中的具身信念推断，强调不确定性与部分可观测性。
   - 公布时间：2026-05-12（日精度）
   - arxiv · 2026-05-12（日精度）：[原文](https://arxiv.org/pdf/2605.11367v2) / [PDF](https://arxiv.org/pdf/2605.11367v2)

12. Future Dynamic 3D Reconstruction: Toward 3D World Modeling with Disentangled Ego-Motion · 进阶
   - 阅读理由：提出FR3D解耦自运动与环境动态，面向未来动态3D重建，适合理解3D世界模型中的几何一致性。
   - 公布时间：2026-06-16（日精度）
   - arxiv · 2026-06-16（日精度）：[原文](https://arxiv.org/pdf/2606.18250v2) / [PDF](https://arxiv.org/pdf/2606.18250v2)

13. DexWorldModel: Causal Latent World Modeling towards Automated Learning of Embodied Tasks · 进阶
   - 阅读理由：提出因果潜世界模型与测试时记忆，面向机器人操作的域泛化与长时程任务。
   - 公布时间：2026-04-13（日精度）
   - arxiv · 2026-04-13（日精度）：[原文](https://arxiv.org/pdf/2604.16484v1) / [PDF](https://arxiv.org/pdf/2604.16484v1)

14. OrbiSim: World Models as Differentiable Physics Engines for Embodied Intelligence · 进阶
   - 阅读理由：将世界模型实现为可微物理引擎，连接结构化场景、神经动力学与强化学习。
   - 公布时间：2026-05-12（日精度）
   - arxiv · 2026-05-12（日精度）：[原文](https://arxiv.org/pdf/2605.16395v1) / [PDF](https://arxiv.org/pdf/2605.16395v1)

15. STORM: Search-Guided Generative World Models for Robotic Manipulation · 进阶
   - 阅读理由：结合扩散策略、视频世界模型与MCTS，展示搜索引导的生成式世界模型用于操作。
   - 公布时间：2025-12-20（日精度）
   - arxiv · 2025-12-20（日精度）：[原文](https://arxiv.org/pdf/2512.18477v1) / [PDF](https://arxiv.org/pdf/2512.18477v1)

16. World-Gymnast: Training Robots with Reinforcement Learning in a World Model · 进阶
   - 阅读理由：在动作条件视频世界模型中对VLA策略做RL微调，展示世界模型作为机器人训练环境的潜力。
   - 公布时间：2026-02-02（日精度）
   - arxiv · 2026-02-02（日精度）：[原文](https://arxiv.org/pdf/2602.02454v1) / [PDF](https://arxiv.org/pdf/2602.02454v1)

17. Semi-Supervised Vision-Centric 3D Occupancy World Model for Autonomous Driving · 进阶
   - 阅读理由：半监督视觉中心3D占用世界模型，适合理解自动驾驶中占用预测与未来预测的结合。
   - 公布时间：2025（年精度）
   - ICLR-2025-Accepted · 2025（年精度）：[官方论文集](https://proceedings.iclr.cc/paper_files/paper/2025/hash/9c979c7a7bcc6a791c3b492697f97e1e-Abstract-Conference.html) / [原文](https://openreview.net/forum?id=rCX9l4OTCT)

18. GaussianWorld: Gaussian World Model for Streaming 3D Occupancy Prediction · 进阶
   - 阅读理由：在高斯空间分解场景演化进行4D占用预测，是自动驾驶世界模型的代表性设计。
   - 公布时间：2025（年精度）
   - CVPR-2025-Accepted · 2025（年精度）：[原文](https://openaccess.thecvf.com/content/CVPR2025/html/Zuo_GaussianWorld_Gaussian_World_Model_for_Streaming_3D_Occupancy_Prediction_CVPR_2025_paper.html)

19. World-in-World: World Models in a Closed-Loop World · 专题
   - 阅读理由：提出闭环世界基准，强调任务成功与可控性，适合理解世界模型评测的范式转变。
   - 公布时间：2025-10-20（日精度）
   - ICLR-2026-Accepted · 2026（年精度）：[官方论文集](https://proceedings.iclr.cc/paper_files/paper/2026/hash/5b4263be85820683d78675cc18d2efc7-Abstract-Conference.html) / [原文](https://openreview.net/forum?id=yDmb7xAfeb)
   - arxiv · 2025-10-20（日精度）：[原文](https://arxiv.org/pdf/2510.18135v2) / [PDF](https://arxiv.org/pdf/2510.18135v2)

20. What Drives Success in Physical Planning with Joint-Embedding Predictive World Models? · 专题
   - 阅读理由：系统研究JEPA世界模型的设计选择与规划成功因素，适合深入潜空间规划专题。
   - 公布时间：2025-12-30（日精度）
   - arxiv · 2025-12-30（日精度）：[原文](https://arxiv.org/pdf/2512.24497v4) / [PDF](https://arxiv.org/pdf/2512.24497v4)

任务：研究方向大礼包

固定窗口：arXiv &#91;2025-10-02, 2026-10-02&#41;；会议 &#91;2024-10-02, 2026-10-02&#41;（UTC，结束日不含）

本次候选评审上限 300，最终名单上限 100；本轮内容预算 10。

覆盖限制：仅检索配置范围内已有库存与预算内候选；向量/会议Top-k召回并非全库遍历，不保证找全相关论文。未核实录用、日期边界和缺失库存不能当作已覆盖。

缺失库存：eccv 2025。

研究需求：帮我查找3dv、世界模型的论文

# d-world

以下为本次固定最终名单，按相关性评分降序；不代表全部相关论文。

1. [World Action Models: The Next Frontier in Embodied AI](https://arxiv.org/abs/2605.12090v1) · 分数 10
2. [HaM-World: Soft-Hamiltonian World Models with Selective Memory for Planning](https://arxiv.org/abs/2605.05951v1) · 分数 10
3. [ABot-3DWorld 0: A Universal World Model to Explore Any 3D Space](https://arxiv.org/abs/2607.11673v2) · 分数 9
4. [DexWorldModel: Causal Latent World Modeling towards Automated Learning of Embodied Tasks](https://arxiv.org/abs/2604.16484v1) · 分数 9
5. [A Comprehensive Survey on World Models for Embodied AI](https://arxiv.org/abs/2510.16732v3) · 分数 9
6. [Semi-Supervised Vision-Centric 3D Occupancy World Model for Autonomous Driving](https://proceedings.iclr.cc/paper_files/paper/2025/hash/9c979c7a7bcc6a791c3b492697f97e1e-Abstract-Conference.html) · 分数 9
7. [3D-Belief: Embodied Belief Inference via Generative 3D World Modeling](https://arxiv.org/abs/2605.11367v2) · 分数 9
8. [Physically Native World Models: A Hamiltonian Perspective on Generative World Modeling](https://arxiv.org/abs/2605.00412v3) · 分数 9
9. [OrbiSim: World Models as Differentiable Physics Engines for Embodied Intelligence](https://arxiv.org/abs/2605.16395v1) · 分数 9
10. [Future Dynamic 3D Reconstruction: Toward 3D World Modeling with Disentangled Ego-Motion](https://arxiv.org/abs/2606.18250v2) · 分数 9
11. [GaussianWorld: Gaussian World Model for Streaming 3D Occupancy Prediction](https://openaccess.thecvf.com/content/CVPR2025/html/Zuo_GaussianWorld_Gaussian_World_Model_for_Streaming_3D_Occupancy_Prediction_CVPR_2025_paper.html) · 分数 9
12. [MVISTA-4D: View-Consistent 4D World Model with Test-Time Action Inference for Robotic Manipulation](https://arxiv.org/abs/2602.09878v2) · 分数 9
13. [Object-Centric World Models for Causality-Aware Reinforcement Learning](https://arxiv.org/abs/2511.14262v3) · 分数 9
14. [RoDyn: Taming Interactive Robot-Dynamic 2.5D World Model for Robotic Manipulation](https://arxiv.org/abs/2510.09036v2) · 分数 9
15. [Nano World Models: A Minimalist Implementation of Future Video Prediction](https://arxiv.org/abs/2605.23993v2) · 分数 9
16. [Learning Interactive World Model for Object-Centric Reinforcement Learning](https://arxiv.org/abs/2511.02225v1) · 分数 9
17. [GEM: A Generalizable Ego-Vision Multimodal World Model for Fine-Grained Ego-Motion, Object Dynamics, and Scene Composition Control](https://openaccess.thecvf.com/content/CVPR2025/html/Hassan_GEM_A_Generalizable_Ego-Vision_Multimodal_World_Model_for_Fine-Grained_Ego-Motion_CVPR_2025_paper.html) · 分数 9
18. [A Step Toward World Models: A Survey on Robotic Manipulation](https://arxiv.org/abs/2511.02097v2) · 分数 9
19. [Parallel Stochastic Gradient-Based Planning for World Models](https://arxiv.org/abs/2602.00475v1) · 分数 9
20. [WorldCompass: Reinforcement Learning for Long-Horizon World Models](https://arxiv.org/abs/2602.09022v1) · 分数 9
21. [Optimistic World Models: Efficient Exploration in Model-Based Deep Reinforcement Learning](https://arxiv.org/abs/2602.10044v1) · 分数 9
22. [Representation World Model: Learning States, Transition and Executable Plans in Representation](https://arxiv.org/abs/2609.29171v1) · 分数 9
23. [Q-Learning With World Models](https://arxiv.org/abs/2608.17163v1) · 分数 9
24. [WorldRFT: Latent World Model Planning with Reinforcement Fine-Tuning for Autonomous Driving](https://arxiv.org/abs/2512.19133v1) · 分数 9
25. [Neural Motion Simulator Pushing the Limit of World Models in Reinforcement Learning](https://openaccess.thecvf.com/content/CVPR2025/html/Hao_Neural_Motion_Simulator_Pushing_the_Limit_of_World_Models_in_CVPR_2025_paper.html) · 分数 9
26. [STORM: Search-Guided Generative World Models for Robotic Manipulation](https://arxiv.org/abs/2512.18477v1) · 分数 9
27. [RoboStereo: Dual-Tower 4D Embodied World Models for Unified Policy Optimization](https://arxiv.org/abs/2603.12639v2) · 分数 9
28. [MaskGWM: A Generalizable Driving World Model with Video Mask Reconstruction](https://openaccess.thecvf.com/content/CVPR2025/html/Ni_MaskGWM_A_Generalizable_Driving_World_Model_with_Video_Mask_Reconstruction_CVPR_2025_paper.html) · 分数 9
29. [World-in-World: World Models in a Closed-Loop World](https://arxiv.org/abs/2510.18135v2) · 分数 9
30. [Physical Object Understanding with a Physically Controllable World Model](https://arxiv.org/abs/2606.00439v1) · 分数 9
31. [ReWorld: Multi-Dimensional Reward Modeling for Embodied World Models](https://arxiv.org/abs/2601.12428v1) · 分数 9
32. [Object-Centric World Models Meet Monte Carlo Tree Search](https://arxiv.org/abs/2601.06604v1) · 分数 9
33. [GrndCtrl: Grounding World Models via Self-Supervised Reward Alignment](https://arxiv.org/abs/2512.01952v2) · 分数 9
34. [World Models as an Intermediary between Agents and the Real World](https://arxiv.org/abs/2602.00785v1) · 分数 9
35. [Learning Implicit Causal World Models from Multi-Agent Demonstrations](https://arxiv.org/abs/2607.26336v1) · 分数 9
36. [World models of environment, agent and joint agent-environment systems](https://arxiv.org/abs/2608.20401v1) · 分数 9
37. [MA-JEPA: Joint-Embedding World Models for Multi-Agent Reinforcement Learning](https://arxiv.org/abs/2609.33563v1) · 分数 9
38. [World Models for Embodied Intelligence: From Plausible to Controllable to Actionable](https://arxiv.org/abs/2609.16697v1) · 分数 9
39. [Latent Action World Models for Control with Unlabeled Trajectories](https://arxiv.org/abs/2512.10016v1) · 分数 9
40. [Amortized Low-Rank Adaptation for Model-Based Reinforcement Learning](https://arxiv.org/abs/2609.12278v1) · 分数 9
41. [Geometry-Aware Rotary Position Embedding for Consistent Video World Model](https://arxiv.org/abs/2602.07854v3) · 分数 9
42. [From Observations to Events: Event-Aware World Model for Reinforcement Learning](https://arxiv.org/abs/2601.19336v1) · 分数 9
43. [WorldFlow3D: Flowing Through 3D Distributions for Unbounded World Generation](https://arxiv.org/abs/2603.29089v1) · 分数 9
44. [Discrete Codebook World Models for Continuous Control](https://proceedings.iclr.cc/paper_files/paper/2025/hash/1dd85d064697ec1a258cd2b8755b8c6d-Abstract-Conference.html) · 分数 9
45. [VisualPredicator: Learning Abstract World Models with Neuro-Symbolic Predicates for Robot Planning](https://proceedings.iclr.cc/paper_files/paper/2025/hash/975db59bfa6eba2175a410f6afcecd99-Abstract-Conference.html) · 分数 9
46. [Foundation World Models for Agents that Learn, Verify, and Adapt Reliably Beyond Static Environments](https://arxiv.org/abs/2602.23997v1) · 分数 9
47. [GigaBrain-0.5M&#42;: a VLA That Learns From World Model-Based Reinforcement Learning](https://arxiv.org/abs/2602.12099v2) · 分数 9
48. [Learning Task-Sufficient World Models by Synergizing Agentic Exploration and Structured Modeling](https://arxiv.org/abs/2607.04409v1) · 分数 9
49. [MrCoM: A Meta-Regularized World-Model Generalizing Across Multi-Scenarios](https://arxiv.org/abs/2511.06252v1) · 分数 9
50. [Learning Massively Multitask World Models for Continuous Control](https://arxiv.org/abs/2511.19584v2) · 分数 9
51. [Mixture-of-World Models: Scaling Multi-Task Reinforcement Learning with Modular Latent Dynamics](https://arxiv.org/abs/2602.01270v1) · 分数 9
52. [StrucPhysVideo: Learning Physical Dynamics from Structured Captions and Robot Actions](https://arxiv.org/abs/2609.18430v1) · 分数 9
53. [Bridging Scene Generation and Planning: Driving with World Model via Unifying Vision and Motion Representation](https://arxiv.org/abs/2603.14948v1) · 分数 9
54. [Navigation World Models](https://openaccess.thecvf.com/content/CVPR2025/html/Bar_Navigation_World_Models_CVPR_2025_paper.html) · 分数 9
55. [&#36;ω&#36;-EVA: Envision, Verify, and Act with Latent Interactive World Models](https://arxiv.org/abs/2606.09457v2) · 分数 9
56. [WMPO: World Model-based Policy Optimization for Vision-Language-Action Models](https://arxiv.org/abs/2511.09515v1) · 分数 9
57. [WoVR: World Models as Reliable Simulators for Post-Training VLA Policies with RL](https://arxiv.org/abs/2602.13977v2) · 分数 9
58. [Towards Zero-Shot Task Transfer with Neurosymbolic World Models](https://arxiv.org/abs/2608.17959v2) · 分数 9
59. [World-Action Models for Robot Learning and Control: A Survey](https://arxiv.org/abs/2609.16074v1) · 分数 9
60. [Policy-Guided World Model Planning for Language-Conditioned Visual Navigation](https://arxiv.org/abs/2603.25981v1) · 分数 9
61. [When Object-Centric World Models Meet Policy Learning: From Pixels to Policies, and Where It Breaks](https://arxiv.org/abs/2511.06136v2) · 分数 9
62. [Predicting Consequences and Reinforcing Navigation Policies with Latent World Models](https://arxiv.org/abs/2608.26190v1) · 分数 9
63. [VIDEAS: Distilling Explicit Action Semantics from Demonstration Videos for World Models via Prior-Guided Simulation](https://arxiv.org/abs/2609.33464v1) · 分数 9
64. [Hierarchical Planning with Latent World Models](https://arxiv.org/abs/2604.03208v2) · 分数 9
65. [What Drives Success in Physical Planning with Joint-Embedding Predictive World Models?](https://arxiv.org/abs/2512.24497v4) · 分数 9
66. [Inverting the Bellman Equation: From &#36;Q&#36;-Values to World Models](https://arxiv.org/abs/2606.21173v1) · 分数 9
67. [WALT: Learning World-Model-Aligned Latent Trajectories for Autonomous Driving](https://arxiv.org/abs/2609.30436v1) · 分数 9
68. [Towards Practical World Model-based Reinforcement Learning for Vision-Language-Action Models](https://arxiv.org/abs/2603.20607v1) · 分数 9
69. [World-Gymnast: Training Robots with Reinforcement Learning in a World Model](https://arxiv.org/abs/2602.02454v1) · 分数 9
70. [WOMBET: World Model-Based Experience Transfer for Robust and Sample-efficient Reinforcement Learning](https://arxiv.org/abs/2604.08958v3) · 分数 9
71. [Scaling World-Model Reinforcement Learning Through Diffusion Policy Optimization](https://arxiv.org/abs/2605.26282v1) · 分数 9
72. [Reinforced Planning with Latent World Models](https://arxiv.org/abs/2608.18669v1) · 分数 9
73. [Self-Evolving World Models for LLM Agent Planning](https://arxiv.org/abs/2606.30639v2) · 分数 9
74. [MemWM: Memory-Augmented Text-Based World Model](https://arxiv.org/abs/2608.07107v2) · 分数 9
75. [Self-adapting Robotic Agents through Online Continual Reinforcement Learning with World Model Feedback](https://arxiv.org/abs/2603.04029v1) · 分数 9
76. [Prioritized Rollouts for Efficient World Model-based Vision-Language-Action Policy Optimization](https://arxiv.org/abs/2609.22879v1) · 分数 9
77. [H-WM: Robotic Task and Motion Planning Guided by Hierarchical World Model](https://arxiv.org/abs/2602.11291v2) · 分数 9
78. [Benchmarking World Models for Continual Learning on Compositional Tasks](https://arxiv.org/abs/2609.22055v1) · 分数 9
79. [Enhancing End-to-End Autonomous Driving with Latent World Model](https://proceedings.iclr.cc/paper_files/paper/2025/hash/6aa4967920e495e90aeeaa3acf18d019-Abstract-Conference.html) · 分数 9
80. [RENEW: Towards Learning World Models and Repairing Model Exploitation from Preferences](https://arxiv.org/abs/2607.14180v1) · 分数 9
81. [Reinforcement World Model Learning for LLM-based Agents](https://arxiv.org/abs/2602.05842v2) · 分数 9
82. [From Word to World: Can Large Language Models be Implicit Text-based World Models?](https://arxiv.org/abs/2512.18832v2) · 分数 9
83. [ReconDreamer: Crafting World Models for Driving Scene Reconstruction via Online Restoration](https://openaccess.thecvf.com/content/CVPR2025/html/Ni_ReconDreamer_Crafting_World_Models_for_Driving_Scene_Reconstruction_via_Online_CVPR_2025_paper.html) · 分数 9
84. [Toward Physically Grounded JEPA World Models for Goal-Conditioned Robotic Planning](https://arxiv.org/abs/2609.03565v1) · 分数 9
85. [WIMLE: Uncertainty-Aware World Models with IMLE for Sample-Efficient Continuous Control](https://arxiv.org/abs/2602.14351v2) · 分数 9
86. [Perceptual 3D Simulation With Physical World Modeling](https://arxiv.org/abs/2606.27575v1) · 分数 9
87. [WISE: World-model-guided Imagination Scheduling for Efficient Post-training of Vision-Language-Action Models](https://arxiv.org/abs/2609.03681v1) · 分数 9
88. [Deep SPI: Safe Policy Improvement via World Models](https://arxiv.org/abs/2510.12312v2) · 分数 9
89. [Enhancing Policy Learning with World-Action Model](https://arxiv.org/abs/2603.28955v1) · 分数 9
90. [FlexiWorld: Learning and Planning via Flexible Action Chunks Across Multiple Time Scales](https://arxiv.org/abs/2609.35138v2) · 分数 9
91. [World-VLA-Loop: Closed-Loop Learning of Video World Model and VLA Policy](https://arxiv.org/abs/2602.06508v2) · 分数 9
92. [From World Models to World Action Models: Rethinking Next-State Prediction](https://arxiv.org/abs/2609.34414v1) · 分数 9
93. [Puzzle it Out: Local-to-Global World Model for Offline Multi-Agent Reinforcement Learning](https://arxiv.org/abs/2601.07463v2) · 分数 9
94. [Imagine-then-Plan: Agent Learning from Adaptive Lookahead with World Models](https://arxiv.org/abs/2601.08955v3) · 分数 9
95. [WPT: World-to-Policy Transfer via Online World Model Distillation](https://arxiv.org/abs/2511.20095v2) · 分数 9
96. [Reconstruction or Semantics? What Makes a Latent Space Useful for Robotic World Models](https://arxiv.org/abs/2605.06388v1) · 分数 9
97. [Internalizing World Models via Self-Play Finetuning for Agentic RL](https://arxiv.org/abs/2510.15047v1) · 分数 9
98. [From Pixels to Cooperation Multi Agent Reinforcement Learning based on Multimodal World Models](https://arxiv.org/abs/2511.01310v2) · 分数 9
99. [DriveDreamer4D: World Models Are Effective Data Machines for 4D Driving Scene Representation](https://openaccess.thecvf.com/content/CVPR2025/html/Zhao_DriveDreamer4D_World_Models_Are_Effective_Data_Machines_for_4D_Driving_CVPR_2025_paper.html) · 分数 9
100. [Research on World Models Is Not Merely Injecting World Knowledge into Specific Tasks](https://arxiv.org/abs/2602.01630v1) · 分数 9

[按公布时间查看](#/starter-pack/20261002-13e431aef9a9/dates)

阅读内容：已完成 0，待补充 100。

部分阅读内容生成失败；固定名单及导出保留，可继续生成缺失内容。

基础阅读页导航恢复也未完成，请检查任务日志后续跑；本轮不视为完整成功。
