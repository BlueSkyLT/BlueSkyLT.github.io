<div class="cv-entry inst-ntu">
  <div class="entry-header">
    <span class="entry-title">ASCAD: AES Side-Channel Attack and Leakage Detection</span>
    <span class="entry-affil">ISRL@NTU</span>
    <span class="entry-period">Dec 2024 – present</span>
  </div>
  <div class="entry-tags"><span class="tag">1D-CNN</span><span class="tag">side-channel analysis</span><span class="tag">physics-informed loss</span></div>
  <div class="entry-desc"><strong>Problem:</strong> Masked AES-128 hardware leaks power/EM side-channel information, but traces are tens of thousands of samples long, low-SNR, and phase-shifted by clock jitter, so classical DPA/CPA fails.<br>
  <strong>Method:</strong> Built a high-throughput 1D preprocessing pipeline (clock-prior point-of-interest slicing + PCA) and multi-scale 1D-CNN/MLP models with a physics-based cross-correlation loss derived from circuit power theory to guide point-of-interest discovery.<br>
  <strong>Result:</strong> Evaluated on the standard ASCAD dataset via guessing entropy and success rate; reduced the number of traces required to fully recover a 16-byte key by several-fold, quantifying the strength of the hardware's masking defense.</div>
</div>

<div class="cv-entry inst-ntu">
  <div class="entry-header">
    <span class="entry-title">Network Anomaly and Cyberattack Detection in Communication Networks</span>
    <span class="entry-affil">CISS@NTU</span>
    <span class="entry-period">Jun 2025 – present</span>
  </div>
  <div class="entry-tags"><span class="tag">dynamic bipartite graphs</span><span class="tag">graph time-series</span><span class="tag">GNN</span></div>
  <div class="entry-desc"><strong>Problem:</strong> Only partial, non-synchronized observations of message broadcasting are available on a dynamic bipartite network, and attacks must be detected and localized as early as possible despite varying attack patterns and scarce data.<br>
  <strong>Method:</strong> Simulated the network's broadcasting structure and observations, converted bipartite graphs into standard graphs, patched non-synchronized series to align with time-series methods, and used flexible GNNs with a calibrated per-node activity baseline for real-time alarms.<br>
  <strong>Result:</strong> Detects various attack types on graphs with 50+ nodes with only half of observations available, enabling day-level anomaly monitoring with node- and link-level localization.</div>
</div>

<div class="cv-entry inst-ntu">
  <div class="entry-header">
    <span class="entry-title">Statistically Guaranteed Disease Source Detection in Social Networks</span>
    <span class="entry-affil">CISS@NTU</span>
    <span class="entry-period">Jun 2025 – present</span>
  </div>
  <div class="entry-tags"><span class="tag">conformal risk control</span><span class="tag">GNN</span><span class="tag">AAAI 2026</span></div>
  <div class="entry-desc"><strong>Problem:</strong> Source localization from a single infection/rumor snapshot is a severely ill-posed inverse problem, and classical diffusion models offer no statistical confidence guarantee.<br>
  <strong>Method:</strong> A spatial-temporal GNN scores each node's non-conformity to being an initial source; conformal risk control turns this into a candidate-set prediction problem with a distribution-free, finite-sample recall guarantee requiring only data exchangeability.<br>
  <strong>Result:</strong> Achieved 90% and 95% nominal recall with compact prediction sets on synthetic and real social/contact networks. Published at <strong>AAAI 2026</strong> (CCF-A, 3rd author); benchmark code open-sourced.</div>
</div>

