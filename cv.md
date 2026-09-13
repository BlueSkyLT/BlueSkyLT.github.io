# CV — Iris Tian Lan (蓝天)

**Location:** Singapore  
**Email:** tian.lan@ntu.edu.sg 
**LinkedIn:** linkedin.com/in/tian-lan-82b21a132  

**GitHub:** github.com/BlueSkyLT  
<!-- Prefer 个人主页-->
**个人主页 Personal Website:** blueskylt.github.io 
<!-- Not finished yet, do not publish-->
**Status:** Chinese National / Singapore PR  
**ORCID:** https://orcid.org/0000-0001-6088-1039  
<!-- All set to private for now, do not publish-->

<!-- Phone (+65 96642877) and WeChat (kaeyasimp): do NOT put on public CVs unless Iris
     explicitly asks. Source of truth for contact: config/profile.yml (pulled from GitHub). -->

## Professional Summary 
<!-- summary and highlight from my skills) -->

PhD-level applied ML researcher and data sceientist with extensive experience in a wide range of topics including xxxxxx. Used architecting scalable data mining and predictive modeling pipelines across complex multimodal physical and cyber domains to solve whatever problems. Proven track record in ingesting, harmonizing, and extracting actionable intelligence from highly heterogeneous, noisy data sources—including geospatial data, dynamic network time-series, multimodal satellite radar imagery, and large-scale graph topologies and many more. Combines rigorous statistical reasoning and signal processing to support reliability monitoring, operational decision-making in complex systems. Fluent in Mandarin, English and Cantonese. Has extensive cross culture experience working with multi culture teams. Great presentation and communication skills and data visualization. 

<!-- SUMMARY VARIANTS (pick by track; default = industry/data above)
data_ml_lead: End-to-End Data & ML Scientist (Ph.D.) with extensive experience in architecting scalable data mining and predictive modeling pipelines across complex multimodal physical and cyber domains. Ingests, harmonizes, and models heterogeneous sources across high-frequency 1D signals, multivariate time-series, geospatial graphs, and multimodal satellite/radar data. Combines rigorous statistical inference with GNNs and Generative RAG systems to deliver high-impact, production-ready solutions.

industry_sg: Applied ML and data engineering researcher with end-to-end experience building production-oriented data pipelines and machine learning systems across heterogeneous data modalities—1D sensor signals, geospatial, tabular, and temporal. Designs and deploys graph-based and time-series models to support reliability monitoring, operational decision-making, and anomaly detection in complex systems.

fintech_quant: Data-driven researcher with broad expertise in analyzing and modeling complex datasets across quantitative domains. Experienced in collecting, processing, and integrating multimodal data—from 1D sensor signals and geospatial information to tabular and temporal datasets—into scalable pipelines for quantitative analysis. Designs machine learning models to uncover patterns, extract insights, and deliver reliable predictions for multivariate time-series.

research: I develop graph neural networks and statistical learning frameworks that discover and exploit graphical relationships in both image and non-image data, bridging computer vision, signal processing, and geometric deep learning for robust, scalable structured prediction.

applied_ai: PhD-level applied ML researcher who builds production data/ML pipelines and deployed custom domain RAG agents. Translates domain corpora (video, audio, text) into end-to-end conversational systems with incremental knowledge retrieval, cost-aware model routing, and source-grounded answering.
-->

## Work & Research Experience

### School of Electrical and Electronic Engineering, Nanyang Technological University (NTU)  — Singapore
**Research Fellow**  
Dec 2024 - present

#### ASCAD: AES Side-Channel Attack and Leakage Detection from High-Frequency Power Traces

<!-- Integrated Systems Research Laboratory (ISRL@NTU) — Singapore 
Period: June 2026 – present
Supervisor: Prof. Gwee Bah Hwee
-->

**Challenge**

- **高阶掩码防御下的微弱物理泄露**

  - 针对密码芯片硬件（AES-128 及带防御机制的 Masked AES），评估其物理运行中的功耗与电磁辐射（EM）侧信道信息泄露脆弱性。

- **极端高维、低信噪比与非同步抖动**

  - 硬件采集的功耗波形单条长达数万个时间采样点，信噪比极低，且存在由芯片内部时钟抖动引起的非同步相位漂移，导致传统差分/相关能量分析（DPA/CPA）完全失效。

**Approach**

