# 06. Ka, Ks, and Ka/Ks Analysis / Ka、Ks 与 Ka/Ks 分析

## 中文版

### 目的

估算同源或复制基因对的非同义替换率 Ka、同义替换率 Ks 及其比值，辅助评估蛋白编码序列的进化约束和选择压力。

### 输入与工具

需要可靠的同源或复制基因对、对应 CDS 和蛋白质序列。常见工具包括 MAFFT、PAL2NAL、ParaAT、KaKs_Calculator 和 PAML。工具和模型应按数据与研究问题选择。

### 流程

1. 明确配对依据：优先使用基因树、共线性、正交群或有依据的复制关系，不应任意组合所有序列。
2. 对蛋白序列进行多序列或成对比对，并检查比对质量。
3. 将蛋白比对映射回 CDS，构建密码子比对；不能将蛋白比对直接当作密码子比对。
4. 使用适当模型估计 Ka、Ks 和 Ka/Ks，并记录遗传密码、模型、参数和软件版本。
5. 检查异常值、零值、极低 Ks、极高 Ks、移码、内部终止和低质量比对。
6. 绘制 Ka–Ks 散点图、Ks 分布、Ka/Ks 分布，并按复制类型、物种或亚家族分组。
7. 如估算复制或分化时间，需使用适用于目标谱系的同义替换速率 λ，并说明公式和单位。常见近似为 T = Ks / (2λ)，其成立依赖速率假设和模型条件。

### 质量控制与解释边界

- Ks 饱和会使较古老基因对的估计不可靠。
- Ks 接近零、Ka/Ks 分母异常或比对质量差时，Ka/Ks 可能不稳定。
- Ka/Ks > 1 的成对比值本身不足以证明正选择；应考虑模型检验、位点或分支层面的证据及统计支持。
- Ka/Ks < 1 通常与纯化选择相符，但也需结合模型和序列质量解释。
- 基因转换、重组、密码子偏好和不同谱系替换速率可能影响估计。
- 不能将所有基因对视为独立生物学重复。

### 输出

基因对清单、蛋白比对、密码子比对、Ka/Ks 结果表、异常值排查记录、分布图和时间估算假设说明。

## English Version

### Objective

Estimate nonsynonymous substitution rates (Ka), synonymous substitution rates (Ks), and their ratio for homologous or duplicated gene pairs to assess coding-sequence constraints and potential selection pressures.

### Inputs and Tools

Use reliable homologous or duplicated gene pairs with corresponding CDS and protein sequences. Common tools include MAFFT, PAL2NAL, ParaAT, KaKs_Calculator, and PAML. Select tools and models according to the data and research question.

### Workflow

1. Define the basis for pairing genes. Prefer evidence from gene trees, synteny, orthogroups, or documented duplication relationships rather than arbitrary pairwise combinations.
2. Align protein sequences and inspect alignment quality.
3. Project the protein alignment back to CDS to generate a codon-aware alignment. A protein alignment alone is not a codon alignment.
4. Estimate Ka, Ks, and Ka/Ks with an appropriate model. Record the genetic code, model, parameters, and software version.
5. Inspect outliers, zero values, very low or high Ks, frameshifts, internal stops, and poor alignments.
6. Plot Ka–Ks scatterplots and Ks and Ka/Ks distributions, stratified by duplication type, species, or subfamily when appropriate.
7. For duplication or divergence dating, use a synonymous substitution rate (λ) appropriate to the lineage and state the formula and units. A common approximation is T = Ks / (2λ), which depends on rate assumptions and model conditions.

### Quality Control and Interpretation Limits

- Ks saturation can make estimates for ancient gene pairs unreliable.
- Ka/Ks may be unstable when Ks is near zero, the denominator is problematic, or the alignment is poor.
- A pairwise Ka/Ks value above 1 is not sufficient by itself to demonstrate positive selection. Consider model tests, site- or branch-level evidence, and statistical support.
- Ka/Ks below 1 is generally consistent with purifying selection but still requires interpretation in light of model and sequence quality.
- Gene conversion, recombination, codon bias, and lineage-specific substitution rates can affect estimates.
- Do not treat all gene pairs as independent biological replicates.

### Outputs

Gene-pair list, protein alignments, codon alignments, Ka/Ks result table, outlier review records, distribution plots, and documentation of dating assumptions.
