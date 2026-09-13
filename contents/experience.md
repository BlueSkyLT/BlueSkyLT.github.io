### School of Electrical and Electronic Engineering, Nanyang Technological University (NTU) — Singapore
**Research Fellow** &nbsp;|&nbsp; 研究员
Dec 2024 – present

#### ASCAD: AES Side-Channel Attack and Leakage Detection from High-Frequency Power Traces

*Detects side-channel information leakage (power/EM) from masked AES-128 hardware using deep learning on
high-frequency, low-SNR, non-synchronized power traces.*

**Challenge 挑战**
- 高阶掩码防御下的微弱物理泄露：针对密码芯片硬件（AES-128 及带防御机制的 Masked AES），评估其物理运行中的功耗与电磁辐射（EM）侧信道信息泄露脆弱性。
- 极端高维、低信噪比与非同步抖动：硬件采集的功耗波形单条长达数万个时间采样点，信噪比极低，且存在由芯片内部时钟抖动引起的非同步相位漂移，导致传统差分/相关能量分析（DPA/CPA）完全失效。

**Approach 方法**
- 高吞吐量 1D 时序信号预处理流水线：结合 AES 电路时钟周期先验进行兴趣点（POI）区间切片与主成分降维（PCA），精准提取 S-box 字节代换敏感操作区间。
- 深度学习侧信道攻防建模：设计针对 1D 时序信号的多尺度深度卷积神经网络（1D-CNN）与多层感知机（MLP），并结合数字电路功耗的物理理论构建带互相关的物理损失函数，用于优化 POI 定位。

**Results 成果**
- 基于标准 ASCAD 数据集评估猜测熵（Guessing Entropy）与攻击成功率（Success Rate）；在强噪声掩码环境下，将完整恢复 16 字节密钥所需的功耗曲线（Trace）条数降低数倍，有效量化评估了硬件物理防御强度。

---

#### Network Anomaly and Cyberattack Detection in Communication Networks

*Graph time-series anomaly detection on dynamic bipartite communication networks with partial, non-synchronized
observations, localizing attacks at node/link level in near real time.*

**Challenge 挑战**
- Only partial observations of message broadcasting are available, and attacks must be detected and localized on
  a dynamic bipartite graph as early as possible; attack patterns vary widely and data is scarce, requiring
  simulation, and message logs are non-synchronized / unevenly spaced.

**Approach 方法**
- Models network message broadcasting and simulates the graph structure, message routes, and resulting
  observations.
- Converts bipartite graphs into normal graphs and aligns non-synchronized time series with other time-series
  methods via patching.
- Builds and tests various metrics to determine normal/abnormal node behavior, and uses flexible GNN models to
  handle different attack types.
- For fast real-time detection, tracks each node's normal activity baseline and raises alarms when a calibrated
  threshold is exceeded.

**Results 成果**
- 实现了对网络异常攻击的天级监控与节点级/链路级的精准微观定位；在拓扑剧烈扰动和低信噪比下大幅降低漏报率，为网络态势感知提供实时可靠决策支持。Can detect various types of attacks on graphs with 50+ nodes while only half of the observations are available,
  enabling day-level anomaly monitoring with node- and link-level attack localization.

#### Statistically Guaranteed Disease Source Detection in Social Networks

*Conformal-risk-controlled source localization on network snapshots with distribution-free statistical coverage
guarantees. Published at AAAI 2026 (CCF-A, 3rd author).*

**Challenge 挑战**
- 快照观测下的逆问题病态性：在社交网络谣言扩散、传染病溯源或金融风险传染场景中，通常只能获取某一时刻全网节点感染状态的单次快照，属于极度病态的逆问题。
- 传统模型缺乏统计置信度保证：传统中心度启发式算法或参数化扩散模型（固定参数的 SIR/SI/IC）依赖强先验假设，无法评估预测不确定性。

