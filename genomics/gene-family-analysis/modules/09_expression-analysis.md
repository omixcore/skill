# 09. Expression Analysis and Heatmaps / 表达分析与热图

## 中文版

### 目的

展示家族成员在不同组织、发育时期和处理条件下的表达模式，并在适当设计下识别差异表达成员。

### 输入与工具

需要表达矩阵、样本信息表、基因 ID 映射表和表达定量方法说明。RNA-seq 差异分析可使用 DESeq2、edgeR 或 limma-voom；热图可使用 ComplexHeatmap、pheatmap 或 ggplot2。

### 流程

1. 核对表达矩阵与样本信息，确保样本名称、组织、时期、处理和生物学重复准确对应。
2. 区分 raw counts、normalized counts、TPM 和 FPKM。不得混用不同量纲的数据。
3. 若开展差异表达推断，应从适当的原始计数矩阵出发，使用 DESeq2、edgeR 等方法及合理的实验设计；不要对 TPM 直接套用不匹配的计数模型。
4. 热图展示可使用 VST/rlog 等变换值，或 log2(TPM + 1) 等适当尺度。按行 Z-score 可突出单个基因在样本间的相对变化。
5. 对样本进行必要的聚类和质量检查，确认重复是否符合实验设计；对缺失值、低表达和零值处理作出说明。
6. 添加组织、时期、处理和亚家族注释条；颜色映射在相关图件中保持一致。
7. 如有多组学数据，可将转录本表达与蛋白丰度并列展示，但应说明不同组学的量纲和检测覆盖差异。

### 质量控制与解释边界

- 行 Z-score 不能用于比较不同基因的绝对表达丰度。
- TPM/FPKM 适合表达展示场景，但不能替代基于计数模型的差异分析。
- 生物学重复与技术重复必须区分。
- 不应因某个样本表达低就未经依据删除样本。
- 不同组织的测序深度、细胞组成和基因长度等因素会影响表达比较。
- 热图颜色应有清晰图例、方向和单位说明。

### 输出

表达矩阵、样本信息表、差异表达结果（如适用）、变换后绘图矩阵、聚类结果、热图及图例。

## English Version

### Objective

Visualize family-member expression across tissues, developmental stages, and treatments, and identify differentially expressed members when the experimental design supports inference.

### Inputs and Tools

Use an expression matrix, sample metadata, gene-ID mapping table, and documentation of the quantification method. Differential-expression tools may include DESeq2, edgeR, or limma-voom. Heatmaps may be generated with ComplexHeatmap, pheatmap, or ggplot2.

### Workflow

1. Verify the expression matrix against sample metadata, including sample names, tissues, stages, treatments, and biological replicates.
2. Distinguish raw counts, normalized counts, TPM, and FPKM. Do not mix values with different scales.
3. For differential-expression inference, start from an appropriate count matrix and use DESeq2, edgeR, or another suitable model with a design that reflects the experiment. Do not apply a count-based model directly to TPM values.
4. For heatmap visualization, use an appropriate scale such as VST/rlog values or log2(TPM + 1). Row-wise Z-scores can highlight relative changes of each gene across samples.
5. Perform appropriate sample clustering and QC. Check replicate consistency and document the treatment of missing values, low expression, and zeros.
6. Add annotations for tissue, stage, treatment, and subfamily. Keep color mappings consistent across related figures.
7. For multi-omics studies, transcript abundance and protein abundance may be shown together, but explain their different scales and detection coverage.

### Quality Control and Interpretation Limits

- Row Z-scores must not be used to compare absolute abundance among different genes.
- TPM/FPKM can be useful for expression visualization but do not replace count-based differential-expression models.
- Distinguish biological from technical replicates.
- Do not remove a low-expression sample without a documented reason.
- Sequencing depth, cell composition, gene length, and other factors can affect comparisons across tissues.
- Heatmaps require clear legends, directionality, and scale descriptions.

### Outputs

Expression matrix, sample metadata, differential-expression results where applicable, transformed plotting matrix, clustering results, heatmap, and figure legend.