- **高吞吐量 1D 时序信号预处理流水线**

  - 结合 AES 电路时钟周期先验进行兴趣点（POI）区间切片与主成分降维（PCA），精准提取 S-box 字节代换敏感操作区间。
- **深度学习侧信道攻防建模**

  - 设计针对 1D 时序信号的多尺度深度卷积神经网络（1D-CNN）与多层感知机（MLP）， made use of physical theories for the power of the digital circuit and build a physical based loss with cross-correlation, so that we can optimize the POI finder. 

**Results**

- **破译效率与防御量化 (Business Impact & Metrics)**

  - 基于标准 ASCAD 数据集评估猜测熵（Guessing Entropy, GE）与攻击成功率（Success Rate, SR）；
  - 在强噪声掩码环境下，将完整恢复 16 字节密钥所需的功耗曲线（Trace）条数降低数倍，有效量化评估了硬件物理防御强度。

---

#### Network Anomaly and Cyberattack Detection in Communication Networks

<!-- Centre for Information Sciences and Systems (CISS@NTU) — Singapore
Position: Researcher
Period: June 2025 – present
Supervisor: Prof. Tay Wee Peng
-->

**Challenge**

 - This is a **Graph Time Series**. In a network we only have partial observations of message broadcasting info and we need to detect from the message logs when there is an attack and find out where the attack is on the network, as soon as possible. It's run on a bipartite graph that is dynamic instead of a normal graph. Also the attack type varies so the patterns changes a lot. We are also lack of data so we need to simulate and run our test on simulated data. Also the message logs are non-synchronized or unevenly-spaced.
    

**Approach**

- **Algorithm & Mathematical Modeling:** Models network message boardcasting and simulate the graph strucuture and message transferring routes and then our observations.
- Convert bipartite graphs into normal graphs and make non-synchronized time series work with other time series works by patching.
- we build and test varies metrics to detemine the normal/abnormal behavior of nodes
- Use flexible gnn models to face differnt types of attacks.
- In case of fast real time detection we keep track of what's the node's normal activity level in the normal days and keeps a dynamic expectation and alarm when above a carefully calibrated threshold.

**Results**

- **细粒度监控与定位**

  - 实现了对网络异常攻击的天级监控与节点级/链路级的精准微观定位；在拓扑剧烈扰动和低信噪比下大幅降低漏报率，为网络态势感知提供实时可靠决策支持。 Can detect varies types of attacks for graphs with 50+ nodes while only half of the observation is available. Enables day-level anomaly monitoring with node- and link-level attack localization, improving operational visibility under topology shifts, noise.

#### Statistically graranteed disease source detection in social network

<!-- Centre for Information Sciences and Systems (CISS@NTU) — Singapore
Position: Researcher
Period: June 2025 – present
Supervisor: Prof. Tay Wee Peng
成果背书：AAAI 2026 (CCF-A 类，三作)
-->

**Challenge**

- **快照观测下的逆问题病态性**

  - 在社交网络谣言扩散、传染病溯源或金融风险传染场景中，通常只能获取某一时刻全网节点感染状态的单次快照（Snapshot Observation）。不同初始信源集合极易演化出高度相似的感染格局，属于极度病态的逆问题。

- **传统模型缺乏统计置信度保证**

  - 传统中心度启发式算法或参数化扩散模型（固定参数的 SIR/SI/IC）依赖强先验假设，在真实无先验场景下无法评估预测不确定性，难以给出可靠置信度区间。

**Approach**

- **Spatial Temporal GNN 节点级后验概率打分网络**

  - Use 图神经网络提取节点在未知级联扩散动力学下的局部与全局网络拓扑特征，输出节点属于初始信源的非一致性评分（Non-conformity Score）。
    
- **保形风险控制（Conformal Risk Control, CRC）框架**

  - 将网络多源定位转化为带统计覆盖保证的候选集合预测问题；利用校准集（Calibration Set）计算保形分位数阈值，自适应构造预测子集。
- **有限样本下的无假设理论保证**

  - 严格证明了在仅满足数据可交换性（Exchangeability）的前提下，无需对扩散动力学参数做任何分布假设，即可在有限样本下严格保证预测集合达到用户预设的名义召回率（$1-\alpha$）。

**Results**