**Approach 方法**
- Spatial-Temporal GNN 节点级后验概率打分网络：提取节点在未知级联扩散动力学下的局部与全局网络拓扑特征，输出节点属于初始信源的非一致性评分（Non-conformity Score）。
- 保形风险控制（Conformal Risk Control）框架：将多源定位转化为带统计覆盖保证的候选集合预测问题，利用校准集计算保形分位数阈值。
- 严格证明了仅需数据可交换性（Exchangeability）假设，无需对扩散动力学参数做任何分布假设，即可在有限样本下保证预测集合达到用户预设的名义召回率。

**Results 成果**
- 在多种复杂合成拓扑与真实社交/接触网络上，严格满足 90%、95% 的名义召回率，同时保持极小的预测集冗余度；成果发表于 **AAAI 2026**（CCF-A 类），并开源基准算法库（第三作者）。

---

#### Improving Component Detection and Classification on PCB Images with Location-Encoded Graphs

*First author. Graph-based, location-encoded component classification on industrial PCB images, published as an
open dataset paper.*

**Challenge 挑战**
- 纯视觉表征失效与严重混淆：工业级高分辨率图像中，IC、分立晶体管、二极管等元器件外观极度相似，传统 CNN/ViT 分类时极易产生假阳性。
- 背景分布偏移与几何多变：跨厂商/产线板级图像存在光照不均、噪声扰动，导致模型分布偏移，且对旋转/缩放敏感。
- 极端类别不平衡与图异质性：常规贴片器件占比 >85%，核心元器件样本不平衡高达 10 倍以上；同类器件极少聚集，网络呈现强异质图（Heterophilic Graph）特性，常规 GNN 消息平滑机制会发生性能退化。

**Approach 方法**
- 基于 Voronoi 空间细分的平面图拓扑构建：将检测定位的元器件中心作为图节点，自适应划分凸多边形 Cell，仅在相邻 Cell 间建边，精准映射电路物理布局，滤除 90% 以上无信息背景噪声。
- 多模态节点特征融合：结合预训练 ResNet50 视觉嵌入与节点局部/全局图论结构特征，构建位置/旋转不变的归一化空间拓扑特征。
- 异质图神经网络与抗不平衡训练：引入 Ego-Neighbor 嵌入解耦机制（GAT-sep、GT-sep）与动态聚合器（GraphSAGE、ACM-GNN），设计加权 BCE 损失与逆频次采样策略。
- 下游系统级 IC 分割集成（SSR-SAGE Pipeline）：以 GNN 分类器替换传统语义分割架构的纯图像分类器，构建粗分割 + 图拓扑分类筛选的端到端硬件可靠性验证流水线。

**Results 成果**
- 处理 50+ 不同厂商来源的工业板卡图像，构建并开源 Graph-F 与 Graph-W 工业图基准库；单图拓扑构建平均 0.81s ~ 1.49s，单卡 RTX A5000 上 200 epochs 平均 20~50 秒收敛。
- Subset F1-Score 达 0.84 ~ 0.85，显著优于纯视觉 MLP 基准（0.77 / 0.61）；下游 SSR-SAGE 分割 IoU 提升至 0.6619（优于 U-Net 0.5481、DeepLabv3 0.5364、原始 SSRNet 0.5957），Dice 提升至 0.7599，像素错误率下降约 30%。

---

### Satellite Research Centre (SaRC@NTU), Nanyang Technological University (NTU) — Singapore
**PhD Researcher** &nbsp;|&nbsp; 博士研究员
August 2019 – December 2024

#### Public-Transport and Demographic Graph Learning for Urban Site Selection

*First author, published in Remote Sensing (JCR Q1, 2022).*

**Challenge 挑战**
- 多源多模态城市数据割裂：商业零售选址需同时融合宏观人口统计、中观路网拓扑与微观兴趣点（POI），传统统计回归无法处理高维异构非结构化数据。
- 忽略交通网络上的非线性空间溢出效应：传统空间计量模型依赖简单地理欧氏距离，无法刻画公共交通路网引流产生的商业活力空间溢出效应。