<div class="cv-entry inst-ntu">
  <div class="entry-header">
    <span class="entry-title">Component Detection and Classification on PCB Images with Location-Encoded Graphs</span>
    <span class="entry-affil">TL@NTU</span>
    <span class="entry-period">Dec 2024 – May 2025</span>
  </div>
  <div class="entry-tags"><span class="tag">Voronoi planar graphs</span><span class="tag">heterophilic GNN</span><span class="tag">weighted BCE</span></div>
  <div class="entry-desc"><strong>Problem:</strong> ICs, transistors, and diodes look nearly identical on industrial PCB images; backgrounds vary across vendors; and common components outnumber rare ones by 10:1, with same-class parts rarely clustering (heterophilic graph), causing vanilla GNNs to degrade.<br>
  <strong>Method:</strong> Built adaptive planar graphs via Voronoi tessellation of detected component centroids, fused ResNet50 visual features with local/global graph structure, and trained decoupled heterophilic GNNs (GAT-sep, GT-sep, ACM-GNN) with weighted BCE loss; integrated the classifier into a downstream IC-segmentation pipeline (SSR-SAGE).<br>
  <strong>Result:</strong> Released the open Graph-F/Graph-W benchmarks (50+ vendors); Subset F1 of 0.84–0.85 vs. 0.61–0.77 for vision-only baselines; downstream IC-segmentation IoU improved from 0.60 to 0.66 with ~30% lower pixel error rate.</div>
</div>

<div class="cv-entry inst-ntu">
  <div class="entry-header">
    <span class="entry-title">Public-Transport and Demographic Graph Learning for Urban Site Selection</span>
    <span class="entry-affil">SaRC@NTU</span>
    <span class="entry-period">Aug 2019 – Dec 2024</span>
  </div>
  <div class="entry-tags"><span class="tag">graph convolutional networks</span><span class="tag">spatial spillover</span><span class="tag">Remote Sensing 2022</span></div>
  <div class="entry-desc"><strong>Problem:</strong> Retail site selection needs population, transit topology, and points-of-interest together, but simple Euclidean spatial models miss the nonlinear commercial spillover effects created by public transit.<br>
  <strong>Method:</strong> Built and released the open <strong>Land and Transport Singapore (LTSG)</strong> benchmark (HDB demographics, MRT/bus stops, POIs), constructed a transit-weighted spatial graph, and trained a multi-layer GCN to predict commercial attractiveness and site scores end-to-end.<br>
  <strong>Result:</strong> Lower MSE and better ranking accuracy than MLP and spatial autoregression baselines. Published in <em>Remote Sensing</em> (JCR Q1, 2022, first author); LTSG open-sourced.</div>
</div>

<div class="cv-entry inst-ntu">
  <div class="entry-header">
    <span class="entry-title">Real-Time Radar Satellite Image Segmentation Algorithm</span>
    <span class="entry-affil">SaRC@NTU</span>
    <span class="entry-period">Aug 2019 – Dec 2024</span>
  </div>
  <div class="entry-tags"><span class="tag">optical–SAR fusion</span><span class="tag">physics-based simulation</span><span class="tag">Remote Sensing 2024</span></div>
  <div class="entry-desc"><strong>Problem:</strong> Optical satellite road segmentation fails under cloud/shadow cover; SAR is all-weather but noisy and scarce in labeled data; onboard FPGA deployment rules out GPU-scale models.<br>
  <strong>Method:</strong> Released the <strong>HybridSAR Road Dataset (HSRD)</strong> combining SpaceNet-6 SAR/optical imagery with OSM-derived masks, built a GPU-accelerated physical-optics simulator (KAISAR) to generate synthetic SLC data, and designed a dual-stream encoder with cross-modal attention to fuse optical and radar features.<br>
  <strong>Result:</strong> Improved road IoU and topological connectivity over optical-only baselines under heavy cloud/shadow. Published in <em>Remote Sensing</em> (JCR Q1, 2024, first author) and <em>ICARCV 2024</em> (first author).</div>
</div>

