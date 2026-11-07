---
name: gene-family-analysis
description: A reproducible, plant-focused workflow for identifying gene-family members and analyzing phylogeny, protein domains and motifs, promoters, synteny, chromosome locations, Ka/Ks, GO, PPI, expression, gene structure, protein properties, gene-family expansion, and qRT-PCR validation.
---

# Gene Family Analysis / 基因家族分析

## 中文版

### 目的与适用范围

本 Skill 用于植物基因家族研究，覆盖从家族成员鉴定、序列与结构分析、物种间比较、基因组演化、功能注释、表达分析到 qRT-PCR 验证的完整流程。可用于转录因子家族、代谢酶家族、光合作用相关基因家族及其他具有明确保守结构域的基因家族。

本 Skill 是可组合的分析框架，不要求每篇论文机械执行全部模块。应根据科学问题、数据质量和研究设计选择分析内容，并明确区分计算预测、统计关联和实验验证。

### 总体流程

1. **基础鉴定与数据质控**：统一基因组和注释版本，使用 HMM 与序列相似性搜索鉴定候选成员，并通过保守结构域复核。
2. **进化树分析**：分别处理单物种家族内部关系和多物种跨物种关系。
3. **Domain 与 Motif 分析**：比较蛋白质保守结构域、保守基序及其排列。
4. **Promoter 分析**：提取启动子并预测顺式作用元件，开展组成统计和有背景的富集比较。
5. **跨物种共线性**：识别物种间保守基因组区段及目标家族的对应关系。
6. **染色体定位与物种内共线性**：展示家族成员染色体分布、重复基因对和 Circos 连线。
7. **Ka、Ks 与 Ka/Ks**：对可靠的同源或复制基因对进行密码子水平的分子进化分析。
8. **GO 分析**：分别进行功能注释和有合适背景集的富集分析。
9. **PPI 分析**：构建蛋白质关联网络，并标注证据类型和预测边界。
10. **表达热图**：整理 RNA-seq 或其他表达矩阵，展示组织、时期和处理条件下的表达模式。
11. **qRT-PCR 验证**：完成引物、内参、扩增效率、重复设计和统计分析。
12. **扩展分析**：按需增加 Gene Structure、Protein Physicochemical Properties，以及 Gene Duplication and Family Expansion。

### 模块索引

- [00. Member Identification and Data QC](modules/00_member-identification-and-data-qc.md)
- [01. Phylogenetic Analysis](modules/01_phylogenetic-analysis.md)
- [02. Domain and Motif Analysis](modules/02_domain-and-motif-analysis.md)
- [03. Promoter and Cis-regulatory Element Analysis](modules/03_promoter-analysis.md)
- [04. Inter-species Synteny](modules/04_inter-species-synteny.md)
- [05. Chromosome Localization and Intra-species Synteny](modules/05_chromosome-and-intra-species-synteny.md)
- [06. Ka, Ks, and Ka/Ks Analysis](modules/06_ka-ks-analysis.md)
- [07. GO Annotation and Enrichment](modules/07_go-analysis.md)
- [08. Protein–Protein Interaction Analysis](modules/08_ppi-analysis.md)
- [09. Expression Analysis and Heatmaps](modules/09_expression-analysis.md)
- [10. qRT-PCR Validation](modules/10_qrt-pcr-validation.md)
- [11. Gene Structure Analysis](modules/11_gene-structure-analysis.md)
- [12. Protein Physicochemical Properties](modules/12_protein-physicochemical-properties.md)
- [13. Gene Duplication and Family Expansion](modules/13_gene-duplication-and-family-expansion.md)

### 通用输入要求

尽可能准备同一参考版本对应的基因组 FASTA、蛋白质 FASTA、CDS FASTA 和 GFF3/GTF 注释文件；跨物种分析还需准备各物种的对应文件及物种系统发育关系。表达分析需提供原始或标准化表达矩阵和完整样本信息；qRT-PCR 需提供原始 Ct、引物信息、扩增效率和重复信息。

必须记录物种名称、基因组组装版本、注释版本、数据库版本、软件版本、关键参数、输入文件来源及文件校验信息。基因 ID、转录本 ID、蛋白 ID 和染色体坐标应建立可追溯映射。

### 质量控制与解释原则

- 不把 BLAST 命中直接等同于功能性家族成员；应结合 HMM、结构域完整性、序列质量和注释证据复核。
- 不把基因树单独作为直系同源关系的充分证据；必要时结合共线性、物种树和基因组上下文。
- 不把预测的顺式元件、GO 注释或 STRING 关联描述为已经实验验证的调控、功能或物理互作。
- 不把 Ka/Ks 单一比值直接作为整个家族受到正选择的结论；需考虑比对质量、Ks 饱和、模型和统计检验。
- 不把基因数量差异直接解释为家族扩张或收缩；应排查基因组质量、注释完整性、同源聚类和系统发育背景。
- 表达热图的行 Z-score 用于展示相对模式，不用于比较不同基因的绝对表达量。
- qRT-PCR 的技术重复不能代替生物学重复；统计检验应使用适当的分析尺度。
- 所有统计分析应报告样本量、检验方法、效应量（适用时）、原始 P 值和多重检验校正方法。

### 输出与可重复性

