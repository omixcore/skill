# 01. Phylogenetic Analysis / 进化树分析

## 中文版

### 目的与分析场景

进化树用于展示家族成员的序列关系和潜在亚家族结构。单物种分析关注家族内部的分化；多物种分析关注跨物种保守性和谱系关系。两种场景应分别组织序列、物种标签和树的解释。

### 输入

经过复核的蛋白质序列、成员 ID 表、物种分类信息，以及必要时的外群序列。跨物种分析应使用可比的基因组版本和成员鉴定标准。

### 流程

1. 使用蛋白序列进行多序列比对，常用 MAFFT；根据序列差异和比对质量选择合适策略。
2. 检查比对质量，识别长缺口、低复杂度片段和不可靠区域。必要时使用 trimAl 或 BMGE 等工具修剪，但记录修剪依据并保留原始比对。
3. 采用最大似然法等适当方法建树，例如 IQ-TREE；根据模型选择结果确定替换模型。
4. 通过 bootstrap、ultrafast bootstrap 或其他合适的分支支持评估方法评估节点支持度，并在图例中明确支持率类型。
5. 单物种树若无合适外群，可展示无根树；需要定根时应说明外群选择依据。
6. 多物种树需标注物种、亚家族和基因 ID。直系同源与旁系同源关系应结合基因组共线性、物种树和基因复制证据判断，不能仅凭树的相邻位置命名。
7. 对树进行可视化时，颜色应对应明确的亚家族或物种类别，避免颜色编码与其他图件冲突。

### 质量控制与解释边界

- 不将低质量或高度截短的序列与完整蛋白不加区分地用于主分析。
- 不在没有依据时强制定根或解释祖先方向。
- 分支支持率表示特定数据和方法下的节点支持，不等于功能证据。
- 对物种取样不均、基因复制和基因丢失保持谨慎。
- 需要区分基因树与物种树；二者不一致可能源于复制、丢失、不完全谱系排序、基因渗入或数据问题。

### 输出

原始和修剪后的比对文件、模型选择结果、Newick 树、建树命令与日志、带标签的树图及成员注释表。

## English Version

### Objective and Analysis Scenarios

Phylogenetic trees describe sequence relationships and potential subfamily structure. Single-species analyses focus on diversification within a family, whereas multi-species analyses examine cross-species conservation and lineage relationships. Organize sequences, species labels, and interpretations separately for these scenarios.

### Inputs

Validated protein sequences, a member-ID table, species taxonomy, and an outgroup when justified. Comparative analyses should use comparable genome releases and member-identification criteria.

### Workflow

1. Perform protein multiple-sequence alignment, commonly with MAFFT, using a strategy appropriate to sequence divergence and alignment quality.
2. Inspect long gaps, low-complexity regions, and unreliable alignment blocks. If trimming with tools such as trimAl or BMGE is justified, document the rationale and retain the untrimmed alignment.
3. Infer a tree using an appropriate method, such as maximum likelihood with IQ-TREE. Select the substitution model based on model testing.
4. Evaluate node support using bootstrap, ultrafast bootstrap, or another justified method. State the support metric in the figure legend.
5. For a single-species tree, an unrooted tree may be appropriate when no defensible outgroup exists. Explain the rationale whenever the tree is rooted.
6. For multi-species trees, label species, subfamilies, and gene IDs. Infer orthology and paralogy using synteny, the species tree, and duplication evidence rather than tree proximity alone.
7. Use colors consistently for subfamilies or species and keep the encoding consistent across related figures.

### Quality Control and Interpretation Limits

- Do not treat low-quality or highly truncated sequences as equivalent to complete proteins.
- Do not force a root or infer an ancestral direction without evidence.
- Branch-support values quantify support under a particular dataset and method; they are not functional evidence.
- Interpret uneven species sampling, duplication, and gene loss cautiously.
- Distinguish gene trees from species trees. Discordance may reflect duplication, loss, incomplete lineage sorting, introgression, or data problems.

### Outputs

Original and trimmed alignments, model-selection results, Newick tree, tree-building commands and logs, annotated tree figures, and member metadata.