<div class="cv-entry inst-other">
  <div class="entry-header">
    <span class="entry-title">Customized Multimodal RAG Agent &amp; Automated Analytics System</span>
    <span class="entry-affil">Independent Project</span>
    <span class="entry-period">Jan 2026 – Jun 2026</span>
  </div>
  <div class="entry-tags"><span class="tag">LLM agent</span><span class="tag">hybrid retrieval</span><span class="tag">multimodal ETL</span></div>
  <div class="entry-desc"><strong>Problem:</strong> A knowledge-domain client's community needed answers grounded in a private, continuously updated video/course corpus without generic or hallucinated responses.<br>
  <strong>Method:</strong> Built an automated ETL pipeline (video scraping, ASR transcription, note ingestion), semantic chunking with BM25 + dense hybrid retrieval and reranking, source-grounded answer generation, and a Telegram bot with per-user conversation state and incremental index updates.<br>
  <strong>Result:</strong> Delivered 24/7 automated community Q&amp;A covering 80%+ of common inquiries, with the knowledge base kept continuously up to date.</div>
</div>

<div class="cv-entry inst-cu">
  <div class="entry-header">
    <span class="entry-title">3D Astrophysical Fluid Simulation and Spatiotemporal Dynamics Analysis</span>
    <span class="entry-affil">Columbia Astrophysics Laboratory</span>
    <span class="entry-period">Aug 2017 – Aug 2019</span>
  </div>
  <div class="entry-tags"><span class="tag">distributed pipelines</span><span class="tag">numerical simulation</span></div>
  <div class="entry-desc"><strong>Problem:</strong> Studying circumgalactic-medium fluid dynamics and cooling during galaxy formation requires processing multi-terabyte simulation grids with coupled fluid, gravity, and radiative-cooling physics.<br>
  <strong>Method:</strong> Built a distributed Python pipeline for multi-TB grid processing using numerical integration, grid interpolation, and statistical-physics modeling of temperature-density phases.<br>
  <strong>Result:</strong> Robustly extracted phase boundaries and cooling timescales, providing quantitative support for galaxy-accretion and star-formation research.</div>
</div>

<div class="cv-entry inst-cu">
  <div class="entry-header">
    <span class="entry-title">High-Dimensional Genomic Signal Extraction with Contrastive PCA</span>
    <span class="entry-affil">Department of Computer Science, Columbia University</span>
    <span class="entry-period">Jan 2019 – May 2019</span>
  </div>
  <div class="entry-tags"><span class="tag">contrastive PCA</span><span class="tag">genomics</span></div>
  <div class="entry-desc"><strong>Problem:</strong> Identifying schizophrenia-associated genes from 100,000+ SNPs is confounded by population-stratification signal dominating traditional PCA variance.<br>
  <strong>Method:</strong> Applied contrastive PCA and generalized eigenvalue decomposition to separate disease-specific variation from background population structure in an unsupervised case/control workflow.<br>
  <strong>Result:</strong> Removed ancestry-related confounding and improved sensitivity for detecting low-signal disease-associated variants.</div>
</div>

<div class="cv-entry inst-uiuc">
  <div class="entry-header">
    <span class="entry-title">Radio Interferometry and 3D Spectral-Line Kinematics for Galaxy Analysis</span>
    <span class="entry-affil">Department of Astronomy, UIUC</span>
    <span class="entry-period">May 2015 – May 2017</span>
  </div>
  <div class="entry-tags"><span class="tag">signal processing</span><span class="tag">ApJ 2018</span></div>
  <div class="entry-desc"><strong>Problem:</strong> Molecular gas spectral cubes from CARMA/GBT/VLA are extremely weak signals buried in receiver noise and time-varying baseline drift.<br>
  <strong>Method:</strong> Developed adaptive smoothing, polynomial baseline fitting, Gaussian line fitting, and moment analysis to recover velocity fields, dispersions, and rotation curves.<br>
  <strong>Result:</strong> Accurately characterized 3D kinematics of nearby galaxies; contributed as a core collaborator to a publication in <em>The Astrophysical Journal (ApJ)</em>, 2018.</div>
</div>