- **理论召回达标与预测集紧致**

  - 在多种复杂合成拓扑与真实社交/接触网络上，严格满足 90%、95% 的名义召回率，同时保持极小的预测集冗余度（Set Size 紧致）；
  - 成果发表于人工智能顶级会议 **AAAI 2026**（CCF-A 类）并开源基准算法库 (第三作者)。

---

#### Improving Component Detection and Classification on PCB Images with Location-Encoded Graphs

<!-- Temasek Laboratories (TL@NTU) — Singapore
Supervisor: Prof. Gwee Bah Hwee
身份/周期：核心完成人 (2024.12 – 2025.05)
成果背书：Paper: Meta: Graph-encoded Printed Circuit Board Datasets for Component Classification with Graph Neural Networks. (first author)
-->

**Challenge**

- **纯视觉表征失效与严重混淆**

  - 工业级高分辨率图像中，核心集成电路（IC）、分立晶体管（Discrete Transistor, DT）、二极管（Diode）等电子元器件外观极度相似（相似封装尺寸、规则矩形、纯黑/金属质感），缺乏自然图像丰富的纹理与上下文语义，传统 CNN/ViT 在分类时极易发生假阳性（False Positives）。
- **背景分布偏移与几何几何多变**

  - 跨厂商/产线的板级图像存在光照不均、阻焊层底色各异、大面积无信息空白等噪声扰动，导致视觉模型产生严重的分布偏移（Distribution Shift），且对板卡旋转/缩放等几何变换敏感。
- **极端类别不平衡与图异质性（Heterophily）**

  - 元器件分布呈长尾效应，大量常规贴片器件（电阻/电容等构成的 Others 类占比 >85%），核心元器件面临高达 10x 以上的样本不平衡；
  - 布局逻辑上，同类器件极少聚集，相连邻域多为不同类器件，网络呈现典型的**强异质图（Heterophilic Graph）**特性，常规 GNN（GCN、GAT）的消息平滑机制会发生灾难性性能退化。

**Approach**

- **基于 Voronoi 空间细分的平面图拓扑构建（Spatial Graph Construction Pipeline）**

  - 抛弃经验式的 k-NN 或固定距离截断（避免局部密集时连边截断或稀疏时跨区域强连），提出基于 Voronoi Tessellation（沃罗诺伊多边形镶嵌） 的自适应空间拓扑构建算法；
  - 将检测定位的元器件中心作为图节点 v ∈ V，将全图空间自适应划分为凸多边形 Cell Rᵥ，仅在共享边界的相邻 Cell 间建立无向边 E，将二维视觉连续空间精准映射为数学上的平面图（Planar Graph），完美保留电路物理布局的相对空间位置，同时滤除 90% 以上无信息背景噪声。
- **多模态节点特征融合（Visual-Spatial Representation）**

  - 节点特征层结合预训练 ResNet50 特征抽取器提取元器件局部视觉嵌入，并融合节点局部/全局图论结构特征（平均度 ~6、局部聚集系数、网络直径）；
  - 构建针对元器件位置/旋转不变性的归一化空间拓扑特征。
- **异质图神经网络与抗不平衡训练机制（Heterophilic GNN & Loss Design）**

  - 针对异质图特性引入 Ego-Neighbor 嵌入解耦机制（GAT-sep、GT-sep）与动态聚合器（GraphSAGE Std / Attn, ACM-GNN）；
  - 设计加权二元交叉熵损失（Weighted BCE Loss）与逆频次采样策略，根据类别出现概率动态补偿稀有类别（IC/DT/Diode）权重。
- **下游系统级 IC 分割集成（SSR-SAGE Pipeline）**

  - 将 GNN 分类器作为核心过滤决策模块，替换传统语义分割架构（SSRNet）的纯图像分类器，构建 粗分割（Few-shot Self-Support Prototype）+ 图拓扑分类筛选（Graph Classifier） 的端到端硬件可靠性验证流水线。
  
**Results**

- **数据集构建与高效图解析流水线**

  - 处理来自50+不同厂商来源的复杂工业板卡图像，构建并开源 Graph-F 与 Graph-W 工业图基准库；
  - 优化空间图构建执行效率，单张超大工业图像生成拓扑图平均仅耗时 0.81s ~ 1.49s，整网训练在单卡 RTX A5000（24GB）上平均 20~50 秒即可完成 200 epochs 收敛。
