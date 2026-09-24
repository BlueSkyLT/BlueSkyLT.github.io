<div class="cv-entry inst-ntu">
  <div class="entry-header">
    <span class="entry-title">ASCAD：AES 侧信道攻击与泄露检测</span>
    <span class="entry-affil">ISRL@NTU</span>
    <span class="entry-period">2024 年 12 月 – 至今</span>
  </div>
  <div class="entry-tags"><span class="tag">1D-CNN</span><span class="tag">侧信道分析</span><span class="tag">物理约束损失</span></div>
  <div class="entry-desc"><strong>挑战：</strong>带掩码防御的 AES-128 芯片存在功耗/电磁侧信道泄露，但功耗曲线单条长达数万采样点、信噪比极低，且存在时钟抖动导致的相位漂移，传统 DPA/CPA 完全失效。<br>
  <strong>方法：</strong>构建高吞吐 1D 预处理流水线（结合时钟先验的兴趣点切片 + PCA），设计多尺度 1D-CNN/MLP 模型，并引入基于电路功耗物理理论的互相关损失函数指导兴趣点定位。<br>
  <strong>成果：</strong>基于标准 ASCAD 数据集以猜测熵与攻击成功率评估，将完整恢复 16 字节密钥所需的功耗曲线条数降低数倍，量化评估了硬件掩码防御强度。</div>
</div>

<div class="cv-entry inst-ntu">
  <div class="entry-header">
    <span class="entry-title">通信网络异常与网络攻击检测</span>
    <span class="entry-affil">CISS@NTU</span>
    <span class="entry-period">2025 年 6 月 – 至今</span>
  </div>
  <div class="entry-tags"><span class="tag">动态二分图</span><span class="tag">图时间序列</span><span class="tag">GNN</span></div>
  <div class="entry-desc"><strong>挑战：</strong>动态二分图网络中仅能获取部分、非同步的消息广播观测，且攻击模式多变、数据稀缺，需尽早检测并定位攻击。<br>
  <strong>方法：</strong>模拟网络广播结构与观测过程，将二分图转化为普通图，通过分块处理使非同步时间序列可与其他时序方法对齐，并使用灵活的 GNN 结合节点级动态基线进行实时告警。<br>
  <strong>成果：</strong>在仅有一半观测的 50+ 节点图上可检测多种攻击类型，实现天级异常监控与节点/链路级定位。</div>
</div>

<div class="cv-entry inst-ntu">
  <div class="entry-header">
    <span class="entry-title">社交网络中具有统计保证的疾病信源检测</span>
    <span class="entry-affil">CISS@NTU</span>
    <span class="entry-period">2025 年 6 月 – 至今</span>
  </div>
  <div class="entry-tags"><span class="tag">保形风险控制</span><span class="tag">GNN</span><span class="tag">AAAI 2026</span></div>
  <div class="entry-desc"><strong>挑战：</strong>从单次感染/谣言快照定位信源属于极度病态的逆问题，传统扩散模型无法给出统计置信度保证。<br>
  <strong>方法：</strong>使用 Spatial-Temporal GNN 为每个节点打出非一致性评分，结合保形风险控制将定位问题转化为候选集合预测问题，仅需数据可交换性假设即可获得有限样本下的分布无关召回率保证。<br>
  <strong>成果：</strong>在合成拓扑与真实社交/接触网络上分别达到 90%、95% 的名义召回率，且预测集紧致；成果发表于 <strong>AAAI 2026</strong>（CCF-A 类，三作），并开源基准算法库。</div>
</div>

<div class="cv-entry inst-ntu">
  <div class="entry-header">
    <span class="entry-title">基于位置编码图的 PCB 元器件检测与分类</span>
    <span class="entry-affil">TL@NTU</span>
    <span class="entry-period">2024 年 12 月 – 2025 年 5 月</span>
  </div>
  <div class="entry-tags"><span class="tag">Voronoi 平面图</span><span class="tag">异质图 GNN</span><span class="tag">加权 BCE</span></div>
  <div class="entry-desc"><strong>挑战：</strong>工业 PCB 图像中 IC、晶体管、二极管外观高度相似，跨厂商背景差异大，常规元器件与稀有元器件比例高达 10:1，且同类元件很少聚集（异质图），常规 GNN 性能退化。<br>
  <strong>方法：</strong>基于检测到的元器件中心构建 Voronoi 平面图拓扑，融合 ResNet50 视觉特征与图结构特征，训练解耦异质图模型（GAT-sep、GT-sep、ACM-GNN）并使用加权 BCE 损失，最终将分类器集成到下游 IC 分割流水线（SSR-SAGE）中。<br>
  <strong>成果：</strong>开源 Graph-F/Graph-W 基准库（覆盖 50+ 厂商）；Subset F1 达 0.84~0.85，显著优于纯视觉基线（0.61~0.77）；下游 IC 分割 IoU 从 0.60 提升至 0.66，像素错误率下降约 30%。</div>
</div>

<div class="cv-entry inst-ntu">
  <div class="entry-header">
    <span class="entry-title">面向城市选址的公共交通与人口图学习</span>
    <span class="entry-affil">SaRC@NTU</span>
    <span class="entry-period">2019 年 8 月 – 2024 年 12 月</span>
  </div>
  <div class="entry-tags"><span class="tag">图卷积网络</span><span class="tag">空间溢出效应</span><span class="tag">Remote Sensing 2022</span></div>
  <div class="entry-desc"><strong>挑战：</strong>零售选址需要同时融合人口统计、交通路网拓扑与兴趣点信息，而传统欧氏空间模型无法刻画公共交通带来的非线性商业溢出效应。<br>
  <strong>方法：</strong>构建并开源 <strong>Land and Transport Singapore (LTSG)</strong> 数据集（组屋人口、地铁/公交站点、POI），建立交通加权空间图，训练多层 GCN 端到端预测商业吸引力与选址得分。<br>
  <strong>成果：</strong>均方误差与排序准确率均优于 MLP 与空间自回归基线；成果发表于《Remote Sensing》（JCR Q1，2022，一作），LTSG 数据集已开源。</div>
