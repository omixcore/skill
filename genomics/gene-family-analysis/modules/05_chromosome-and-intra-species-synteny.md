# 05. Chromosome Localization and Intra-species Synteny / 染色体定位与物种内共线性

## 中文版

### 目的

展示家族成员在单一物种染色体上的分布，并识别物种内保守共线性区块和潜在重复基因关系。该模块与物种间共线性分开处理。

### 输入与工具

需要同一参考版本的 GFF3/GTF、染色体长度文件、目标家族成员坐标及全基因组蛋白序列。可使用 MCScanX、WGDI、TBtools、Circos 或 R 绘图工具。

### 流程

1. 从注释文件提取基因染色体、起止位置和链方向，核对坐标是否落在对应染色体长度范围内。
2. 绘制染色体定位图，突出目标家族成员，并根据需要添加染色体长度、基因密度或其他背景信息。
3. 进行全基因组自比对和共线性分析，过滤自匹配并识别共线性区块。
4. 将目标家族成员映射到区块，提取同一物种内的重复基因对。
5. 根据明确的距离和共线性证据区分 tandem、proximal、segmental/WGD 及其他复制类别；分类阈值和软件定义必须记录。
6. 绘制 Circos 图时，可将染色体作为外圈，将家族成员作为高亮标记，将共线性区块或目标基因对作为连线。控制连线数量和透明度，避免遮挡。
7. 对多倍体或复杂基因组，明确亚基因组、染色体命名和重复关系的判定规则。

### 质量控制与解释边界

- 染色体定位只描述位置，不等于复制或功能证据。
- 仅凭物理距离不能可靠区分所有复制类型；应结合共线性区块和基因组演化背景。
- 物种内共线性不应与物种间共线性混为一谈。
- Circos 图应保留可追溯的连线数据表，不能只保存图片。
- 高密度连线应采用分层、筛选或局部放大方式展示。

### 输出

染色体坐标表、染色体定位图、物种内共线性区块表、重复基因对表、Circos 连线文件和高分辨率图件。

## English Version

### Objective

Display the chromosomal distribution of family members within one species and identify intra-genomic syntenic blocks and potential duplicated-gene relationships. Keep this module distinct from inter-species synteny.

### Inputs and Tools

Use GFF3/GTF, chromosome-length files, target-member coordinates, and whole-genome protein sequences from the same reference release. Suitable tools include MCScanX, WGDI, TBtools, Circos, and R plotting packages.

### Workflow

1. Extract chromosome, start, end, and strand information from the annotation and verify that coordinates fall within chromosome boundaries.
2. Plot chromosome locations, highlighting family members and optionally adding chromosome lengths, gene density, or other genomic context.
3. Perform whole-genome self-comparison and synteny analysis, remove self-matches, and identify collinear blocks.
4. Map family members to blocks and retrieve intra-species duplicated gene pairs.
5. Classify tandem, proximal, segmental/WGD, and other duplication categories using explicit distance and synteny evidence. Record software definitions and thresholds.
6. For Circos plots, use chromosomes as outer tracks, highlight family members, and draw links for syntenic blocks or target gene pairs. Control link density and transparency to prevent visual clutter.
7. For polyploid or complex genomes, define subgenome labels, chromosome nomenclature, and duplication-classification rules explicitly.

### Quality Control and Interpretation Limits

- Chromosome localization describes genomic position; it is not evidence of duplication or function.
- Physical distance alone cannot reliably distinguish all duplication classes. Integrate syntenic blocks and genome-evolution context.
- Do not conflate intra-species with inter-species synteny.
- Retain traceable link tables for Circos plots rather than saving only the image.
- Use layering, filtering, or local insets for dense connections.

### Outputs

Chromosomal coordinate table, chromosome-location plot, intra-species syntenic-block table, duplicated-pair table, Circos link files, and publication-quality figures.
