# 04. Inter-species Synteny / 物种间共线性分析

## 中文版

### 目的

识别不同物种之间保守的基因组区段，并定位目标家族成员在这些区段中的对应关系，为跨物种保守性、复制历史和候选直系同源关系提供证据。

### 输入与工具

准备各物种同一注释体系下的蛋白质序列、基因组坐标和 GFF3/GTF。可使用 MCScanX、JCVI、WGDI 或其他适合的共线性工具；同源群识别可结合 OrthoFinder 或相似性搜索。

### 流程

1. 核对物种名称、基因组版本、注释版本、染色体命名和坐标单位。
2. 建立跨物种同源候选关系，可结合全蛋白相似性、正交群和系统发育结果。
3. 运行全基因组共线性分析，识别保守基因块；记录锚定基因数量、块长度和筛选规则。
4. 将目标家族成员映射到共线性区块，识别跨物种保守的邻近基因和局部基因顺序。
5. 对重点成员绘制局部 microsynteny 图，显示目标基因及其上下游邻近基因。
6. 对未找到对应成员的情况，检查基因组缺口、注释差异、基因丢失、易位、快速序列分化和检索阈值。

### 质量控制与解释边界

- 共线性支持基因组上下文保守，但不能单独证明基因功能相同。
- 不能把所有相似基因都称为直系同源；应综合基因树、共线性和物种关系。
- 物种间染色体融合、断裂、倍性差异和组装质量会影响图形解释。
- 不同物种基因注释完整度不一致时，缺失成员可能是注释缺失而非真实基因丢失。
- 比较图应标明物种、染色体、区间和方向。

### 输出

跨物种共线性区块表、目标家族对应关系表、局部 microsynteny 图、全基因组共线性图和未匹配成员复核表。

## English Version

### Objective

Identify conserved genomic regions across species and map family members within those regions. This provides evidence for cross-species conservation, duplication history, and candidate orthology.

### Inputs and Tools

Prepare protein sequences, genomic coordinates, and GFF3/GTF annotations for each species. Suitable tools include MCScanX, JCVI, and WGDI. Orthogroup inference can be integrated using OrthoFinder or sequence-similarity searches.

### Workflow

1. Verify species names, genome and annotation releases, chromosome naming conventions, and coordinate units.
2. Establish candidate homologous relationships using whole-proteome similarity, orthogroups, and phylogenetic evidence.
3. Run genome-wide synteny analysis to identify conserved blocks. Record anchor-gene counts, block lengths, and filtering rules.
4. Map target family members to syntenic blocks and identify conserved neighboring genes and local gene order.
5. Draw local microsynteny plots for important members, showing the target gene and its flanking genes.
6. For unmatched members, investigate assembly gaps, annotation differences, gene loss, rearrangements, rapid sequence divergence, and search thresholds.

### Quality Control and Interpretation Limits

- Synteny supports conservation of genomic context but does not by itself prove identical gene function.
- Do not label every similar sequence as an ortholog. Integrate gene trees, synteny, and species relationships.
- Chromosome fusion, fission, ploidy differences, and assembly quality can affect interpretation.
- Incomplete annotation may explain an apparently missing member; absence from an annotation is not automatically evidence of gene loss.
- Label species, chromosomes, intervals, and orientation in comparative plots.

### Outputs

Inter-species syntenic-block table, family-member correspondence table, local microsynteny plots, genome-wide synteny plots, and a review table for unmatched members.
