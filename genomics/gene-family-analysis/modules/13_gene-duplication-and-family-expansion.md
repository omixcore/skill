# 13. Gene Duplication and Family Expansion / 基因复制与家族扩张分析

## 中文版

### 目的

分析基因家族成员增加、减少和复制类型，探索家族在不同谱系中的演化历史，并区分基因组复制、局部复制、基因丢失和注释差异的影响。

### 输入与工具

需要多个物种的可靠家族成员清单、蛋白质和 CDS 序列、基因组注释、物种系统发育树及共线性结果。可结合 OrthoFinder、MCScanX、WGDI、CAFE 或其他适用工具。

### 分析流程

1. **统一家族鉴定**：对各物种使用一致的结构域和序列鉴定策略，记录每个物种的基因组和注释质量。
2. **建立同源群**：结合全蛋白同源聚类、基因树和共线性关系识别 orthogroup，并区分可能的直系同源和旁系同源。
3. **复制类型分类**：结合基因组位置和共线性证据区分 tandem、proximal、segmental/WGD、dispersed 等类型。使用的软件定义和阈值必须记录。
4. **家族成员数比较**：按物种和亚家族统计成员数量，同时报告基因组大小、注释完整性和成员鉴定证据。
5. **扩张/收缩检验**：如研究问题需要，可将家族计数映射到物种树并使用 CAFE 等 birth–death 模型进行检验；明确模型、树、时间校准、误差和参数。
6. **整合 Ks 和共线性**：利用可靠的复制基因对、Ks 分布和共线性区块补充复制历史证据，但避免重复计算或把不可靠的 Ks 值用于定年。
7. **解释谱系特异变化**：结合物种取样、基因丢失、基因组复制和注释差异，提出保守且可验证的解释。

### 质量控制与解释边界

- 家族成员数量差异本身不能证明扩张或收缩。
- 注释质量差异、基因组组装缺口、基因模型碎片化和不同筛选阈值会造成假性数量差异。
- tandem、segmental 和 WGD 的分类应依据明确规则，不能只凭图形位置判断。
- CAFE 等模型依赖物种树、家族计数和模型假设；需检查误差和过度离散等问题。
- 复制基因不一定保留原功能，也不一定发生功能分化。
- 家族扩张结论应与表达、结构、选择压力或功能证据交叉验证。

### 输出

物种 × 家族成员数矩阵、orthogroup 表、复制类型表、共线性证据、Ks 结果、扩张/收缩模型结果和整合进化图。

## English Version

### Objective

Analyze gene-family gains, losses, and duplication classes to investigate family evolution across lineages while distinguishing genome duplication, local duplication, gene loss, and annotation differences.

### Inputs and Tools

Use reliable family-member lists from multiple species, protein and CDS sequences, genome annotations, a species phylogeny, and synteny results. Tools may include OrthoFinder, MCScanX, WGDI, CAFE, or other suitable software.

### Workflow

1. **Harmonize family identification:** apply consistent domain and sequence-identification criteria across species and record genome and annotation quality for each species.
2. **Build orthogroups:** integrate whole-proteome clustering, gene trees, and synteny to identify orthogroups and distinguish candidate orthologs from paralogs.
3. **Classify duplication types:** use genomic positions and synteny evidence to classify tandem, proximal, segmental/WGD, and dispersed duplications. Record software definitions and thresholds.
4. **Compare family sizes:** summarize member counts by species and subfamily while reporting genome size, annotation completeness, and member-identification evidence.
5. **Test expansion or contraction:** when required, map family counts onto a species tree and use a birth–death model such as CAFE. Specify the model, tree, time calibration, error treatment, and parameters.
6. **Integrate Ks and synteny:** use reliable duplicated pairs, Ks distributions, and syntenic blocks as complementary evidence, avoiding double-counting and unreliable Ks-based dating.
7. **Interpret lineage-specific changes:** account for species sampling, gene loss, genome duplication, and annotation differences before proposing evolutionary explanations.

### Quality Control and Interpretation Limits

- Differences in family-member counts alone do not prove expansion or contraction.
- Differences in annotation quality, assembly gaps, fragmented gene models, and inconsistent filtering thresholds can create apparent count differences.
- Classify tandem, segmental, and WGD duplications using explicit rules rather than visual position alone.
- Models such as CAFE depend on the species tree, family counts, and model assumptions; inspect error and overdispersion issues.
- Duplicated genes do not necessarily retain the original function or undergo functional divergence.
- Cross-check expansion claims with expression, structure, selection-pressure, or functional evidence.

### Outputs

Species-by-family count matrix, orthogroup table, duplication-class table, synteny evidence, Ks results, expansion/contraction model results, and integrated evolutionary figures.
