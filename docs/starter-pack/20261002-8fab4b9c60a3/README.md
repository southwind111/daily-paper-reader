<div class="dpr-topic-result-actions"><button type="button" data-topic-copy="docs/starter-pack/20261002-8fab4b9c60a3/papers.md">复制论文清单</button> <a href="docs/starter-pack/20261002-8fab4b9c60a3/papers.md" download data-no-router>下载 Markdown</a> <a href="docs/starter-pack/20261002-8fab4b9c60a3/papers.json" download data-no-router>下载 JSON</a> <button type="button" data-topic-continue="20261002-8fab4b9c60a3">继续生成阅读内容</button></div>

# spatial-ai · 入门导读

> 本导读基于所列论文的标题、摘要和已有速览，不代表已阅读全部全文。近期窗口不是完整领域史；检索不保证覆盖全部相关论文。模型导读需结合原文核验。

检索窗口：arXiv &#91;2025-10-02, 2026-10-02&#41;；会议 &#91;2024-10-02, 2026-10-02&#41;（UTC，结束日不含）

## 方向概览

本导读围绕“场景理解与空间智能”这一近期检索窗口内的研究问题展开：多模态基础模型（MLLM/VLM）如何从图像、视频、多视角观测中感知3D结构、推断物体间空间关系，并进一步支持具身交互与规划。现有工作大致沿三条主线推进：一是通过大规模空间数据构造与训练（如程序化数据合成、多视角/视频监督、渐进式训练）提升模型的空间感知与推理能力；二是通过工具调用、场景图、认知地图、主动探索等结构化表示与智能体框架，把几何证据显式引入推理过程；三是从评测角度揭示模型在开放世界、退化视觉、跨视角、长时程与具身闭环中的系统性缺陷。整体趋势是从“被动单帧识别”走向“主动、多视角、时序一致、可验证”的空间理解，但当前模型在度量精度、跨视角一致性、动作闭环和泛化性上仍存在显著差距。需要说明：本导读仅依据输入论文的标题与摘要生成，未补写任何外部经典文献、实验数字或领域事实；所有论文均无TLDR字段，因此导读内容完全来自标题与摘要。

依据：[Scaling Spatial Intelligence with Multimodal Foundation Models](/20251002-20261001/2511.13719v4)；[HiSpatial: Taming Hierarchical 3D Spatial Understanding in Vision-Language Models](/20251002-20261001/2603.25411v1)；[From Perception to Action: Spatial AI Agents and World Models](/20251002-20261001/2602.01644v1)；[ChainSpace: A Chained-Reasoning Paradigm for Spatial Intelligence](/20251002-20261001/2608.15788v1)；[From Indoor to Open World: Revealing the Spatial Reasoning Gap in MLLMs](/20251002-20261001/2512.19683v2)；[COOPER: A Unified Model for Cooperative Perception and Reasoning in Spatial Intelligence](/20251002-20261001/2512.04563v2)；[ArchSIBench: Benchmarking the Architectural Spatial Intelligence of Vision-Language Models](/20251002-20261001/2605.20837v1)；[OmniView-Space: Reinforcing Spatial Reasoning via Multi-Perspective Spatial Mapping](/20251002-20261001/2607.00881v1)；[3D CoCa v2: Contrastive Learners with Test-Time Search for Generalizable Spatial Intelligence](/20251002-20261001/2601.06496v1)；[CoCoSI: Collaborative Cognitive Map Construction for Spatial Intelligence](/20251002-20261001/2606.10401v2)；[Imagine in Space: Exploring the Frontier of Spatial Intelligence and Reasoning Efficiency in Vision Language Models](/20251002-20261001/2511.13782v1)；[S-Agent: Spatial Tool-Use Elicits Reasoning for Spatial Intelligence](/20251002-20261001/2606.20515v3)；[SpatialReasoner: Active Perception for Large-Scale 3D Scene Understanding](/20251002-20261001/2512.03284v1)；[SSR: Pushing the Limit of Spatial Intelligence with Structured Scene Reasoning](/20251002-20261001/2603.00409v1)；[Scaling Spatial Reasoning in MLLMs through Programmatic Data Synthesis](/20251002-20261001/2512.16237v1)；[Towards Physics-informed Spatial Intelligence with Human Priors: An Autonomous Driving Pilot Study](/20251002-20261001/2510.21160v1)；[SpatialLadder: Progressive Training for Spatial Reasoning in Vision-Language Models](/20251002-20261001/2510.08531v1)；[Thinking in Structures: Evaluating Spatial Intelligence in Constraint-Governed Spaces](/20251002-20261001/2602.07864v2)；[ESI-Bench: Towards Embodied Spatial Intelligence that Closes the Perception-Action Loop](/20251002-20261001/2605.18746v2)；[Video2Layout: Recall and Reconstruct Metric-Grounded Cognitive Map for Spatial Reasoning](/20251002-20261001/2511.16160v2)

## 空间智能的总体问题与近期综述定位

这一部分给出领域的问题框架与综述性定位。核心问题是：大模型在语义理解上表现强劲，但在3D空间感知、空间关系推断与物理约束下的行动上仍显著不足。相关综述与立场性工作把空间智能拆解为感知、推理、记忆、行动等维度，并指出空间 grounding（几何与物理的度量理解）与符号 grounding（图像与文本关联）需要区分。也有工作从智能体与世界模型角度提出统一分类，强调层次化记忆、GNN-LLM结合与世界模型对长时程空间任务的重要性。这些工作为后续子方向提供了共同术语与问题边界。

依据：[From Perception to Action: Spatial AI Agents and World Models](/20251002-20261001/2602.01644v1)；[Multimodal Spatial Reasoning in the Large Model Era: A Survey and Benchmarks](/20251002-20261001/2510.25760v2)；[Scaling Spatial Intelligence with Multimodal Foundation Models](/20251002-20261001/2511.13719v4)；[Imagine in Space: Exploring the Frontier of Spatial Intelligence and Reasoning Efficiency in Vision Language Models](/20251002-20261001/2511.13782v1)

## 数据构造与训练范式：从模板数据到程序化、自演化监督

