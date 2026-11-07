# 03. Promoter and Cis-regulatory Element Analysis / 启动子与顺式作用元件分析

## 中文版

### 目的

描述家族成员启动子区域的预测顺式作用元件组成，并比较不同亚家族、组织或功能分组之间的元件分布差异。

### 输入

同一参考版本的基因组 FASTA、GFF3/GTF、目标基因 ID 和链方向。若有可靠 TSS 注释，应优先以 TSS 为基准；若无 TSS 信息，可将基因起始位点上游 2 kb 作为初始分析窗口，但必须注明这是操作性定义而非所有基因通用的生物学边界。

### 流程

1. 按基因链方向提取上游序列。正链和负链的上游方向必须正确处理。
2. 检查启动子是否超出染色体边界，是否与相邻基因、上游基因或其他注释区间重叠。对重叠序列记录处理方式，不应无说明地截断或重复计算。
3. 使用 PlantCARE、PLACE、PlantPAN 或其他合适数据库预测顺式作用元件，记录数据库版本、检索参数和元件定义。
4. 将元件按光响应、激素响应、胁迫响应、生长发育等类别归类。类别映射应有明确依据，不能仅凭名称猜测。
5. 分别统计元件总次数、含有某元件的启动子数量、每个启动子的元件数量，以及按长度标准化的频率。
6. 若进行组间统计或富集分析，定义适当背景启动子集合；尽量保证背景与目标集合采用相同提取规则，并考虑启动子长度和 GC 含量差异。
7. 根据数据分布选择统计检验，并对多元件、多组比较进行 FDR 等多重检验校正。

### 质量控制与解释边界

- 预测到元件不证明该元件在目标组织或处理条件下具有调控活性。
- 原始计数、启动子阳性比例和每 kb 频率是不同指标，不应混为一谈。
- 若启动子长度不一致，直接比较原始元件计数可能产生长度偏倚。
- 数据库中同一序列模式可能对应多个元件注释，需检查重复命中和类别定义。
- 统计显著性不等同于生物学效应；报告效应量和样本数。
- 需要功能结论时，应结合报告基因、缺失分析、定点突变或其他实验验证。

### 输出

启动子 FASTA、元件注释明细、基因 × 元件矩阵、类别统计表、统计检验结果、启动子分布图和热图。

## English Version

### Objective

Describe predicted cis-regulatory element composition in family-member promoters and compare element distributions among subfamilies, tissues, or functional groups.

### Inputs

Genome FASTA, GFF3/GTF, target gene IDs, and strand information from the same reference release. Use reliable TSS annotations when available. If TSS data are unavailable, an upstream 2-kb interval from the annotated gene start may be used as an initial operational window, but it must not be presented as a universal biological promoter boundary.

### Workflow

1. Extract upstream sequences according to gene strand. Handle upstream orientation correctly for both positive- and negative-strand genes.
2. Check whether a promoter extends beyond a chromosome boundary or overlaps neighboring genes, upstream genes, or other annotated intervals. Document how overlaps are handled; do not silently truncate or double-count sequences.
3. Predict cis-elements using PlantCARE, PLACE, PlantPAN, or another suitable resource. Record database versions, search settings, and element definitions.
4. Group elements into categories such as light-responsive, hormone-responsive, stress-responsive, and development-related elements. Use explicit classification rules rather than inferring categories from names alone.
5. Report total element counts, the number of promoters containing each element, per-promoter counts, and length-normalized frequencies separately.
6. For group comparisons or enrichment tests, define an appropriate background promoter set. Apply the same extraction rules to foreground and background and consider differences in promoter length and GC content.
7. Select statistical tests according to data distributions and apply multiple-testing correction, such as FDR, across elements and group comparisons.

### Quality Control and Interpretation Limits

- A predicted element does not demonstrate regulatory activity in the target tissue or treatment.
- Raw counts, promoter prevalence, and counts per kilobase are different metrics and must not be conflated.
- Comparing raw counts across promoters of different lengths may introduce length bias.
- The same sequence pattern may map to multiple database annotations; inspect duplicate hits and category definitions.
- Statistical significance is not equivalent to biological effect. Report effect sizes and sample sizes.
- Functional claims require supporting experiments such as reporter assays, deletion analysis, site-directed mutagenesis, or other appropriate validation.

### Outputs

Promoter FASTA files, detailed element annotations, gene-by-element matrix, category summary tables, statistical results, promoter maps, and heatmaps.