- **核心分类指标提升**

  - 在严格排除 Others 背景类干扰的 Subset F1-Score 评估下，GraphSAGE 与解耦异质图模型取得 0.84 ~ 0.85 的极高分类性能，相比纯视觉 MLP 基准（0.77 / 0.61）显著提升；
  - 通过交叠检测百分比（Percentage of Overlapping Detections, POD）验证，图网络从拓扑结构中挖掘出纯视觉模型完全忽略的互补判别信息。
- **下游 IC 分割指标跨越式提升**

  - 在端到端 IC 分割任务中，结合图分类器的 SSR-SAGE 达成：
  - IoU 提升至 0.6619（显著超越 U-Net 0.5481、DeepLabv3 0.5364、原始 SSRNet 0.5957）；
  - Dice 提升至 0.7599（原始 SSRNet 0.7123）；
  - 像素级错误率（Error Rate）直降至 0.0224（下降约 30%）。

<!-- 在不同类型 CV 中的裁剪使用建议（即插即用）

┌───────────────────────────┬─────────────────────────────────────────────────────────────────────────────────────┐
│ 简历投递方向              │ 提取重点与关键词建议                                                                │
├───────────────────────────┼─────────────────────────────────────────────────────────────────────────────────────┤
│ Applied ML / Algorithm    │ 强调 Voronoi 平面图拓扑建模、异质图（Heterophilic GNN）解耦设计、加权 BCE 处理 10x  │
│ 算法岗                    │ 类别不平衡、IoU/F1 量化收益。                                                       │
├───────────────────────────┼─────────────────────────────────────────────────────────────────────────────────────┤
│ Data Mining / Data        │ 强调 空间细分算法流水线、跨 50+ 厂商异构图像特征清洗与结构化映射、单图 0.8s         │
│ Engineer 数据工程岗       │ 秒级图构建与批处理吞吐、开源基准数据集发布。                                        │
├───────────────────────────┼─────────────────────────────────────────────────────────────────────────────────────┤
│ Computer Vision /         │ 强调 空间拓扑与 ResNet 局部特征联合表征、对抗工业图像背景分布偏移与微小部件外观混淆 │
│ Multimodal 视觉/多模态岗  │ 、下游分割 IoU 提升。                                       │
└───────────────────────────┴─────────────────────────────────────────────────────────────────────────────────────┘

-->

---


### Satellite Research Centre (SaRC@NTU), Nanyang Technological University (NTU) — Singapore
**PhD Researcher**  
August 2019 – December 2024
<!-- Supervisor: Prof. Wen Bihan 
This can be merged with NTU experience above-->

#### Public-Transport and Demographic Graph Learning for Urban Site Selection

<!-- 成果背书：Remote Sensing (JCR Q1, 2022, 一作) -->

**Challenge**

- **多源多模态城市数据割裂**

  - 商业零售选址与城市空间吸引力预测需同时融合宏观人口统计、中观路网拓扑与微观兴趣点（POI）。传统多准则决策（MCDM）或平铺统计回归无法处理高维异构非结构化数据。
- **忽略交通网络上的非线性空间溢出效应**

  - 传统空间计量模型依赖简单地理欧氏距离，无法刻画公共交通路网（MRT/公交）引流产生的非线性流动与商业活力空间溢出（Spatial Spillover）效应。

**Approach**

- **全岛多源异构数据清洗与 LTSG 基准构建**

  - 抓取、清洗并空间对齐新加坡全岛多源异构公开数据，构建并开源 **Land and Transport Singapore (LTSG)** 基准数据集；
  - 整合全岛 55 个规划区组屋（HDB）人口/房型统计表、数百个 MRT/LRT 地铁站与公交站点矢量坐标、以及餐饮/零售全量 POI 属性与类别分布。
- **公共交通空间拓扑图构建**

  - 将全岛地理栅格单元作为图节点，以真实公共交通通勤时间、换乘便利度及路网连通性构建加权邻接矩阵，建立真实反映人群流动效率的交通拓扑图。
- **空间图卷积（GCN）预测模型**

  - 部署多层 GCN 模型联合聚合邻域节点的空间多源特征与拓扑流动信息，学习高维可解释的区域空间嵌入（Spatial Embeddings），端到端预测区域商业吸引力与选址得分。

**Results**