每个模块应保留原始输入、关键中间文件、最终结果表、绘图数据、脚本或命令、软件和数据库版本，以及排除记录。图表应同时提供可复现的数据来源和清晰图例。论文图件遵循仓库中的 [Scientific Figure Standards](../../plotting/figure-standards.md)。

## English Version

### Purpose and Scope

This Skill provides a plant-focused workflow for gene-family research, from member identification and sequence analysis to comparative genomics, genome evolution, functional annotation, expression profiling, and qRT-PCR validation. It applies to transcription-factor families, metabolic enzyme families, photosynthesis-related families, and other gene families defined by conserved sequence features.

The workflow is modular; not every study needs every module. Select analyses according to the biological question, data quality, and study design. Clearly distinguish computational predictions, statistical associations, and experimental validation.

### End-to-end Workflow

1. **Member identification and data QC:** harmonize genome and annotation versions, identify candidates using profile HMMs and sequence similarity, and validate conserved domains.
2. **Phylogenetic analysis:** analyze within-species family relationships and cross-species evolutionary relationships separately.
3. **Domain and motif analysis:** compare conserved protein domains, motifs, and their arrangements.
4. **Promoter analysis:** extract promoter sequences, predict cis-regulatory elements, and perform composition statistics or enrichment tests with an appropriate background.
5. **Inter-species synteny:** identify conserved genomic blocks and corresponding family members across species.
6. **Chromosome localization and intra-species synteny:** display chromosomal distributions, duplicated gene pairs, and Circos links.
7. **Ka, Ks, and Ka/Ks:** perform codon-level evolutionary analyses on reliable homologous or duplicated gene pairs.
8. **GO analysis:** distinguish functional annotation from enrichment analysis and use an appropriate background universe.
9. **PPI analysis:** construct protein-association networks while documenting evidence types and prediction limits.
10. **Expression heatmaps:** organize RNA-seq or other expression matrices to visualize patterns across tissues, stages, and treatments.
11. **qRT-PCR validation:** document primer specificity, reference genes, amplification efficiency, biological replicates, and statistical analysis.
12. **Optional extensions:** add Gene Structure, Protein Physicochemical Properties, and Gene Duplication and Family Expansion as required.

### Module Index

- [00. Member Identification and Data QC](modules/00_member-identification-and-data-qc.md)
- [01. Phylogenetic Analysis](modules/01_phylogenetic-analysis.md)
- [02. Domain and Motif Analysis](modules/02_domain-and-motif-analysis.md)
- [03. Promoter and Cis-regulatory Element Analysis](modules/03_promoter-analysis.md)
- [04. Inter-species Synteny](modules/04_inter-species-synteny.md)
- [05. Chromosome Localization and Intra-species Synteny](modules/05_chromosome-and-intra-species-synteny.md)
- [06. Ka, Ks, and Ka/Ks Analysis](modules/06_ka-ks-analysis.md)
- [07. GO Annotation and Enrichment](modules/07_go-analysis.md)
- [08. Protein–Protein Interaction Analysis](modules/08_ppi-analysis.md)
- [09. Expression Analysis and Heatmaps](modules/09_expression-analysis.md)
- [10. qRT-PCR Validation](modules/10_qrt-pcr-validation.md)
- [11. Gene Structure Analysis](modules/11_gene-structure-analysis.md)
- [12. Protein Physicochemical Properties](modules/12_protein-physicochemical-properties.md)
- [13. Gene Duplication and Family Expansion](modules/13_gene-duplication-and-family-expansion.md)

### General Input Requirements

Whenever possible, prepare genome FASTA, protein FASTA, CDS FASTA, and GFF3/GTF annotation files from the same reference release. Comparative analyses additionally require corresponding files for each species and a species phylogeny. Expression analyses require an expression matrix and complete sample metadata. qRT-PCR analyses require raw Ct values, primer information, amplification efficiencies, and replicate metadata.

Record species names, genome assembly and annotation releases, database and software versions, key parameters, input provenance, and file checksums. Maintain traceable mappings among gene IDs, transcript IDs, protein IDs, and genomic coordinates.

### Quality Control and Interpretation Rules

- A BLAST hit alone does not establish a functional family member. Review HMM evidence, domain integrity, sequence quality, and annotation support.
- A gene tree alone is not sufficient to establish orthology. Integrate synteny, the species tree, and genomic context when needed.
- Predicted cis-elements, GO annotations, and STRING associations must not be described as experimentally validated regulation, function, or physical interaction.
- A single Ka/Ks ratio must not be used to claim positive selection across an entire family. Consider alignment quality, Ks saturation, model choice, and statistical tests.
- Differences in gene counts alone do not demonstrate family expansion or contraction. Check genome quality, annotation completeness, orthogroup inference, and phylogenetic context.
- Row Z-scores in expression heatmaps show relative patterns, not absolute expression differences among genes.
- Technical qPCR replicates do not replace biological replicates. Statistical tests must use an appropriate measurement scale.
- Report sample sizes, statistical tests, effect sizes where relevant, raw P values, and multiple-testing correction methods.

### Outputs and Reproducibility

Retain original inputs, key intermediate files, final result tables, plotting data, scripts or commands, software and database versions, and exclusion records for every module. Figures must have traceable data sources and clear legends. Follow the repository's [Scientific Figure Standards](../../plotting/figure-standards.md).