这一子方向关注如何为空间智能构造可扩展、可验证的训练数据与训练流程。多条工作指出模板数据虽可扩展但结构僵化，人工标注语言多样但不可扩展且计算不精确；因此转向用模拟器与LLM程序化合成空间问答，把真值生成重构为代码生成与验证任务。另有工作提出渐进式训练（先定位、再多维空间任务、再强化学习）、自演化闭环（proposer与solver协同、难度反馈）、以及以确定性几何环境替代模型共识来避免强化自身几何错误。这些工作共同把“数据质量与可验证性”作为空间智能的核心瓶颈。

依据：[Scaling Spatial Reasoning in MLLMs through Programmatic Data Synthesis](/20251002-20261001/2512.16237v1)；[SpatialLadder: Progressive Training for Spatial Reasoning in Vision-Language Models](/20251002-20261001/2510.08531v1)；[Ouroboros-Spatial: Closing the Data-Model Loop for Spatial Reasoning](/20251002-20261001/2606.11719v2)；[OpenSpatial: A Principled Data Engine for Empowering Spatial Intelligence](/20251002-20261001/2604.07296v2)；[SpatialEvo: Self-Evolving Spatial Intelligence via Deterministic Geometric Environments](/20251002-20261001/2604.14144v1)；[Scaling Spatial Intelligence with Multimodal Foundation Models](/20251002-20261001/2511.13719v4)；[HiSpatial: Taming Hierarchical 3D Spatial Understanding in Vision-Language Models](/20251002-20261001/2603.25411v1)

## 结构化表示与几何先验注入：场景图、认知地图与空间token

这一子方向探索如何把几何结构显式引入模型，而不是仅靠文本或隐式特征。代表思路包括：以3D场景图作为可查询的结构化记忆，通过符号工具提供确定性几何；以认知地图或鸟瞰图重锚定多视角证据；以连续空间token或几何参照表示把3D属性注入语言推理链；以及用双通路几何感知模块在RGB输入下内部化度量与结构先验。这些方法的共同假设是：显式、可验证的结构化表示比纯端到端隐式推理更可靠，但也面临重建噪声与表示对齐的挑战。

依据：[RieMind: Geometry-Grounded Spatial Agent for Scene Understanding](/20251002-20261001/2603.15386v1)；[GraFT: A Training-Free Framework for Spatial Reasoning in Multimodal Large Language Models via 3D Scene Graphs](/20251002-20261001/2609.03892v1)；[CoCoSI: Collaborative Cognitive Map Construction for Spatial Intelligence](/20251002-20261001/2606.10401v2)；[Video2Layout: Recall and Reconstruct Metric-Grounded Cognitive Map for Spatial Reasoning](/20251002-20261001/2511.16160v2)；[Chain of Spatial Thoughts: Modality-Agnostic Spatial Grounding for Vision Language Models](/20251002-20261001/2608.10278v1)；[Boosting MLLM Spatial Reasoning with Geometrically Referenced 3D Scene Representations](/20251002-20261001/2603.08592v2)；[Dual-Pathway Geometry-Aware MLLM for Spatial Intelligence](/20251002-20261001/2605.25334v1)；[Thinking with Geometry: Active Geometry Integration for Spatial Reasoning](/20251002-20261001/2602.06037v5)；[SSR: Pushing the Limit of Spatial Intelligence with Structured Scene Reasoning](/20251002-20261001/2603.00409v1)；[OmniView-Space: Reinforcing Spatial Reasoning via Multi-Perspective Spatial Mapping](/20251002-20261001/2607.00881v1)

## 工具调用与智能体式空间推理：主动感知、程序合成与记忆

这一子方向把空间推理从静态问答扩展为“感知—行动—再感知”的智能体过程。相关工作包括：让VLM作为语义规划者调用空间工具与专家，把2D grounding提升为3D几何证据并聚合为高层空间知识；以程序合成动态生成API解决子问题；以主动感知框架自主调用工具探索大规模3D场景；以及用经验记忆、认知地图和验证器引导的反思实现无参数更新的自演化。核心主张是：主动获取证据、按需检索几何、并在多轮中保持空间状态，比单帧被动推理更接近真实空间智能。

依据：[S-Agent: Spatial Tool-Use Elicits Reasoning for Spatial Intelligence](/20251002-20261001/2606.20515v3)；[Visual Agentic AI for Spatial Reasoning with a Dynamic API](/conference/cvpr-2025/cvpr-2025-marsili-visual-agentic-ai-for-spatial-reasoning-with-a-dynamic-api-cvpr-2025-paper-visual-agentic-ai-for-spatial-reasoning-with-a-dynamic-api)；[SpatialReasoner: Active Perception for Large-Scale 3D Scene Understanding](/20251002-20261001/2512.03284v1)；[Spatial Memory Agent: Experience-Grounded Procedure Memory for Spatial Intelligence](/20251002-20261001/2608.12743v1)；[Perceive, Interact, Reason: Building Tool-Augmented Visual Agents for Spatial Reasoning](/20251002-20261001/2606.12830v1)；[AlloSpatial: Agentic Harness Framework for Spatial Reasoning in Foundation Models](/20251002-20261001/2606.08952v1)；[Active Exploring like a Pigeon: Reinforcing Spatial Reasoning via Agentic Vision-Language Models](/20251002-20261001/2606.02459v1)；[World2Mind: Cognition Toolkit for Allocentric Spatial Reasoning in Foundation Models](/20251002-20261001/2603.09774v1)；[LAST: Leveraging Tools as Hints to Enhance Spatial Reasoning for Multimodal Large Language Models](/20251002-20261001/2604.09712v1)；[Pursuing Minimal Sufficiency in Spatial Reasoning](/20251002-20261001/2510.16688v2)

## 视频、多视角与流式场景理解：时序一致性与长时程空间记忆

这一子方向处理连续视觉输入下的空间理解。问题包括：如何在多帧/多视角间保持几何一致，如何在长时程视频流中维护空间证据，以及如何从碎片化观测中重建全局布局。代表工作涵盖：流式测试时训练与快权重更新、双记忆（工作记忆与情景记忆）、4D场景图与时空token、跨视角对齐与对象级一致性、以及面向第一人称视频流的持续空间推理。共同挑战是上下文长度、视角变化、遮挡与动态物体带来的空间状态漂移。