- **预测性能超越传统基准**

  - 在真实商业零售选址任务上，GCN 模型均方误差（MSE）与排序准确率显著超越多层感知机（MLP）与传统空间自回归模型；
  - 成果发表于权威英文 SCI 期刊《Remote Sensing》（JCR Q1，一作），LTSG 数据集在 GitHub 开源。
 
<!-- role-tailoring guides

┌───────────────────────────┬─────────────────────────────────────────────────────────────────────────────────────┐
│ 简历投递方向              │ 提取重点与关键词建议                                                                │
├───────────────────────────┼─────────────────────────────────────────────────────────────────────────────────────┤
│ Applied ML / Algorithm    │  │
│ 算法岗                    │                                            │
├───────────────────────────┼─────────────────────────────────────────────────────────────────────────────────────┤


-->

#### Real-time Radar Satellite Image Segmentation Algorithm

<!-- 成果背书：Remote Sensing (JCR Q1, 2024, 一作) -->

**Challenge**

- **光学遥感的全天候盲区**

  - 高分辨率光学遥感卫星受制于多云、雨雾气象与建筑物/树木阴影，道路特征极易被遮挡造成语义分割断裂与漏检。
- **SAR 雷达解译困难与高质量样本匮乏**

  - 合成孔径雷达（SAR）具备全天候微波穿透能力，但图像存在强相干斑噪声与几何失真，且在轨采集成本极高、业内极度缺乏高质量标注的高分辨率 SAR 遥感数据集。
- **星上边缘算力约束（Onboard Edge Compute）**

  - 道路分割算法需面向卫星载荷侧 **FPGA** 部署（无桌面级 GPU），要求模型轻量、低功耗推理；地面训练/仿真可用 GPU，星上推理以 FPGA 为约束。

**Approach**

- **首个高分辨率多模态道路基准 HSRD 构建**

  - 发起并开源 **HybridSAR Road Dataset (HSRD)**，包含 SpaceNet-6 真实 SAR 影像、光学影像以及利用 OpenStreetMap（OSM）矢量路网转换对齐的高精掩码；建立自动化亚像素级配准流水线。
- **物理仿真流水线与 3D 几何建模（KAISAR Simulation Pipeline）**

  - 基于微波物理光学与电磁散射原理，依托 GPU 加速的 KAISAR 仿真平台开发端到端合成数据生成流水线；
  - 导入地物高精 3D 几何网格模型，设定雷达载频、极化方式、入射角等物理参数，批量模拟生成高分辨率单视复数（SLC）微波遥感图像（SN3-SAR / SN6-SynSAR 数据集），用于下游预训练与数据增强。
- **跨模态特征融合网络架构**

  - 设计双流多尺度编码器，分别提取光学多光谱纹理特征与 SAR 微波后向散射强度特征；
  - 引入跨模态注意力融合模块，自适应根据光学遮挡程度动态调整雷达特征权重，恢复被云层遮挡的道路拓扑连续性。

**Results**

- **恶劣环境下路网连通性突破与顶刊发表**

  - 在严重云雾与阴影干扰场景下，多模态融合网络在道路分割 IoU 与拓扑连通度指标上显著超越单模态光学基准；
  - 成果发表于权威英文 SCI 期刊《Remote Sensing》（JCR Q1，一作）以及自动化与视觉国际会议 *ICARCV 2024*（一作）。
 
<!-- 在不同类型 CV 中的裁剪使用建议（即插即用）

┌───────────────────────────┬─────────────────────────────────────────────────────────────────────────────────────┐
│ 简历投递方向              │ 提取重点与关键词建议                                                                │
├───────────────────────────┼─────────────────────────────────────────────────────────────────────────────────────┤
│ Applied ML / Algorithm    │ 强调 算法 make use of SOTA of challenges, with Resnet and GAN  │
│ 算法岗                    │ extreme类别不平衡、。                                                       │
├───────────────────────────┼─────────────────────────────────────────────────────────────────────────────────────┤
│ Data Mining / Data        │ 强调automatic multi source map image gathering and slicing and pairing with geospatial codes │
│ Engineer 数据工程岗       │ 、开源基准数据集发布。                                        │
├───────────────────────────┼─────────────────────────────────────────────────────────────────────────────────────┤
│ Computer Vision /         │ 强调multimodal images, radar image is very different from optical data │
│ Multimodal 视觉/多模态岗  │ 。                                       │
└───────────────────────────┴─────────────────────────────────────────────────────────────────────────────────────┘

