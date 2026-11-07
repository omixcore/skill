# 11. Gene Structure Analysis / 基因结构分析

## 中文版

### 目的

比较家族成员的外显子、内含子、UTR 和 CDS 结构，分析不同亚家族之间的基因结构保守性和差异。

### 输入与工具

使用与参考基因组匹配的 GFF3/GTF、基因组 FASTA、CDS 和转录本注释。可使用 TBtools、GSDS、Gene Structure Display Server 或 R/Python 绘图流程。

### 流程

1. 根据 gene、transcript、exon、CDS 和 UTR 注释建立层级关系。
2. 明确每个基因用于展示的转录本。默认代表转录本策略应与家族成员鉴定阶段一致；若研究剪接差异，则保留多个转录本。
3. 提取外显子数、内含子数、基因长度、CDS 长度、UTR 长度和内含子长度。
4. 检查注释中是否存在 exon/CDS 不一致、缺失 UTR、异常短外显子或转录本坐标错误。
5. 将基因结构图与进化树或亚家族分组对齐，比较结构模式。
6. 对多物种分析，考虑不同注释项目对 UTR 和转录本的注释完整度差异。

### 质量控制与解释边界

- GFF3 的层级和 Parent ID 必须正确解析。
- 基因结构差异可能来自注释流程差异，而不一定代表真实进化事件。
- 不同转录本的 exon 数量不可直接混作同一基因的唯一结构。
- 图中坐标、比例尺和正负链方向应准确。
- 结构保守性可支持进化解释，但不能单独证明功能相同。

### 输出

基因结构统计表、转录本映射表、exon–intron 图和与进化树整合的结构图。

## English Version

### Objective

Compare exon, intron, UTR, and CDS structures among family members and assess structural conservation or divergence among subfamilies.

### Inputs and Tools

Use GFF3/GTF annotations, genome FASTA, CDS, and transcript annotations that match the same reference assembly. Suitable tools include TBtools, GSDS, Gene Structure Display Server, or custom R/Python workflows.

### Workflow

1. Parse gene, transcript, exon, CDS, and UTR relationships from the annotation hierarchy.
2. Define the transcript used for each gene. Keep the representative-transcript strategy consistent with member identification; retain multiple transcripts when splicing variation is the research focus.
3. Extract exon count, intron count, gene length, CDS length, UTR length, and intron lengths.
4. Check for inconsistencies between exon and CDS annotations, missing UTRs, unusually short exons, and incorrect transcript coordinates.
5. Align gene-structure plots with the phylogenetic tree or subfamily groups to compare structural patterns.
6. For multi-species analyses, consider differences in annotation completeness for UTRs and transcript isoforms.

### Quality Control and Interpretation Limits

- Parse GFF3 hierarchy and Parent IDs correctly.
- Structural differences may arise from annotation pipelines rather than genuine evolutionary events.
- Exon counts from different transcript isoforms must not be treated as one unique structure per gene.
- Coordinates, scale bars, and strand orientation must be accurate.
- Structural conservation can support evolutionary interpretation but does not by itself establish identical function.

### Outputs

Gene-structure summary table, transcript mapping table, exon–intron plots, and integrated phylogeny–structure figures.