依据：[Spatial-TTT: Streaming Visual-based Spatial Intelligence with Test-Time Training](/20251002-20261001/2603.12255v1)；[Vision-Language Memory for Spatial Reasoning](/20251002-20261001/2511.20644v2)；[IGGT4D: Streaming 4D Instance-Grounded Geometry Transformer](/20251002-20261001/2607.19228v1)；[SNOW: Spatio-Temporal Scene Understanding with World Knowledge for Open-World Embodied Reasoning](/20251002-20261001/2512.16461v1)；[CrossView Suite: Harnessing Cross-view Spatial Intelligence of MLLMs with Dataset, Model and Benchmark](/20251002-20261001/2605.18621v1)；[Keep It in Mind: User Centric Continual Spatial Intelligence Reasoning in Egocentric Video Streams](/20251002-20261001/2606.15200v1)；[Spatial-IQ: Deconstructing Spatial Intelligence via Hierarchical Capability Tests](/20251002-20261001/2607.22864v1)；[GST-Bench: Can VLMs Develop Global Spatial Awareness from Video?](/20251002-20261001/2608.05747v1)；[OVO-S-Bench: A Hierarchical Benchmark for Streaming Spatial Intelligence in Multimodal LLMs](/20251002-20261001/2606.03890v2)；[SpaceEra++: A Unified Framework Towards 3D Spatial Reasoning in Video](/20251002-20261001/2607.01784v1)

## 评测与诊断：基准、认知层次与失效模式

这一子方向聚焦如何系统评估空间智能。多篇工作批评现有基准过度简化、偏室内、偏静态或可被语言先验短路，因而提出层次化认知框架、约束治理空间、退化视觉、跨视角、4D时空、具身闭环等新基准。诊断结论反复出现：模型在低层感知与高层推理之间存在断裂，依赖语言捷径，跨视角与度量估计薄弱，主动探索优于被动多视角但动作选择常出错，且空间微调模型在分布外基准上泛化有限。这些基准为后续方法提供了可比较的失效画像。

依据：[ArchSIBench: Benchmarking the Architectural Spatial Intelligence of Vision-Language Models](/20251002-20261001/2605.20837v1)；[Thinking in Structures: Evaluating Spatial Intelligence in Constraint-Governed Spaces](/20251002-20261001/2602.07864v2)；[SpaceDG: Benchmarking Spatial Intelligence under Visual Degradation](/20251002-20261001/2605.22536v2)；[Spatial4D-Bench: A Versatile 4D Spatial Intelligence Benchmark](/20251002-20261001/2601.00092v2)；[MMSI-Video-Bench: A Holistic Benchmark for Video-Based Spatial Intelligence](/20251002-20261001/2512.10863v1)；[Spatial-DISE: A Unified Benchmark for Evaluating Spatial Reasoning in Vision-Language Models](/20251002-20261001/2510.13394v4)；[Embodied3DBench: Benchmarking Low-Level Embodied Spatial Intelligence of Vision Language Models](/20251002-20261001/2605.29074v1)；[ESPIRE: A Diagnostic Benchmark for Embodied Spatial Reasoning of Vision-Language Models](/20251002-20261001/2603.13033v1)；[MultihopSpatial: Multi-hop Compositional Spatial Reasoning Benchmark for Vision-Language Model](/20251002-20261001/2603.18892v2)；[Seeing through Imagination: Learning Scene Geometry via Implicit Spatial World Modeling](/20251002-20261001/2512.01821v2)；[SpatialQuery: Benchmarking Geometry-Grounded Multi-Instance Spatial Reasoning in Vision-Language Models](/20251002-20261001/2608.01709v1)；[From Hallucination to Grounding: Diagnosing Visual Spatial Intelligence via CRISP](/20251002-20261001/2606.26535v1)；[Attention in Space: Functional Roles of VLM Heads for Spatial Reasoning](/20251002-20261001/2603.20662v1)；[Reasoning Path and Latent State Analysis for Multi-view Visual Spatial Reasoning: A Cognitive Science Perspective](/20251002-20261001/2512.02340v1)；[Spatial-IQ: Deconstructing Spatial Intelligence via Hierarchical Capability Tests](/20251002-20261001/2607.22864v1)

## 具身空间智能与感知—行动闭环

这一子方向把空间智能放到具身场景中检验：智能体必须决定部署何种能力（感知、移动、操作）并排序，以主动积累任务相关证据。相关工作提出具身空间智能基准、机器人中心低层空间智能评测、导航指令跟随基准，以及从视觉演示中学习程序性上下文并主动选择视角、发出度量命令、根据执行反馈修正的闭环评测。共同发现是：主动探索显著优于被动观测，但动作盲目、过早自信与几何迁移失败是主要瓶颈，且不完美的3D表示可能比2D基线更有害。

依据：[ESI-Bench: Towards Embodied Spatial Intelligence that Closes the Perception-Action Loop](/20251002-20261001/2605.18746v2)；[VABench: Measuring Embodied Spatial Intelligence through Visual Demonstrations, Active Perception, and Metric Control](/20251002-20261001/2609.19554v1)；[Embodied3DBench: Benchmarking Low-Level Embodied Spatial Intelligence of Vision Language Models](/20251002-20261001/2605.29074v1)；[NavSpace: How Navigation Agents Follow Spatial Intelligence Instructions](/20251002-20261001/2510.08173v2)；[ESPIRE: A Diagnostic Benchmark for Embodied Spatial Reasoning of Vision-Language Models](/20251002-20261001/2603.13033v1)；[Active Exploring like a Pigeon: Reinforcing Spatial Reasoning via Agentic Vision-Language Models](/20251002-20261001/2606.02459v1)；[Learning Multi-View Spatial Reasoning from Cross-View Relations](/20251002-20261001/2603.27967v1)

## 模型架构与表示学习：从2D先验到3D几何内部化

这一子方向关注模型内部如何获得空间能力。路线包括：用多视角/视频数据自监督学习几何表示；把深度、相机位姿、点云等3D属性作为监督或辅助任务内部化；以双通路或层次化融合对齐视觉、几何与语言；以及从视频中蒸馏几何知识重塑MLLM潜在空间。核心争论是：额外3D输入与外部编码器是否必要，还是可以通过训练让模型从RGB内部化几何。多篇工作报告了在空间基准上的提升，但摘要未提供统一可比数字，需谨慎解读。