-->

---

### Columbia University — United States

#### 3D Astrophysical Fluid Simulation and Spatiotemporal Dynamics Analysis

<!-- Columbia Astrophysics Laboratory 
Position: Research Assistant 
Period: August 2017 – August 2019
Supervisor: Prof. Greg Bryan
-->

**Challenge**

- **宇宙学尺度下的高维流体耦合**

  - 研究星系形成过程中星系际介质（Circumgalactic Medium, CGM）的流体动力学演化与湍流冷却机制。模拟网格数据量达多 Terabytes，涉及流体力学、引力场与热力学辐射冷却的高维非线性耦合。

**Approach & Results — Three Dimensions**

- **Algorithm & Mathematical Modeling:** Uses numerical integration, grid interpolation, and statistical-physics modeling to estimate CGM temperature-density phases and cooling timescales in galaxy-formation simulations.

  - **Engineering & System Architecture:** Implements a distributed Python pipeline for multi-terabyte simulation grids and extracts physical structures from coupled fluid, gravity, and radiative-cooling fields.

  - **Business Impact & Metrics:** Converts large, complex simulations into quantitative evidence about phase boundaries and cooling behavior for galaxy-accretion and star-formation research.

**Detailed Implementation**

- **高性能分布式数据处理与统计建模**

  - 基于 Python 开发分布式多 TB 级网格数据处理流水线，执行大规模数值积分、网格插值与统计物理建模；推导并建立了 CGM 介质温度-密度多相态演化与冷却速率的数学估算模型。

**Results**

- **提取物理属性**

  - 从复杂多相动态流体模拟中稳健提取相变边界与冷却时标，为星系吸积与恒星形成反馈理论提供了定量数值支撑。

#### High-Dimensional Genomic Signal Extraction with Contrastive PCA

<!-- Department of Computer Science, Columbia University
Position: Research Assistant 
Period: January 2019 – May 2019
Supervisor: Prof. Itsik Pe'er
-->

**Challenge**

- **高维遗传特征与强族裔背景干扰**

  - 生物学家试图通过分析 DNA 寻找精神分裂症发病相关的基因，但数据包含 100,000+ 个单核苷酸多态性（SNPs）位点，特征维度极高。在传统主成分分析（PCA）等算法下，普遍存在的族裔背景群体结构（Population Stratification）构成主要方差成分，导致真实的致病遗传关联信号极度微弱。

**Approach & Results — Three Dimensions**

- **Algorithm & Mathematical Modeling:** Applies contrastive PCA and generalized eigenvalue decomposition to separate disease-specific genomic variation from dominant population-stratification directions.

  - **Engineering & System Architecture:** Processes 100,000+ SNP features by contrasting case and background datasets in an unsupervised dimensionality-reduction workflow.

  - **Business Impact & Metrics:** Removes ancestry-related confounding and improves the sensitivity of low-signal disease-associated variant discovery.

**Detailed Implementation**

- **对比主成分分析（Contrastive PCA, cPCA）**

  - 引入对比学习与广义特征值分解，在目标数据集（病例组）与背景数据集（对照组/族裔背景）之间优化对比目标函数；在无监督模式下自动消除由祖源结构引起的背景主方差方向，精准分离提取出与精神分裂症发病特异性强相关的微弱多态性变异信号。

**Results**

- **混杂偏差消除与致病位点定位**

  - 成功剥离了混合族裔的全局群体结构混淆，显著提升了低信噪比下疾病相关变异位点的识别灵敏度。

---

### University of Illinois Urbana-Champaign (UIUC) — United States

#### Radio Interferometry and 3D Spectral-Line Kinematics for Galaxy Analysis

<!-- Department of Astronomy, UIUC
Position: Research Assistant  
Period: May 2015 – May 2017
Supervisor: Prof. Tony Wong
成果背书：ApJ 顶刊发表 (2018)
-->

**Challenge**

- **极低信噪比与基线漂移**

  - 来自 CARMA 毫米波干涉阵列、GBT 及 VLA 射电望远镜的星系外分子气体三维谱立方体（Position-Position-Velocity Spectral Cubes）信号极其微弱，被淹没在接收机热噪声与时变频域基线漂移中。

**Approach & Results — Three Dimensions**