**Approach 方法**
- 全岛多源异构数据清洗与 LTSG 基准构建：整合新加坡全岛 55 个规划区组屋人口/房型统计、数百个 MRT/LRT 与公交站点坐标以及餐饮/零售 POI 属性，开源 **Land and Transport Singapore (LTSG)** 数据集。
- 构建公共交通空间拓扑图，以真实通勤时间、换乘便利度与路网连通性建立加权邻接矩阵。
- 部署多层图卷积网络（GCN）联合聚合邻域空间多源特征与拓扑流动信息，端到端预测区域商业吸引力与选址得分。

**Results 成果**
- GCN 模型在均方误差与排序准确率上显著超越 MLP 与传统空间自回归模型；成果发表于 *Remote Sensing*（JCR Q1，一作），LTSG 数据集在 GitHub 开源。

#### Real-time Radar Satellite Image Segmentation Algorithm

*First author, published in Remote Sensing (JCR Q1, 2024) and ICARCV 2024.*

**Challenge 挑战**
- 光学遥感的全天候盲区：高分辨率光学卫星受制于多云、雨雾气象与阴影遮挡，道路特征易被遮挡造成分割断裂与漏检。
- SAR 雷达解译困难与高质量样本匮乏：合成孔径雷达（SAR）具备全天候穿透能力，但图像存在强相干斑噪声与几何失真，高质量标注数据集稀缺。
- 星上边缘算力约束：道路分割算法需面向卫星载荷侧 FPGA 部署，要求模型轻量、低功耗推理。

**Approach 方法**
- 构建首个高分辨率多模态道路基准 **HybridSAR Road Dataset (HSRD)**，整合 SpaceNet-6 真实 SAR/光学影像与 OSM 矢量路网转换的高精掩码。
- 基于微波物理光学与电磁散射原理，依托 GPU 加速的 KAISAR 仿真平台开发端到端合成数据生成流水线，批量模拟高分辨率 SLC 微波遥感图像。
- 设计双流多尺度编码器分别提取光学纹理与 SAR 后向散射特征，引入跨模态注意力融合模块动态调整雷达特征权重，恢复被云层遮挡的道路拓扑连续性。

**Results 成果**
- 在严重云雾与阴影干扰场景下，多模态融合网络在道路分割 IoU 与拓扑连通度上显著超越单模态光学基准；成果发表于 *Remote Sensing*（JCR Q1，一作）与 *ICARCV 2024*（一作）。

---

### Columbia University — United States

#### 3D Astrophysical Fluid Simulation and Spatiotemporal Dynamics Analysis

**Research Assistant** &nbsp;|&nbsp; 研究助理
August 2017 – August 2019

**Challenge 挑战:** Studies fluid-dynamical evolution and turbulent cooling of the circumgalactic medium (CGM)
during galaxy formation, involving multi-terabyte simulation grids with coupled fluid, gravity, and radiative
cooling physics.

**Approach & Results 方法与成果**
- Uses numerical integration, grid interpolation, and statistical-physics modeling to estimate CGM
  temperature-density phases and cooling timescales.
- 基于 Python 开发分布式多 TB 级网格数据处理流水线，执行大规模数值积分与统计物理建模，推导 CGM 介质温度-密度多相态演化与冷却速率的数学估算模型。
- 从复杂多相动态流体模拟中稳健提取相变边界与冷却时标，为星系吸积与恒星形成反馈理论提供了定量数值支撑。

#### High-Dimensional Genomic Signal Extraction with Contrastive PCA

**Research Assistant** &nbsp;|&nbsp; 研究助理
January 2019 – May 2019

**Challenge 挑战:** 生物学家试图通过分析 DNA 寻找精神分裂症发病相关的基因，但数据包含 100,000+ 个 SNP 位点，族裔背景群体结构在传统 PCA 下构成主要方差成分，导致致病遗传关联信号极度微弱。