依据：[Learning 3D Representations for Spatial Intelligence from Unposed Multi-View Images](/20251002-20261001/2604.10573v1)；[Learning Geometric Representations from Videos for Spatial Intelligent Multimodal Large Language Models](/20251002-20261001/2606.05833v2)；[SpatialStack: Layered Geometry-Language Fusion for 3D VLM Spatial Reasoning](/20251002-20261001/2603.27437v3)；[EgoMind: Activating Spatial Cognition through Linguistic Reasoning in MLLMs](/20251002-20261001/2604.03318v2)；[Spa3R: Predictive Spatial Field Modeling for 3D Visual Reasoning](/20251002-20261001/2602.21186v2)；[3D CoCa v2: Contrastive Learners with Test-Time Search for Generalizable Spatial Intelligence](/20251002-20261001/2601.06496v1)；[Which Pretraining Paradigm Better Serves Spatial Intelligence? An Empirical Comparison of Vision-Language and Video Generation Models](/20251002-20261001/2605.28132v1)；[SpatioLM: Towards General Physical Spatial Intelligence in Vision-Language Models](/20251002-20261001/2608.01899v1)；[SPARGen: Unifying Spatial Perception and Reasoning through Native Multimodal Generation](/20251002-20261001/2608.14138v1)；[Object-Uni: A Unified Model for Object-Centric Spatial Understanding and Controllable Generation](/20251002-20261001/2608.22757v1)；[SceneScaffold: Active Scene-State Construction for Unified 3D Scene Understanding](/20251002-20261001/2609.33518v1)

## 进展、局限与证据不足说明

进展方面：数据规模与多样性显著提升，出现百万级空间问答与多任务数据集；训练范式从单一监督扩展到渐进式、强化学习与自演化闭环；结构化表示（场景图、认知地图、空间token）与工具调用成为提升空间推理的主流手段；评测从单帧VQA扩展到视频、跨视角、4D、退化视觉与具身闭环。局限方面：模型仍依赖语言先验、度量估计不精确、跨视角一致性弱、长时程空间状态易漂移、主动探索中的动作选择常出错，且空间微调可能损害通用能力或难以泛化到分布外。证据不足说明：输入论文均无TLDR字段，本导读未获得任何论文的TLDR摘要；所有结论仅来自标题与摘要，未补写外部经典文献、未验证代码仓库或链接、未引用摘要之外的实验数字。部分论文摘要提到代码或数据集将公开，但本导读不确认其可用性。

依据：[Scaling Spatial Intelligence with Multimodal Foundation Models](/20251002-20261001/2511.13719v4)；[HiSpatial: Taming Hierarchical 3D Spatial Understanding in Vision-Language Models](/20251002-20261001/2603.25411v1)；[From Indoor to Open World: Revealing the Spatial Reasoning Gap in MLLMs](/20251002-20261001/2512.19683v2)；[ESI-Bench: Towards Embodied Spatial Intelligence that Closes the Perception-Action Loop](/20251002-20261001/2605.18746v2)；[VABench: Measuring Embodied Spatial Intelligence through Visual Demonstrations, Active Perception, and Metric Control](/20251002-20261001/2609.19554v1)；[From Hallucination to Grounding: Diagnosing Visual Spatial Intelligence via CRISP](/20251002-20261001/2606.26535v1)；[On the Generalization Capacities of MLLMs for Spatial Intelligence](/20251002-20261001/2603.06704v1)；[SpaceDG: Benchmarking Spatial Intelligence under Visual Degradation](/20251002-20261001/2605.22536v2)；[OVO-S-Bench: A Hierarchical Benchmark for Streaming Spatial Intelligence in Multimodal LLMs](/20251002-20261001/2606.03890v2)；[GST-Bench: Can VLMs Develop Global Spatial Awareness from Video?](/20251002-20261001/2608.05747v1)

## 建议阅读顺序

以下为建议学习顺序，不是公布时间排序。