- **Algorithm & Mathematical Modeling:** Uses adaptive smoothing, polynomial baseline fitting, Gaussian line fitting, and moment analysis to recover velocity fields, dispersions, and rotation curves from spectral cubes.

  - **Engineering & System Architecture:** Builds a signal-processing workflow across CARMA, GBT, and VLA observations to handle weak signals, receiver noise, and time-varying frequency baselines.

  - **Business Impact & Metrics:** Turns low-SNR radio observations into reliable three-dimensional molecular-gas kinematics and contributed to an ApJ publication.

**Detailed Implementation**

- **微弱谱线去噪与基线拟合**

  - 开发高阶多项式动态基线拟合与自适应平滑算法，消除接收机频域基线漂移；
  - 基于高斯谱线拟合与矩分析（Moment Analysis），从微弱发射谱中稳健提取分子气体速度场、速度弥散剖面与三维旋转曲线。

**Results**

- **顶刊发表与星系动力学刻画**

  - 准确刻画了近邻星系分子与电离气体的三维运动学特征；成果作为核心合作者发表于天体物理顶级权威期刊 *The Astrophysical Journal (ApJ)*（2018）。

---


#### 定制化垂直领域多模态 RAG 智能体与自动化分析系统
Customized Multimodal RAG Agent & Automated Analytics System

<!-- Period: January 2026 – June 2026
Tech Stack: Python, Telegram Bot API, Vector DB, ASR, RAG, Webhook, Docker
-->

**Challenge**

- **垂直领域高拟真交互与严格防幻觉**

  - A knowledge-domain client’s community generated frequent, repetitive questions. Without the client’s private course corpus, a general-purpose model could produce generic, off-target, or hallucinated answers and could not reproduce the client’s professional style.
- **多模态语料解析与增量维护**

  - The client continuously updated video courses and livestreams on Douyin/Bilibili, so the knowledge base needed automated ingestion and low-cost incremental updates rather than full vector-store rebuilds.

**Approach**

- **多模态 ETL 自动化数据清洗流水线**

  - 构建自动化爬取脚本定向抓取抖音/B站长视频课程，进行格式转码与音频提取；
  - 接入自动语音识别（ASR）引擎生成带精准时间戳的高保真逐字稿；结合咨询笔记与讲义进行降噪与元数据标注。
  - 每天自动收集并监测聊天记录，分析内容制作成报告给用户
- **语义分块、增量向量索引与混合检索（Hybrid RAG）**

  - 依据客户领域语境与对话逻辑设计语义分块（Semantic Chunking）策略，构建稠密向量索引；
  - 实施 **BM25 关键词 + Dense 向量双路混合检索与重排（Rerank）**，回答生成严格附带**精确来源引用（对应视频片段秒数/讲义章节）**；
  - 建立定时增量索引任务，对新增视频逐字稿与社群答疑做增量 Upsert。
- **Bot 交互层、多轮记忆与成本感知路由**

  - 基于 Telegram Webhook 实现群内 `@` 提及与私聊交互，配置防刷限流与置信度不足兜底；
  - 设计基于学员 ID 的轻量级对话状态机，保持多轮追问上下文一致；

**Results**

- **社群高频答疑自动化**

  - 实现了 7×24 小时社群答疑自动化，回答口吻高度契合客户风格，有效承接了 80% 以上的常见课程咨询，知识库自动保持最新状态。

## Education

<!-- EDUCATION_INTERNAL: see config/education-facts.yml and references/education-policy.md
     Public view = industry_default: three schools, completion year ONLY.
     Never emit attendance ranges or SYSU on public PDFs. -->

- **Ph.D., Electrical and Electronic Engineering** — Nanyang Technological University (Singapore), **2025**
- **Bridge to Ph.D. Program in the Natural Sciences (Astrophysics)** — Columbia University, **2019**
- **B.S., Physics & Astronomy** — University of Illinois Urbana-Champaign, **2016**

## Honors & Awards 人才计划/项目

- 上海市超级博士后激励计划
- 上海市白玉兰人才计划青年项目

## Publications

1. **Jian, Xingchao; Zhang, Purui; Lan, Tian; et al.** Conformal Prediction for Multi-Source Detection on a Network. *The Fortieth AAAI Conference on Artificial Intelligence (AAAI)*, 2026. https://openreview.net/forum?id=GkpSmLe5Jx  
   *Uncertainty quantification and statistical inference on source detection with network-structured data.*