**Approach 方法:** Applies contrastive PCA and generalized eigenvalue decomposition to separate disease-specific
genomic variation from dominant population-stratification directions, contrasting case and background datasets
in an unsupervised workflow.

**Results 成果:** 成功剥离了混合族裔的全局群体结构混淆，显著提升了低信噪比下疾病相关变异位点的识别灵敏度。

---

### University of Illinois Urbana-Champaign (UIUC) — United States

#### Radio Interferometry and 3D Spectral-Line Kinematics for Galaxy Analysis

**Research Assistant** &nbsp;|&nbsp; 研究助理
May 2015 – May 2017

**Challenge 挑战:** 来自 CARMA、GBT 及 VLA 射电望远镜的星系外分子气体三维谱立方体信号极其微弱，被淹没在接收机热噪声与时变频域基线漂移中。

**Approach 方法:** Uses adaptive smoothing, polynomial baseline fitting, Gaussian line fitting, and moment
analysis to recover velocity fields, dispersions, and rotation curves from spectral cubes across CARMA, GBT, and
VLA observations.

**Results 成果:** 准确刻画了近邻星系分子与电离气体的三维运动学特征；成果作为核心合作者发表于 *The Astrophysical Journal (ApJ)*（2018）。

---

### Independent Project — Customized Multimodal RAG Agent & Automated Analytics System
定制化垂直领域多模态 RAG 智能体与自动化分析系统

**Challenge 挑战**
- A knowledge-domain client's community generated frequent, repetitive questions; without the client's private
  course corpus, a general-purpose model would produce generic, off-target, or hallucinated answers.
- 多模态语料解析与增量维护：客户持续更新视频课程与直播，知识库需自动化摄取与低成本增量更新，而非全量重建。

**Approach 方法**
- 多模态 ETL 自动化数据清洗流水线：自动化爬取抖音/B站长视频课程，进行转码与音频提取，接入 ASR 引擎生成带时间戳的逐字稿，并结合笔记降噪与元数据标注；每日自动收集并分析社群聊天记录生成报告。
- 语义分块、增量向量索引与混合检索：设计语义分块策略构建稠密向量索引，实施 **BM25 + Dense 向量混合检索与重排**，回答严格附带精确来源引用（视频片段秒数/讲义章节），并建立定时增量索引任务。
- Bot 交互层、多轮记忆与成本感知路由：基于 Telegram Webhook 实现群内 @ 提及与私聊交互，配置防刷限流，设计轻量级对话状态机保持多轮追问上下文一致。

**Results 成果**
- 实现了 7×24 小时社群答疑自动化，回答口吻高度契合客户风格，有效承接了 80% 以上的常见课程咨询，知识库自动保持最新状态。

---

## Teaching Experience 教学经历

### Youlu (有录) — Part-time Study-Abroad Tutor
August 2024 – present

- Guided students from high school through graduate level on applications to top universities in the US, UK,
  Australia, Hong Kong, and Singapore.
- Coached personal statements, research proposals, and full-English interview preparation.

### Nanyang Technological University — Teaching Assistant
August 2021 – August 2023

- Guided undergraduate students on machine learning team projects from design through implementation and
  presentation.
- Led weekly discussion and lab sessions connecting theory to practice.
- Developed supplementary teaching materials and programming tutorials, and independently designed a full
  teaching package on NAND-gate circuits.

### University of Illinois Urbana-Champaign — Grader / Undergraduate Teaching Support
Spring 2015

- Prepared grading rubrics and sample solutions; graded homework and quizzes for astronomy coursework.
- Assisted observational lab sessions, including telescope setup and sky tours for the public.

### Sun Yat-sen University — Student Assistant
Spring 2013

- Coordinated guest lecturer visits and logistics for special lecture series.
- Designed and analyzed feedback surveys on guest talks; produced posters and outreach materials.
