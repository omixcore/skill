# 07. GO Annotation and Enrichment / GO 功能注释与富集分析

## 中文版

### 目的

为家族成员提供 Gene Ontology 功能注释，并在适当背景集合下检验某些 GO 条目是否过度代表。必须区分“功能注释”和“功能富集”。

### 输入与工具

准备目标基因 ID、物种信息、蛋白序列及注释来源。可使用 InterProScan、eggNOG-mapper、Ensembl Plants、UniProt 或物种专属注释资源；富集可使用 clusterProfiler、topGO 或其他统计工具。

### 流程

1. 记录注释数据库、版本、物种、映射策略和证据类型。
2. 将蛋白或基因 ID 映射到 GO ID，去除无效映射并保留未注释成员清单。
3. 将 GO 注释按 Biological Process、Molecular Function 和 Cellular Component 分类汇总。
4. 如开展富集分析，定义 foreground 和 background。背景通常应为本研究中有机会被检测或注释的基因集合，而不是未经说明地使用任意全基因组集合。
5. 选择适当的过度代表分析或基于排序的富集方法，明确检验统计量和多重检验校正。
6. 报告 GO term、基因数、背景数、富集倍数、P 值和 FDR，并对冗余条目进行合理归并或可视化。
7. 对小型家族，若统计功效不足，应以注释汇总和文献证据为主，不强行生成富集结论。

### 质量控制与解释边界

- 同源转移得到的 GO 注释应与本物种直接实验注释区分。
- 不能将预测注释写成实验验证功能。
- 背景集合错误会显著改变富集结果。
- 需考虑不同基因注释数量和注释深度带来的偏倚。
- GO 富集表示统计过度代表，不直接证明生物学机制。
- 报告 FDR，而非只报告未经校正的 P 值。

### 输出

GO 注释表、ID 映射表、未注释成员表、富集结果表、BP/MF/CC 分类图和富集气泡图。

## English Version

### Objective

Provide Gene Ontology annotations for family members and test whether selected GO terms are overrepresented using an appropriate background. Keep functional annotation distinct from functional enrichment.

### Inputs and Tools

Prepare target gene IDs, species information, protein sequences, and annotation sources. Resources may include InterProScan, eggNOG-mapper, Ensembl Plants, UniProt, or species-specific annotation databases. Enrichment tools may include clusterProfiler, topGO, or other statistical packages.

### Workflow

1. Record annotation databases, versions, species, mapping procedures, and evidence types.
2. Map protein or gene IDs to GO terms, remove invalid mappings, and retain a list of unannotated members.
3. Summarize annotations across Biological Process, Molecular Function, and Cellular Component.
4. For enrichment, define foreground and background sets. The background should generally represent genes that could have been detected or annotated in the study, rather than an arbitrary whole-genome set.
5. Choose an appropriate over-representation or rank-based enrichment method and document the test statistic and multiple-testing correction.
6. Report GO terms, foreground counts, background counts, enrichment ratios, P values, and FDR. Reduce redundant terms carefully for visualization.
7. For small families with limited statistical power, prioritize annotation summaries and supporting literature rather than forcing enrichment claims.

### Quality Control and Interpretation Limits

- Distinguish homology-transferred GO annotations from direct experimental annotations in the target species.
- Do not present predicted annotations as experimentally validated functions.
- An inappropriate background set can substantially change enrichment results.
- Consider biases caused by differences in gene annotation coverage and annotation depth.
- GO enrichment indicates statistical overrepresentation; it does not directly establish a biological mechanism.
- Report FDR rather than only unadjusted P values.

### Outputs

GO annotation table, ID mapping table, unannotated-member list, enrichment results, BP/MF/CC classification plots, and enrichment dot plots.