2. **Lan, Tian; Wang, Yuhang; Ji, Feng; et al.** Meta: Graph-encoded Printed Circuit Board Datasets for Component Classification with Graph Neural Networks. *IEEE Data Descriptions*, 2026.  
   *Graph-based feature extraction and node classification on 20k+ component dataset (GraphPCB).*

3. **Lan, Tian; He, Shuting; Qing, Yuanyuan; Wen, Bihan.** Leveraging Mixed Data Sources for Enhanced Road Segmentation in Synthetic Aperture Radar Images. *Remote Sensing*, 16(16), 3024, 2024. https://doi.org/10.3390/rs16163024  
   *Multi-modal data fusion for road extraction from optical and radar images (HSRD).*

4. **Lan, Tian; Wen, Bihan.** A Physics-Based SAR Simulation Framework for Remote Sensing Imaging. *Proceedings of ICARCV*, 2024.  
   *Physics-based SAR simulation (optional on short industry CVs).*

5. **Lan, Tian; Cheng, Hao; Wang, Yi; Wen, Bihan.** Site Selection via Learning Graph Convolutional Neural Networks: A Case Study of Singapore. *Remote Sensing*, 14(15), 3579, 2022. https://doi.org/10.3390/rs14153579  
   *Multi-source data integration and predictive modeling on transportation networks (LTSG).*

## Teaching Experience

<!-- Default: omit on industry PDFs; include for teaching / academic tracks. -->

### Youlu (有录) — Part-time study-abroad tutor

August 2024 – present

- Guided students from high school through graduate level on applications to top universities in the US, UK, Australia, Hong Kong, and Singapore.
- Coached personal statements, research proposals, and full-English interview preparation (mock interviews, profile advice).

### Nanyang Technological University — Teaching Assistant

August 2021 – August 2023

- Guided undergraduate students on machine learning team projects from design through implementation and presentation.
- Led weekly discussion and lab sessions connecting theory to practice.
- Developed supplementary teaching materials and programming tutorials for diverse learner needs.
- Independently designed a full teaching package on NAND-gate circuits (principles, logic, applications).

### University of Illinois Urbana-Champaign — Grader / Undergraduate teaching support

Spring 2015

- Prepared grading rubrics and sample solutions; graded homework and quizzes for astronomy coursework.
- Assisted observational lab sessions: set up telescopes and gave sky tours to undergraduates and the public.

### Sun Yat-sen University — Student assistant

Spring 2013

- Coordinated guest lecturer visits and logistics for special lecture series.
- Designed and analyzed feedback surveys on guest talks; produced posters and outreach materials.

## Skills

- **Programming:** Python (NumPy, Pandas, PyTorch, Scikit-learn), C++, Linux, Git, LaTeX  
- **Data Engineering:** web scraping, ETL pipelines, dataset construction, standardization, data visualization
- **Machine Learning:** Graph Neural Networks, time-series forecasting, anomaly detection, feature engineering, image segmentation, uncertainty quantification / conformal prediction  
- **LLM applications / agents:** ACP (stdio agent protocol); MCP tool servers; custom agent skills, personas, and workflows; Telegram agent UX; human-in-the-loop tool use; multi-provider model endpoints; Ollama for local small-model experiments.  
- **Languages:** English; Chinese (Mandarin, Cantonese, Hakka)

## Teaching-track extras (CN market / teaching roles)

- Subject breadth: mathematics, physics, computer science, data science, astronomy  
- Full-English teaching experience across international universities  
- Cross-border education (China, US, Singapore); familiarity with top-university admissions coaching  
- Ongoing AI research publications to connect teaching with research frontiers  

## References (on request)

- **Tay Wee Peng** — Associate Professor, School of Electrical and Electronic Engineering, NTU  
- **Wen Bihan (文碧汉)** — Associate Professor, School of Electrical and Electronic Engineering, NTU  
- **Itsik Pe'er** — Professor, Department of Computer Science, Columbia University  
- **Greg Bryan** — Professor, Department of Astronomy, Columbia University  

<!-- Source vault: ../CV_Lan/ (Research banks, CV_*.tex track framing, Publications/lt.bib, Teaching/, Education/master.tex).
     Edit facts here for career-ops generation; prefer jargon from references/jargon-bank.md. -->