</div>

<div class="cv-entry inst-ntu">
  <div class="entry-header">
    <span class="entry-title">实时雷达卫星图像分割算法</span>
    <span class="entry-affil">SaRC@NTU</span>
    <span class="entry-period">2019 年 8 月 – 2024 年 12 月</span>
  </div>
  <div class="entry-tags"><span class="tag">光学-SAR 融合</span><span class="tag">物理仿真</span><span class="tag">Remote Sensing 2024</span></div>
  <div class="entry-desc"><strong>挑战：</strong>光学卫星道路分割在多云/阴影下失效；SAR 具备全天候能力但噪声强、标注数据稀缺；星上 FPGA 部署排除了桌面级 GPU 方案。<br>
  <strong>方法：</strong>发布 <strong>HybridSAR Road Dataset (HSRD)</strong>（融合 SpaceNet-6 SAR/光学影像与 OSM 掩码），基于 GPU 加速物理光学仿真平台 KAISAR 生成合成 SLC 数据，设计带跨模态注意力的双流编码器融合光学与雷达特征。<br>
  <strong>成果：</strong>在严重云雾遮挡场景下，道路 IoU 与拓扑连通度显著优于纯光学基线；成果发表于《Remote Sensing》（JCR Q1，2024，一作）与 *ICARCV 2024*（一作）。</div>
</div>

<div class="cv-entry inst-other">
  <div class="entry-header">
    <span class="entry-title">定制化垂直领域多模态 RAG 智能体与自动化分析系统</span>
    <span class="entry-affil">独立项目</span>
    <span class="entry-period">2026 年 1 月 – 2026 年 6 月</span>
  </div>
  <div class="entry-tags"><span class="tag">LLM 智能体</span><span class="tag">混合检索</span><span class="tag">多模态 ETL</span></div>
  <div class="entry-desc"><strong>挑战：</strong>客户社区需要基于私有课程语料的高保真问答，且语料持续更新，通用大模型容易给出泛化或幻觉回答。<br>
  <strong>方法：</strong>构建自动化 ETL 流水线（视频抓取、ASR 转写、笔记摄取），采用语义分块结合 BM25 + 稠密向量的混合检索与重排，生成附带来源引用的回答，并搭建带用户级对话状态与增量索引更新的 Telegram 机器人。<br>
  <strong>成果：</strong>实现 7×24 小时社群自动问答，承接 80% 以上常见咨询，知识库持续保持最新。</div>
</div>

<div class="cv-entry inst-cu">
  <div class="entry-header">
    <span class="entry-title">三维天体物理流体模拟与时空动力学分析</span>
    <span class="entry-affil">哥伦比亚天体物理实验室</span>
    <span class="entry-period">2017 年 8 月 – 2019 年 8 月</span>
  </div>
  <div class="entry-tags"><span class="tag">分布式流水线</span><span class="tag">数值模拟</span></div>
  <div class="entry-desc"><strong>挑战：</strong>研究星系形成过程中环星系介质的流体动力学与冷却机制，需处理多 TB 级、涉及流体-引力-辐射冷却耦合的模拟网格数据。<br>
  <strong>方法：</strong>基于 Python 构建分布式多 TB 网格处理流水线，结合数值积分、网格插值与统计物理建模估算温度-密度相态。<br>
  <strong>成果：</strong>稳健提取相变边界与冷却时标，为星系吸积与恒星形成研究提供了定量支撑。</div>
</div>

<div class="cv-entry inst-cu">
  <div class="entry-header">
    <span class="entry-title">基于对比主成分分析的高维基因组信号提取</span>
    <span class="entry-affil">哥伦比亚大学计算机科学系</span>
    <span class="entry-period">2019 年 1 月 – 2019 年 5 月</span>
  </div>
  <div class="entry-tags"><span class="tag">对比 PCA</span><span class="tag">基因组学</span></div>
  <div class="entry-desc"><strong>挑战：</strong>从 100,000+ SNP 位点中识别精神分裂症相关基因，传统 PCA 下族裔背景群体结构构成主要方差成分，掩盖了致病信号。<br>
  <strong>方法：</strong>应用对比 PCA 与广义特征值分解，在病例组与背景组之间的无监督流程中分离疾病特异性变异与群体结构方差。<br>
  <strong>成果：</strong>剥离了族裔混杂因素，显著提升低信噪比下致病变异位点的识别灵敏度。</div>
</div>

<div class="cv-entry inst-uiuc">
  <div class="entry-header">
    <span class="entry-title">射电干涉测量与星系三维谱线运动学分析</span>
    <span class="entry-affil">UIUC 天文学系</span>
    <span class="entry-period">2015 年 5 月 – 2017 年 5 月</span>
  </div>
  <div class="entry-tags"><span class="tag">信号处理</span><span class="tag">ApJ 2018</span></div>
  <div class="entry-desc"><strong>挑战：</strong>来自 CARMA/GBT/VLA 的分子气体谱立方体信号极其微弱，淹没在接收机噪声与时变基线漂移中。<br>
  <strong>方法：</strong>开发自适应平滑、多项式基线拟合、高斯谱线拟合与矩分析，恢复速度场、弥散剖面与旋转曲线。<br>
  <strong>成果：</strong>准确刻画了近邻星系的三维运动学特征，作为核心合作者发表于《The Astrophysical Journal (ApJ)》，2018 年。</div>
</div>
