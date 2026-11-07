# 00. Gene Family Member Identification and Data QC / 基因家族成员鉴定与数据质控

## 中文版

### 目的

建立可信、可追溯的家族成员集合，为进化树、结构域、启动子、共线性和功能分析提供统一输入。

### 必需输入

- 参考基因组 FASTA、蛋白质 FASTA、CDS FASTA 和 GFF3/GTF。
- 物种名称、基因组组装版本和基因注释版本。
- 目标家族的保守结构域信息、Pfam HMM 或经过验证的种子蛋白序列。
- 可用时提供已发表的家族成员清单或人工验证序列。

### 分析流程

1. **核对参考数据**：确认蛋白、CDS、基因组和注释文件来自同一组装版本；检查序列 ID 是否能与注释文件对应。
2. **候选检索**：使用 HMMER 的 profile-HMM 搜索和 BLASTP 等相似性搜索。可使用 Pfam、InterPro 或经过验证的家族序列建立检索依据。阈值应依据模型、家族保守性和物种背景确定，不使用对所有家族都通用的固定 E-value。
3. **结构域复核**：使用 InterProScan、Pfam、CDD 或 SMART 检查候选蛋白的结构域类型、完整性、位置和组合。排查仅含短片段、低复杂度区域或非特异命中的序列。
4. **转录本处理**：默认可选择每个基因最长的完整蛋白异构体作为家族比较的代表序列，但必须保留转录本映射表。若研究涉及可变剪接、组织特异异构体或结构域差异，应保留并分析多个转录本。
5. **序列质量检查**：检查蛋白长度、内部终止、异常字符、CDS 与蛋白翻译一致性、移码和缺失结构域。疑似假基因、部分基因模型和低质量模型应单独标记，不应静默删除。
6. **ID 和坐标整合**：建立 gene ID、transcript ID、protein ID、染色体、起止位置和链方向的映射表。检查重复 ID、缺失坐标和同一基因的多个转录本。
7. **人工抽查**：检查家族边界成员、极短或极长蛋白、结构域异常成员及不同数据库结果不一致的候选。

### 质量控制

- 区分“检索到的候选”“结构域支持的成员”和“高可信完整成员”。
- 记录被排除或单独归类的序列及理由。
- 对注释缺失或组装不完整的物种，不宣称已穷尽全部家族成员。
- 不以基因名称或注释描述作为唯一鉴定依据。
- 跨物种比较时使用一致的鉴定流程和可比的证据标准。

### 输出

- 高可信家族成员清单。
- 全部候选及排除原因表。
- 蛋白和 CDS FASTA。
- gene–transcript–protein ID 映射表。
- 结构域验证结果。
- 参考版本、软件、数据库、阈值和运行记录。

## English Version

### Objective

Establish a reliable and traceable set of family members that can be used consistently in phylogenetic, domain, promoter, synteny, and functional analyses.

### Required Inputs

- Reference genome FASTA, protein FASTA, CDS FASTA, and GFF3/GTF annotation.
- Species name, genome assembly release, and gene annotation release.
- Conserved-domain information, a Pfam HMM profile, or validated seed protein sequences.
- Published member lists or experimentally validated sequences, when available.

### Workflow

1. **Verify reference data:** confirm that protein, CDS, genome, and annotation files belong to the same assembly release and that sequence identifiers match the annotation.
2. **Retrieve candidates:** search with HMMER profile-HMMs and sequence-similarity tools such as BLASTP. Use Pfam, InterPro, or validated family sequences as evidence. Set thresholds according to the model, family conservation, and species context rather than applying one universal E-value.
3. **Validate domains:** use InterProScan, Pfam, CDD, or SMART to inspect domain identity, integrity, position, and architecture. Flag short fragments, low-complexity sequences, and nonspecific matches.
4. **Handle transcript isoforms:** a longest complete protein isoform per gene may be used as the default representative for family-level comparisons, but retain the transcript mapping table. Analyze multiple isoforms when alternative splicing, tissue-specific isoforms, or domain variation is relevant.
5. **Check sequence quality:** inspect protein length, internal stop codons, invalid characters, CDS-to-protein translation consistency, frameshifts, and missing domains. Flag suspected pseudogenes, partial models, and low-confidence models separately rather than silently removing them.
6. **Integrate IDs and coordinates:** create a mapping table for gene ID, transcript ID, protein ID, chromosome, start, end, and strand. Check duplicate IDs, missing coordinates, and multiple transcripts per gene.
7. **Manually review edge cases:** inspect boundary candidates, unusually short or long proteins, abnormal domain architectures, and candidates with conflicting database results.

### Quality Control

- Distinguish retrieved candidates, domain-supported members, and high-confidence complete members.
- Record excluded or separately classified sequences and the reason for each decision.
- Do not claim a complete family inventory when genome assembly or annotation is incomplete.
- Do not use gene names or annotation descriptions as the sole identification criterion.
- Apply comparable identification procedures and evidence standards across species.

### Outputs

- High-confidence family-member list.
- Complete candidate and exclusion-reason table.
- Protein and CDS FASTA files.
- Gene–transcript–protein ID mapping table.
- Domain-validation results.
- Reference releases, software and database versions, thresholds, and run records.
