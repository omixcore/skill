# 10. qRT-PCR Validation / qRT-PCR 实验验证

## 中文版

### 目的

通过独立的表达实验验证候选基因在特定组织、发育阶段或处理条件下的表达趋势，并与 RNA-seq 结果进行适当比较。

### 实验设计

1. 明确生物学问题、目标组织、发育时期、处理条件和采样时间。
2. 生物学重复应来自独立生物样本；技术重复用于评估检测重复性，不能代替生物学重复。重复数量应结合效应大小、变异度和实验资源确定。
3. 使用 Primer3 等工具设计引物，并通过基因组或转录组比对检查特异性。对于多拷贝家族，重点检查同源成员间的交叉扩增。
4. 检查引物扩增产物、熔解曲线、阴性对照和必要的无逆转录对照。
5. 对候选内参基因进行组织和处理条件下的稳定性验证，不默认某个常用内参在所有实验中都稳定。
6. 使用标准曲线或其他合适方法评估扩增效率。ΔΔCt 方法通常要求目标基因和内参的扩增效率具有可比性；若效率差异明显，应采用效率校正方法。

### 数据分析

- 检查原始 Ct、扩增曲线、熔解曲线和异常重复。
- 根据实验设计计算 ΔCt；需要相对对照组表达量时，再计算 ΔΔCt 和适用条件下的 2^-ΔΔCt。
- 统计检验原则上在 ΔCt 等适当分析尺度上进行，而不是直接对未经处理的倍数变化值进行检验。
- 若扩增效率不满足 ΔΔCt 假设，采用效率校正的相对定量方法并报告计算方式。
- 展示生物学重复分布、均值或估计值、误差范围、统计检验和显著性标记。
- 与 RNA-seq 比较时，比较表达变化方向和实验条件，不要求不同平台的数值完全相等。

### 质量控制与解释边界

- 技术重复不能作为独立样本用于增加统计样本量。
- 内参基因必须在本实验材料和处理条件下验证。
- 引物特异性、扩增效率和样本质量会影响相对定量结果。
- 2^-ΔΔCt 不是所有扩增效率条件下都适用。
- qRT-PCR 验证的是所测样本和条件下的转录水平，不直接证明蛋白功能或调控机制。
- 参考 MIQE 等报告规范，完整记录样本、引物、扩增条件、效率和数据处理流程。

### 输出

引物信息表、原始 Ct 表、扩增效率记录、熔解曲线和扩增曲线、ΔCt/ΔΔCt 计算表、统计结果和表达验证图。

## English Version

### Objective

Use an independent expression assay to validate candidate-gene expression patterns in defined tissues, developmental stages, or treatment conditions and compare them appropriately with RNA-seq results.

### Experimental Design

1. Define the biological question, target tissues, developmental stages, treatments, and sampling time points.
2. Biological replicates must come from independent biological samples. Technical replicates assess assay repeatability and do not replace biological replicates. Determine replicate numbers using expected effect size, variability, and available resources.
3. Design primers with tools such as Primer3 and check specificity against the genome or transcriptome. For multi-copy families, explicitly test potential cross-amplification among homologous members.
4. Inspect amplicons, melting curves, negative controls, and no-reverse-transcription controls where appropriate.
5. Validate reference-gene stability under the actual tissues and treatments. Do not assume that a commonly used reference gene is stable in every experiment.
6. Evaluate amplification efficiency using standard curves or another suitable method. The ΔΔCt method generally requires comparable amplification efficiencies for target and reference assays; use an efficiency-corrected method when this assumption is not met.

### Data Analysis

- Inspect raw Ct values, amplification curves, melting curves, and anomalous replicates.
- Calculate ΔCt according to the experimental design. For relative expression against a control, calculate ΔΔCt and use 2^-ΔΔCt only when its assumptions are appropriate.
- Perform statistical tests on ΔCt or another suitable analysis scale rather than directly testing untransformed fold-change values.
- If amplification efficiencies do not satisfy the ΔΔCt assumptions, use and report an efficiency-corrected relative-quantification method.
- Show biological replicate distributions, means or estimates, uncertainty, statistical tests, and significance annotations.
- When comparing with RNA-seq, compare the direction of expression changes and experimental conditions; exact numerical equality across platforms is not expected.

### Quality Control and Interpretation Limits

- Technical replicates must not be counted as independent samples to inflate statistical sample size.
- Reference genes must be validated in the actual material and treatment conditions.
- Primer specificity, amplification efficiency, and sample quality affect relative quantification.
- The 2^-ΔΔCt method is not appropriate under every amplification-efficiency condition.
- qRT-PCR validates transcript abundance in the measured samples and conditions; it does not directly establish protein function or a regulatory mechanism.
- Follow reporting standards such as MIQE and document samples, primers, amplification conditions, efficiencies, and data-processing procedures.

### Outputs

Primer information table, raw Ct table, amplification-efficiency records, melting and amplification curves, ΔCt/ΔΔCt calculation table, statistical results, and validation plots.
