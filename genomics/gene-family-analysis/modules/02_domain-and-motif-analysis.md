# 02. Domain and Motif Analysis / 保守结构域与 Motif 分析

## 中文版

### 目的

比较家族蛋白的保守结构域、短保守基序及其排列，识别亚家族间的结构差异和可能的功能分化线索。

### 输入与工具

使用经过质控的蛋白质 FASTA 和成员注释表。结构域分析可采用 Pfam、InterProScan、CDD 或 SMART；Motif 发现可采用 MEME Suite。应记录数据库和软件版本。

### 流程

1. 运行结构域搜索，记录结构域名称、数据库编号、起止位置、得分和显著性指标。
2. 复核目标家族定义所依赖的核心结构域，区分完整结构域、部分结构域和可疑命中。
3. 使用 MEME 等工具识别保守 Motif。Motif 数量、宽度和分布设置应依据家族规模及序列特征确定，并记录参数。
4. 将 Motif 编号、氨基酸序列、长度和蛋白位置整理成表格；必要时生成 sequence logo。
5. 将结构域和 Motif 架构与进化树并列展示，检查亚家族内保守性和亚家族间差异。
6. 若比较多个物种，应使用一致的蛋白代表序列策略和可比的 Motif 搜索设置。

### 质量控制与解释边界

- Motif 是序列模式，不等同于已验证的功能位点。
- 不同长度蛋白的 Motif 数量差异可能受序列长度和算法设置影响。
- 结构域缺失可能来自真实结构变异，也可能来自基因模型不完整、序列截短或组装缺口；应先复核。
- 不应只依据一个短 Motif 对蛋白进行家族归类。
- 图中结构域坐标应与蛋白序列长度一致。

### 输出

结构域注释表、Motif 序列与位置表、sequence logo、蛋白结构架构图，以及与进化树对应的整合图。

## English Version

### Objective

Compare conserved protein domains, short sequence motifs, and their arrangements to identify structural differences among subfamilies and potential clues to functional diversification.

### Inputs and Tools

Use quality-controlled protein FASTA files and member metadata. Domain analysis can use Pfam, InterProScan, CDD, or SMART; motif discovery can use MEME Suite. Record database and software versions.

### Workflow

1. Run domain searches and record domain names, database accessions, coordinates, scores, and significance metrics.
2. Validate the core domain that defines the family. Distinguish complete domains, partial domains, and questionable matches.
3. Identify conserved motifs with tools such as MEME. Choose motif number, width, and distribution settings according to family size and sequence characteristics, and record all parameters.
4. Compile motif identifiers, amino-acid sequences, lengths, and protein coordinates; generate sequence logos when useful.
5. Compare domain and motif architectures alongside the phylogenetic tree to assess conservation within and differences among subfamilies.
6. For multi-species comparisons, use a consistent representative-isoform strategy and comparable motif-search settings.

### Quality Control and Interpretation Limits

- A motif is a sequence pattern, not a functionally validated site.
- Differences in motif counts among proteins of different lengths may be influenced by sequence length and algorithm settings.
- Domain absence may reflect genuine structural variation, incomplete gene models, truncated sequences, or assembly gaps; investigate before interpreting it biologically.
- Do not classify a protein solely on the basis of one short motif.
- Domain coordinates in figures must match the corresponding protein lengths.

### Outputs

Domain-annotation table, motif sequence and coordinate table, sequence logos, protein architecture plots, and integrated figures aligned with the phylogenetic tree.