1. [From Perception to Action: Spatial AI Agents and World Models](/20251002-20261001/2602.01644v1) · 入门
   - 阅读理由：从智能体与世界模型角度给出统一分类，适合作为进入空间智能领域的总体地图。
   - 公布时间：2026-02-02（日精度）
   - arxiv · 2026-02-02（日精度）：[原文](https://arxiv.org/pdf/2602.01644v1) / [PDF](https://arxiv.org/pdf/2602.01644v1)

2. [Multimodal Spatial Reasoning in the Large Model Era: A Survey and Benchmarks](/20251002-20261001/2510.25760v2) · 入门
   - 阅读理由：综述多模态空间推理任务与基准，帮助建立任务谱系与术语体系。
   - 公布时间：2025-10-29（日精度）
   - arxiv · 2025-10-29（日精度）：[原文](https://arxiv.org/pdf/2510.25760v2) / [PDF](https://arxiv.org/pdf/2510.25760v2)

3. [Scaling Spatial Intelligence with Multimodal Foundation Models](/20251002-20261001/2511.13719v4) · 入门
   - 阅读理由：以大规模数据与多基准评测展示空间智能的当前能力与短板，适合理解问题规模。
   - 公布时间：2025-11-17（日精度）
   - arxiv · 2025-11-17（日精度）：[原文](https://arxiv.org/pdf/2511.13719v4) / [PDF](https://arxiv.org/pdf/2511.13719v4)

4. [Imagine in Space: Exploring the Frontier of Spatial Intelligence and Reasoning Efficiency in Vision Language Models](/20251002-20261001/2511.13782v1) · 入门
   - 阅读理由：从想象与推理效率角度剖析VLM空间推理机制，适合建立对失效模式的直觉。
   - 公布时间：2025-11-16（日精度）
   - arxiv · 2025-11-16（日精度）：[原文](https://arxiv.org/pdf/2511.13782v1) / [PDF](https://arxiv.org/pdf/2511.13782v1)

5. [From Indoor to Open World: Revealing the Spatial Reasoning Gap in MLLMs](/20251002-20261001/2512.19683v2) · 入门
   - 阅读理由：揭示室内到开放世界的空间推理差距，适合理解评测域偏移问题。
   - 公布时间：2025-12-22（日精度）
   - arxiv · 2025-12-22（日精度）：[原文](https://arxiv.org/pdf/2512.19683v2) / [PDF](https://arxiv.org/pdf/2512.19683v2)

6. [ArchSIBench: Benchmarking the Architectural Spatial Intelligence of Vision-Language Models](/20251002-20261001/2605.20837v1) · 入门
   - 阅读理由：建筑空间智能基准，展示从基础空间技能到高层空间认知的评测维度。
   - 公布时间：2026-05-20（日精度）
   - arxiv · 2026-05-20（日精度）：[原文](https://arxiv.org/pdf/2605.20837v1) / [PDF](https://arxiv.org/pdf/2605.20837v1)

7. [Thinking in Structures: Evaluating Spatial Intelligence in Constraint-Governed Spaces](/20251002-20261001/2602.07864v2) · 入门
   - 阅读理由：约束治理空间下的结构中心空间推理基准，说明确定性与歧义对评测的影响。
   - 公布时间：2026-02-08（日精度）
   - arxiv · 2026-02-08（日精度）：[原文](https://arxiv.org/pdf/2602.07864v2) / [PDF](https://arxiv.org/pdf/2602.07864v2)

8. [HiSpatial: Taming Hierarchical 3D Spatial Understanding in Vision-Language Models](/20251002-20261001/2603.25411v1) · 进阶
   - 阅读理由：层次化3D空间理解框架与数据管线，适合作为方法设计的起点。
   - 公布时间：2026-03-26（日精度）
   - arxiv · 2026-03-26（日精度）：[原文](https://arxiv.org/pdf/2603.25411v1) / [PDF](https://arxiv.org/pdf/2603.25411v1)

9. [Scaling Spatial Reasoning in MLLMs through Programmatic Data Synthesis](/20251002-20261001/2512.16237v1) · 进阶
   - 阅读理由：程序化数据合成范式，解决空间推理数据可扩展与可验证的矛盾。
   - 公布时间：2025-12-18（日精度）
   - arxiv · 2025-12-18（日精度）：[原文](https://arxiv.org/pdf/2512.16237v1) / [PDF](https://arxiv.org/pdf/2512.16237v1)

10. [SpatialLadder: Progressive Training for Spatial Reasoning in Vision-Language Models](/20251002-20261001/2510.08531v1) · 进阶
   - 阅读理由：渐进式训练从感知到推理，提供可复用的训练课程设计思路。
   - 公布时间：2025-10-09（日精度）
   - arxiv · 2025-10-09（日精度）：[原文](https://arxiv.org/pdf/2510.08531v1) / [PDF](https://arxiv.org/pdf/2510.08531v1)
   - ICLR-2026-Accepted · 2026（年精度）：[官方论文集](https://proceedings.iclr.cc/paper_files/paper/2026/hash/7bc3fe234454107149fa9d44faacaa64-Abstract-Conference.html) / [原文](https://openreview.net/forum?id=KtrFXlvgrK)

11. [OpenSpatial: A Principled Data Engine for Empowering Spatial Intelligence](/20251002-20261001/2604.07296v2) · 进阶
   - 阅读理由：开源数据引擎与任务层级设计，适合理解空间数据构造的系统工程。
   - 公布时间：2026-04-08（日精度）
   - arxiv · 2026-04-08（日精度）：[原文](https://arxiv.org/pdf/2604.07296v2) / [PDF](https://arxiv.org/pdf/2604.07296v2)
   - ECCV-2026-Accepted-Program · 2026（年精度）：[原文](https://eccv.ecva.net/virtual/2026/poster/4681) / [PDF](https://media.eventhosts.cc/Conferences/ECCV2026/pdfs/6992.pdf)

12. [Ouroboros-Spatial: Closing the Data-Model Loop for Spatial Reasoning](/20251002-20261001/2606.11719v2) · 进阶
   - 阅读理由：自演化数据-模型闭环，展示如何用难度反馈提升数据效率。
   - 公布时间：2026-06-10（日精度）
   - arxiv · 2026-06-10（日精度）：[原文](https://arxiv.org/pdf/2606.11719v2) / [PDF](https://arxiv.org/pdf/2606.11719v2)

13. [RieMind: Geometry-Grounded Spatial Agent for Scene Understanding](/20251002-20261001/2603.15386v1) · 进阶
   - 阅读理由：以3D场景图解耦感知与推理，适合理解结构化表示的优势与边界。
   - 公布时间：2026-03-16（日精度）
   - arxiv · 2026-03-16（日精度）：[原文](https://arxiv.org/pdf/2603.15386v1) / [PDF](https://arxiv.org/pdf/2603.15386v1)

14. [GraFT: A Training-Free Framework for Spatial Reasoning in Multimodal Large Language Models via 3D Scene Graphs](/20251002-20261001/2609.03892v1) · 进阶
   - 阅读理由：训练免费框架用3D场景图提供几何、鸟瞰布局与属性 grounding，实用性强。
   - 公布时间：2026-09-03（日精度）
   - arxiv · 2026-09-03（日精度）：[原文](https://arxiv.org/pdf/2609.03892v1)

15. [CoCoSI: Collaborative Cognitive Map Construction for Spatial Intelligence](/20251002-20261001/2606.10401v2) · 进阶
   - 阅读理由：多智能体协同构建认知地图，展示无训练、模型无关的空间记忆方案。
   - 公布时间：2026-06-09（日精度）
   - arxiv · 2026-06-09（日精度）：[原文](https://arxiv.org/pdf/2606.10401v2) / [PDF](https://arxiv.org/pdf/2606.10401v2)

16. [S-Agent: Spatial Tool-Use Elicits Reasoning for Spatial Intelligence](/20251002-20261001/2606.20515v3) · 进阶
   - 阅读理由：空间工具使用智能体范式，连接感知、工具与多轮推理。
   - 公布时间：2026-06-18（日精度）
   - arxiv · 2026-06-18（日精度）：[原文](https://arxiv.org/pdf/2606.20515v3) / [PDF](https://arxiv.org/pdf/2606.20515v3)

17. [SpatialReasoner: Active Perception for Large-Scale 3D Scene Understanding](/20251002-20261001/2512.03284v1) · 进阶
   - 阅读理由：主动感知框架面向大规模3D场景，展示工具调用与强化学习结合。
   - 公布时间：2025-12-02（日精度）
   - arxiv · 2025-12-02（日精度）：[原文](https://arxiv.org/pdf/2512.03284v1) / [PDF](https://arxiv.org/pdf/2512.03284v1)

18. [Spatial-TTT: Streaming Visual-based Spatial Intelligence with Test-Time Training](/20251002-20261001/2603.12255v1) · 专题
   - 阅读理由：流式视频空间智能与测试时训练，适合理解长时程空间记忆。
   - 公布时间：2026-03-12（日精度）
   - arxiv · 2026-03-12（日精度）：[原文](https://arxiv.org/pdf/2603.12255v1) / [PDF](https://arxiv.org/pdf/2603.12255v1)
   - ECCV-2026-Accepted-Program · 2026（年精度）：[原文](https://eccv.ecva.net/virtual/2026/poster/5426) / [PDF](https://media.eventhosts.cc/Conferences/ECCV2026/pdfs/10554.pdf)

19. [ESI-Bench: Towards Embodied Spatial Intelligence that Closes the Perception-Action Loop](/20251002-20261001/2605.18746v2) · 专题
   - 阅读理由：具身空间智能基准强调感知—行动闭环，适合研究主动探索与动作盲目问题。
   - 公布时间：2026-05-18（日精度）
   - arxiv · 2026-05-18（日精度）：[原文](https://arxiv.org/pdf/2605.18746v2) / [PDF](https://arxiv.org/pdf/2605.18746v2)

20. [VABench: Measuring Embodied Spatial Intelligence through Visual Demonstrations, Active Perception, and Metric Control](/20251002-20261001/2609.19554v1) · 专题
   - 阅读理由：从视觉演示到主动感知与度量控制的闭环评测，适合深入具身空间智能前沿。
   - 公布时间：2026-09-17（日精度）
   - arxiv · 2026-09-17（日精度）：[原文](https://arxiv.org/pdf/2609.19554v1)

任务：研究方向大礼包

固定窗口：arXiv &#91;2025-10-02, 2026-10-02&#41;；会议 &#91;2024-10-02, 2026-10-02&#41;（UTC，结束日不含）

本次候选评审上限 300，最终名单上限 100；本轮内容预算 10。

覆盖限制：仅检索配置范围内已有库存与预算内候选；向量/会议Top-k召回并非全库遍历，不保证找全相关论文。未核实录用、日期边界和缺失库存不能当作已覆盖。

缺失库存：eccv 2025。

研究需求：帮我查找场景理解、空间智能的论文

# spatial-ai

以下为本次固定最终名单，按相关性评分降序；不代表全部相关论文。

1. [Scaling Spatial Intelligence with Multimodal Foundation Models](https://arxiv.org/abs/2511.13719v4) · 分数 10
2. [HiSpatial: Taming Hierarchical 3D Spatial Understanding in Vision-Language Models](https://arxiv.org/abs/2603.25411v1) · 分数 9
3. [From Perception to Action: Spatial AI Agents and World Models](https://arxiv.org/abs/2602.01644v1) · 分数 9
4. [ChainSpace: A Chained-Reasoning Paradigm for Spatial Intelligence](https://arxiv.org/abs/2608.15788v1) · 分数 9
5. [From Indoor to Open World: Revealing the Spatial Reasoning Gap in MLLMs](https://arxiv.org/abs/2512.19683v2) · 分数 9
6. [COOPER: A Unified Model for Cooperative Perception and Reasoning in Spatial Intelligence](https://arxiv.org/abs/2512.04563v2) · 分数 9
7. [ArchSIBench: Benchmarking the Architectural Spatial Intelligence of Vision-Language Models](https://arxiv.org/abs/2605.20837v1) · 分数 9
8. [OmniView-Space: Reinforcing Spatial Reasoning via Multi-Perspective Spatial Mapping](https://arxiv.org/abs/2607.00881v1) · 分数 9
9. [3D CoCa v2: Contrastive Learners with Test-Time Search for Generalizable Spatial Intelligence](https://arxiv.org/abs/2601.06496v1) · 分数 9
10. [CoCoSI: Collaborative Cognitive Map Construction for Spatial Intelligence](https://arxiv.org/abs/2606.10401v2) · 分数 9
11. [Imagine in Space: Exploring the Frontier of Spatial Intelligence and Reasoning Efficiency in Vision Language Models](https://arxiv.org/abs/2511.13782v1) · 分数 9
12. [S-Agent: Spatial Tool-Use Elicits Reasoning for Spatial Intelligence](https://arxiv.org/abs/2606.20515v3) · 分数 9
13. [SpatialReasoner: Active Perception for Large-Scale 3D Scene Understanding](https://arxiv.org/abs/2512.03284v1) · 分数 9
14. [SSR: Pushing the Limit of Spatial Intelligence with Structured Scene Reasoning](https://arxiv.org/abs/2603.00409v1) · 分数 9
15. [Scaling Spatial Reasoning in MLLMs through Programmatic Data Synthesis](https://arxiv.org/abs/2512.16237v1) · 分数 9
16. [Towards Physics-informed Spatial Intelligence with Human Priors: An Autonomous Driving Pilot Study](https://arxiv.org/abs/2510.21160v1) · 分数 9
17. [SpatialLadder: Progressive Training for Spatial Reasoning in Vision-Language Models](https://arxiv.org/abs/2510.08531v1) · 分数 9
18. [Thinking in Structures: Evaluating Spatial Intelligence in Constraint-Governed Spaces](https://arxiv.org/abs/2602.07864v2) · 分数 9
19. [ESI-Bench: Towards Embodied Spatial Intelligence that Closes the Perception-Action Loop](https://arxiv.org/abs/2605.18746v2) · 分数 9
20. [Video2Layout: Recall and Reconstruct Metric-Grounded Cognitive Map for Spatial Reasoning](https://arxiv.org/abs/2511.16160v2) · 分数 9
21. [Which Pretraining Paradigm Better Serves Spatial Intelligence? An Empirical Comparison of Vision-Language and Video Generation Models](https://arxiv.org/abs/2605.28132v1) · 分数 9
22. [Multimodal Spatial Reasoning in the Large Model Era: A Survey and Benchmarks](https://arxiv.org/abs/2510.25760v2) · 分数 9
23. [Dual-Pathway Geometry-Aware MLLM for Spatial Intelligence](https://arxiv.org/abs/2605.25334v1) · 分数 9
24. [Spatial4D-Bench: A Versatile 4D Spatial Intelligence Benchmark](https://arxiv.org/abs/2601.00092v2) · 分数 9
25. [Ouroboros-Spatial: Closing the Data-Model Loop for Spatial Reasoning](https://arxiv.org/abs/2606.11719v2) · 分数 9
26. [Seeing through Imagination: Learning Scene Geometry via Implicit Spatial World Modeling](https://arxiv.org/abs/2512.01821v2) · 分数 9
27. [OpenSpatial: A Principled Data Engine for Empowering Spatial Intelligence](https://arxiv.org/abs/2604.07296v2) · 分数 9
28. [RieMind: Geometry-Grounded Spatial Agent for Scene Understanding](https://arxiv.org/abs/2603.15386v1) · 分数 9
29. [SpaceDG: Benchmarking Spatial Intelligence under Visual Degradation](https://arxiv.org/abs/2605.22536v2) · 分数 9
30. [SpatialImaginer: Towards Adaptive Visual Imagination for Spatial Reasoning](https://arxiv.org/abs/2604.17385v1) · 分数 9
31. [G&#36;^2&#36;VLM: Geometry Grounded Vision Language Model with Unified 3D Reconstruction and Spatial Reasoning](https://arxiv.org/abs/2511.21688v2) · 分数 9
32. [Keep It in Mind: User Centric Continual Spatial Intelligence Reasoning in Egocentric Video Streams](https://arxiv.org/abs/2606.15200v1) · 分数 9
33. [CrossView Suite: Harnessing Cross-view Spatial Intelligence of MLLMs with Dataset, Model and Benchmark](https://arxiv.org/abs/2605.18621v1) · 分数 9
34. [SpatioLM: Towards General Physical Spatial Intelligence in Vision-Language Models](https://arxiv.org/abs/2608.01899v1) · 分数 9
35. [Spatial-DISE: A Unified Benchmark for Evaluating Spatial Reasoning in Vision-Language Models](https://arxiv.org/abs/2510.13394v4) · 分数 9
36. [From Symbolic to Geometric: Enabling Spatial Reasoning in Large Language Models](https://arxiv.org/abs/2606.04381v1) · 分数 9
37. [MMSI-Video-Bench: A Holistic Benchmark for Video-Based Spatial Intelligence](https://arxiv.org/abs/2512.10863v1) · 分数 9
38. [SpatialSV: Internalizing Interpretable 3D Spatial Awareness in MLLMs via Task-Oriented Visual Supervision](https://arxiv.org/abs/2606.19915v1) · 分数 9
39. [SpatialBlock: Enhancing Spatial Intelligence in LVLMs via Synthetic Block-Stacking Problem](https://arxiv.org/abs/2609.07064v1) · 分数 9
40. [MultihopSpatial: Multi-hop Compositional Spatial Reasoning Benchmark for Vision-Language Model](https://arxiv.org/abs/2603.18892v2) · 分数 9
41. [Learning 3D Representations for Spatial Intelligence from Unposed Multi-View Images](https://arxiv.org/abs/2604.10573v1) · 分数 9
42. [Abstract 3D Perception for Spatial Intelligence in Vision-Language Models](https://arxiv.org/abs/2511.10946v3) · 分数 9
43. [MonoSR: Open-Vocabulary Spatial Reasoning from Monocular Images](https://arxiv.org/abs/2511.19119v2) · 分数 9
44. [Embodied3DBench: Benchmarking Low-Level Embodied Spatial Intelligence of Vision Language Models](https://arxiv.org/abs/2605.29074v1) · 分数 9
45. [Spatial-IQ: Deconstructing Spatial Intelligence via Hierarchical Capability Tests](https://arxiv.org/abs/2607.22864v1) · 分数 9
46. [SpatialThinker: Reinforcing Scene Graph-Grounded Spatial Reasoning via Dense Rewards](https://arxiv.org/abs/2511.07403v2) · 分数 9
47. [VABench: Measuring Embodied Spatial Intelligence through Visual Demonstrations, Active Perception, and Metric Control](https://arxiv.org/abs/2609.19554v1) · 分数 9
48. [World2Mind: Cognition Toolkit for Allocentric Spatial Reasoning in Foundation Models](https://arxiv.org/abs/2603.09774v1) · 分数 9
49. [3ViewSense: Spatial and Mental Perspective Reasoning from Orthographic Views in Vision-Language Models](https://arxiv.org/abs/2603.07751v2) · 分数 9
50. [Visual Agentic AI for Spatial Reasoning with a Dynamic API](https://openaccess.thecvf.com/content/CVPR2025/html/Marsili_Visual_Agentic_AI_for_Spatial_Reasoning_with_a_Dynamic_API_CVPR_2025_paper.html) · 分数 9
51. [SpatialStack: Layered Geometry-Language Fusion for 3D VLM Spatial Reasoning](https://arxiv.org/abs/2603.27437v3) · 分数 9
52. [SpaceEra++: A Unified Framework Towards 3D Spatial Reasoning in Video](https://arxiv.org/abs/2607.01784v1) · 分数 9
53. [Chain of Spatial Thoughts: Modality-Agnostic Spatial Grounding for Vision Language Models](https://arxiv.org/abs/2608.10278v1) · 分数 9
54. [SNOW: Spatio-Temporal Scene Understanding with World Knowledge for Open-World Embodied Reasoning](https://arxiv.org/abs/2512.16461v1) · 分数 9
55. [OneCanvas: 3D Scene Understanding via Panoramic Reprojection](https://arxiv.org/abs/2606.19253v1) · 分数 9
56. [Reasoning Path and Latent State Analysis for Multi-view Visual Spatial Reasoning: A Cognitive Science Perspective](https://arxiv.org/abs/2512.02340v1) · 分数 9
57. [Spatial-TTT: Streaming Visual-based Spatial Intelligence with Test-Time Training](https://arxiv.org/abs/2603.12255v1) · 分数 9
58. [SPARGen: Unifying Spatial Perception and Reasoning through Native Multimodal Generation](https://arxiv.org/abs/2608.14138v1) · 分数 9
59. [From Hallucination to Grounding: Diagnosing Visual Spatial Intelligence via CRISP](https://arxiv.org/abs/2606.26535v1) · 分数 9
60. [Disentangling 3D Modeling from Spatial Reasoning](https://arxiv.org/abs/2608.05242v2) · 分数 9
61. [Learning Geometric Representations from Videos for Spatial Intelligent Multimodal Large Language Models](https://arxiv.org/abs/2606.05833v2) · 分数 9
62. [EgoMind: Activating Spatial Cognition through Linguistic Reasoning in MLLMs](https://arxiv.org/abs/2604.03318v2) · 分数 9
63. [GraFT: A Training-Free Framework for Spatial Reasoning in Multimodal Large Language Models via 3D Scene Graphs](https://arxiv.org/abs/2609.03892v1) · 分数 9
64. [Spatial Memory Agent: Experience-Grounded Procedure Memory for Spatial Intelligence](https://arxiv.org/abs/2608.12743v1) · 分数 9
65. [Spa3R: Predictive Spatial Field Modeling for 3D Visual Reasoning](https://arxiv.org/abs/2602.21186v2) · 分数 9
66. [GST-Bench: Can VLMs Develop Global Spatial Awareness from Video?](https://arxiv.org/abs/2608.05747v1) · 分数 9
67. [Learning Multi-View Spatial Reasoning from Cross-View Relations](https://arxiv.org/abs/2603.27967v1) · 分数 9
68. [Learning to Reason in 4D: Dynamic Spatial Understanding for Vision Language Models](https://arxiv.org/abs/2512.20557v1) · 分数 9
69. [Active Exploring like a Pigeon: Reinforcing Spatial Reasoning via Agentic Vision-Language Models](https://arxiv.org/abs/2606.02459v1) · 分数 9
70. [NavSpace: How Navigation Agents Follow Spatial Intelligence Instructions](https://arxiv.org/abs/2510.08173v2) · 分数 9
71. [LAST: Leveraging Tools as Hints to Enhance Spatial Reasoning for Multimodal Large Language Models](https://arxiv.org/abs/2604.09712v1) · 分数 9
72. [Beyond Flatlands: Unlocking Spatial Intelligence by Decoupling 3D Reasoning from Numerical Regression](https://arxiv.org/abs/2511.11239v2) · 分数 9
73. [Boosting MLLM Spatial Reasoning with Geometrically Referenced 3D Scene Representations](https://arxiv.org/abs/2603.08592v2) · 分数 9
74. [Thinking with Blueprints: Assisting Vision-Language Models in Spatial Reasoning via Structured Object Representation](https://arxiv.org/abs/2601.01984v1) · 分数 9
75. [Vision-Language Memory for Spatial Reasoning](https://arxiv.org/abs/2511.20644v2) · 分数 9
76. [EagleVision: A Dual-Stage Framework with BEV-grounding-based Chain-of-Thought for Spatial Intelligence](https://arxiv.org/abs/2512.15160v2) · 分数 9
77. [SpatialQuery: Benchmarking Geometry-Grounded Multi-Instance Spatial Reasoning in Vision-Language Models](https://arxiv.org/abs/2608.01709v1) · 分数 9
78. [IGGT4D: Streaming 4D Instance-Grounded Geometry Transformer](https://arxiv.org/abs/2607.19228v1) · 分数 9
79. [ESPIRE: A Diagnostic Benchmark for Embodied Spatial Reasoning of Vision-Language Models](https://arxiv.org/abs/2603.13033v1) · 分数 9
80. [SpatialEvo: Self-Evolving Spatial Intelligence via Deterministic Geometric Environments](https://arxiv.org/abs/2604.14144v1) · 分数 9
81. [Pursuing Minimal Sufficiency in Spatial Reasoning](https://arxiv.org/abs/2510.16688v2) · 分数 9
82. [SpatialLLM: A Compound 3D-Informed Design towards Spatially-Intelligent Large Multimodal Models](https://openaccess.thecvf.com/content/CVPR2025/html/Ma_SpatialLLM_A_Compound_3D-Informed_Design_towards_Spatially-Intelligent_Large_Multimodal_Models_CVPR_2025_paper.html) · 分数 9
83. [Thinking with Camera: A Unified Multimodal Model for Camera-Centric Understanding and Generation](https://arxiv.org/abs/2510.08673v2) · 分数 9
84. [Thinking with Geometry: Active Geometry Integration for Spatial Reasoning](https://arxiv.org/abs/2602.06037v5) · 分数 9
85. [OVO-S-Bench: A Hierarchical Benchmark for Streaming Spatial Intelligence in Multimodal LLMs](https://arxiv.org/abs/2606.03890v2) · 分数 9
86. [Attention in Space: Functional Roles of VLM Heads for Spatial Reasoning](https://arxiv.org/abs/2603.20662v1) · 分数 9
87. [Visual Spatial Tuning](https://arxiv.org/abs/2511.05491v1) · 分数 9
88. [Perceive, Interact, Reason: Building Tool-Augmented Visual Agents for Spatial Reasoning](https://arxiv.org/abs/2606.12830v1) · 分数 9
89. [CVP: Central-Peripheral Vision-Inspired Multimodal Model for Spatial Reasoning](https://arxiv.org/abs/2512.08135v1) · 分数 9
90. [AlloSpatial: Agentic Harness Framework for Spatial Reasoning in Foundation Models](https://arxiv.org/abs/2606.08952v1) · 分数 9
91. [Reasoning in Space via Grounding in the World](https://arxiv.org/abs/2510.13800v2) · 分数 9
92. [MosaicThinker: On-Device Visual Spatial Reasoning for Embodied AI via Iterative Construction of Space Representation](https://arxiv.org/abs/2602.07082v1) · 分数 9
93. [Unleashing Spatial Reasoning in Multimodal Large Language Models via Textual Representation Guided Reasoning](https://arxiv.org/abs/2603.23404v2) · 分数 9
94. [GeoAnchor: Collaborative Reasoning via Latent Decomposition for 3D Spatial Understanding](https://arxiv.org/abs/2607.13454v2) · 分数 9
95. [SpatialMosaic: A Multiview VLM Dataset for Partial Visibility](https://arxiv.org/abs/2512.23365v4) · 分数 9
96. [Object-Uni: A Unified Model for Object-Centric Spatial Understanding and Controllable Generation](https://arxiv.org/abs/2608.22757v1) · 分数 9
97. [SpatialBench: Benchmarking Multimodal Large Language Models for Spatial Cognition](https://arxiv.org/abs/2511.21471v4) · 分数 9
98. [REM: Evaluating LLM Embodied Spatial Reasoning through Multi-Frame Trajectories](https://arxiv.org/abs/2512.00736v1) · 分数 9
99. [On the Generalization Capacities of MLLMs for Spatial Intelligence](https://arxiv.org/abs/2603.06704v1) · 分数 9
100. [SceneScaffold: Active Scene-State Construction for Unified 3D Scene Understanding](https://arxiv.org/abs/2609.33518v1) · 分数 9

[按公布时间查看](#/starter-pack/20261002-8fab4b9c60a3/dates)

阅读内容：已完成 10，待补充 90。
