# 12. Protein Physicochemical Properties / 蛋白质理化性质分析

## 中文版

### 目的

描述家族蛋白的基本理化性质，为蛋白长度、分子量、等电点和整体氨基酸组成差异提供比较信息。

### 输入与工具

使用经过质控的蛋白质 FASTA，明确代表转录本选择策略。可使用 ExPASy ProtParam、Biopython 或其他经过验证的序列分析工具。

### 分析指标

- 氨基酸长度（Length）。
- 分子量（Molecular Weight）。
- 理论等电点（Theoretical pI）。
- 不稳定指数（Instability Index）。
- 脂肪族指数（Aliphatic Index）。
- 平均亲水性（GRAVY）。
- 可按研究问题补充氨基酸组成、半胱氨酸比例或其他指标。

### 流程

1. 检查蛋白序列是否含有异常字符、内部终止或明显截短。
2. 使用一致的软件和参数计算所有成员的理化指标。
3. 将结果与基因 ID、亚家族和蛋白长度关联。
4. 采用箱线图、小提琴图或散点图比较亚家族或物种间分布。
5. 若需要预测信号肽、跨膜区或亚细胞定位，应作为独立预测结果展示，并记录相应工具和版本。

### 质量控制与解释边界

- 理论 pI、分子量和 GRAVY 是基于序列的计算值，不等于实验测量结果。
- 不稳定指数、脂肪族指数等经验指标不能单独证明蛋白在体内的稳定性或热稳定性。
- 蛋白长度和异常序列会影响理化指标，应先完成序列质控。
- 不应仅凭某一理化参数推断蛋白定位、功能或生物学活性。
- 比较时应考虑蛋白长度和亚家族组成差异。

### 输出

蛋白理化性质结果表、统计汇总表、分组比较图和序列质控记录。

## English Version

### Objective

Describe basic physicochemical properties of family proteins and compare differences in protein length, molecular weight, isoelectric point, and overall amino-acid composition.

### Inputs and Tools

Use quality-controlled protein FASTA files and a clearly defined representative-transcript strategy. Tools may include ExPASy ProtParam, Biopython, or other validated sequence-analysis software.

### Metrics

- Amino-acid length.
- Molecular weight.
- Theoretical isoelectric point (pI).
- Instability index.
- Aliphatic index.
- Grand average of hydropathicity (GRAVY).
- Additional metrics, such as amino-acid composition or cysteine proportion, may be included when relevant.

### Workflow

1. Check protein sequences for invalid characters, internal stops, and obvious truncations.
2. Calculate all properties using consistent software and settings.
3. Link results to gene IDs, subfamilies, and protein lengths.
4. Compare distributions among subfamilies or species using boxplots, violin plots, or scatterplots.
5. If signal peptides, transmembrane regions, or subcellular localization are predicted, present them as separate prediction results and record the corresponding tools and versions.

### Quality Control and Interpretation Limits

- Theoretical pI, molecular weight, and GRAVY are sequence-derived estimates, not experimental measurements.
- Empirical indices such as instability and aliphatic indices do not independently prove in vivo stability or thermostability.
- Protein length and abnormal sequences affect calculated properties and must be checked first.
- Do not infer localization, function, or biological activity from one physicochemical parameter alone.
- Consider differences in protein length and subfamily composition when comparing groups.

### Outputs

Protein physicochemical-property table, summary statistics, group-comparison plots, and sequence-QC records.
