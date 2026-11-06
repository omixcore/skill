# 科研分析方法 Word 文档规范 / Analysis Methods Word Document Standard

适用于科研数据分析、生物信息学分析、转录组、蛋白组、代谢组、多组学整合、遗传学分析及其他需要形成论文级 Methods 描述的任务。

This standard applies to scientific data analysis, bioinformatics, transcriptomics, proteomics, metabolomics, multi-omics integration, genetics, and other workflows that require a manuscript-level Methods description.

**默认要求：每项正式分析任务完成时，除分析结果、代码和图表外，另行提供一份英文版 Microsoft Word 方法文档（`.docx`）。** 文档应达到高水平 SCI 论文 Materials and Methods 部分的清晰度、准确性和可复现性。

**Default requirement: For every formal analysis task, provide an additional English-language Microsoft Word Methods document (`.docx`) alongside the results, code, and figures.** The document should meet the clarity, accuracy, and reproducibility standards expected of a strong SCI-journal Materials and Methods section.

## 中文版

### 1. 文档语言与格式

- **文件格式：** Microsoft Word `.docx`。
- **语言：** 正式 Methods 文档全英文，包括标题、表格、图注、注释和方法描述；不要在可投稿的 Methods 正文中混入中文。
- **字体：** 全文 Times New Roman。
- **字号：** 正文和标题均为 12 pt，除非目标期刊模板另有明确要求。
- **文字颜色：** 纯黑色（`#000000`）。
- **正文：** 常规字重，不加粗。
- **一级标题：** 黑色、加粗、Times New Roman、12 pt，使用清晰的编号层级，例如 `1. Plant Materials and Experimental Design`。
- **二级标题：** 黑色、加粗、Times New Roman、12 pt，采用层级编号，例如 `1.1. Plant Materials` 和 `1.2. Experimental Design`。
- **三级标题：** 非必要不使用；复杂方法确有需要时，使用黑色、加粗、Times New Roman、12 pt，并保持编号一致（如 `1.1.1.`）。
- 使用 Word 原生 Heading 1 和 Heading 2 样式，不要只通过手动放大或加粗段落模拟标题，以确保文档可导航、可编辑。
- 段落间距、缩进、行距、页边距、表格和图注应统一、专业；不添加装饰性颜色或无必要的设计元素。

### 2. 推荐章节结构

仅保留与实际分析有关的章节。根据项目需要调整、合并、拆分或删除标题，不要强制所有项目套用完全相同的模板。

常见章节可包括：

1. **Plant Materials and Experimental Design（植物材料与实验设计）**
   - 植物材料、基因型、生物材料、样本分组、组织、发育阶段、处理条件、生物学/技术重复及实验设计。
2. **Data Sources and Data Acquisition（数据来源与获取）**
   - 公共数据库编号、数据仓库、必要时的下载日期、原始数据类型、仪器/平台、参考基因组、注释版本和元数据来源。
3. **Data Quality Control and Preprocessing（数据质控与预处理）**
   - 质量评估、过滤、剪切、污染检查、缺失值处理、标准化、转换、填补和排除标准。
4. **Sequence Processing and Quantification（序列处理与定量，适用时）**
   - 比对或伪比对、基因组/转录组参考版本、注释版本、定量方法及相关设置。
5. **Differential Analysis and Statistical Testing（差异分析与统计检验）**
   - 统计模型、比较组、检验类型、多重检验校正、显著性阈值、效应量标准和软件/程序包版本。
6. **Functional Annotation and Enrichment Analysis（功能注释与富集分析）**
   - 注释数据库及版本、背景基因集、富集方法、基因/蛋白/代谢物标识符、校正方法和阈值。
7. **Multi-Omics Integration（多组学整合，适用时）**
   - 数据匹配、尺度转换、整合策略、相关性或一致性分析、九象限/分类规则及解释标准。
8. **Network and Pathway Analysis（网络与通路分析，适用时）**
   - 数据库/来源及版本、互作置信度阈值、通路定义和分析参数。
9. **Statistical Analysis and Data Visualization（统计分析与数据可视化）**
   - 统计检验、假设条件、重复定义、误差线含义、软件版本、绘图程序包和显著性标记。
10. **Software Availability and Reproducibility（软件可用性与可重复性）**
    - 软件名称和版本、可用的脚本或仓库链接、计算环境及复现步骤。

根据具体项目使用科学上合适的标题。例如 GWAS、QTL、单细胞、启动子分析、蛋白组、代谢组或显微成像，应采用能够准确反映各自流程的方法章节。

### 3. 科学写作与报告要求

- 使用简洁、正式、可用于投稿的学术英语。
- 按照有助于理解和复现的顺序，描述实际完成的工作。
- 在适用时写明生物材料、样本量、分组结构、重复类型和实验条件。
- 尽可能报告数据来源、登录号、参考组装版本、注释版本、软件/程序包名称及版本、数据库版本。
- 报告关键参数、过滤标准、标准化与转换流程、统计模型、检验类型、多重检验校正方法、显著性阈值及相关单位。
- 定义实验或统计单位，并区分生物学重复与技术重复。
- 在适用时说明缺失数据、离群值、批次效应和低质量样本/特征的处理方法。
- 在富集分析中说明背景集/统计背景及标识符映射方法。
- 仅在可视化选择属于分析方法或为结果复现所必需时描述相关设置。
- 基因、蛋白、代谢物、物种、品种、组织和发育阶段的命名保持一致。
- 确保 Methods 与脚本、软件日志、输入数据、表格、图片及结果一致。

### 4. 准确性与可重复性

- **不得编造流程。** 不得描述实际未执行或无法核实的分析、实验、参数、软件版本、数据库版本、样本量或验证步骤。
- 区分已完成的步骤与拟议/推荐的步骤；正式 Methods 只能写入已完成且经过核实的流程。
- 如果关键信息缺失，应在工作稿中明确标记为 `[TO BE CONFIRMED]`，并单独列出待核实事项，不得默默猜测。
- 如果数值或参数可从脚本、配置文件、日志或源记录中恢复，应先检查这些记录，再询问用户或撰写 Methods。
- 数值、单位、阈值、样本数和软件版本必须对照实际分析记录核实。
- 统计描述必须与实际使用的检验和模型一致；不能在文字中把未运行的方法替换成看似更高级的方法。
- 软件、方法和数据库引用必须遵循 `reference-verification.md` 中的文献真实性与语句支撑性核查规范。
- 如果原始数据、脚本或计算细节不可用，不得夸大可重复性，应明确说明局限。

### 5. 交付要求

正式分析任务应提供：

1. 英文版 Methods Word 文档（`.docx`）。
2. 适用时提供分析脚本和相关配置文件。
3. 支持分析的关键结果表、图片和处理后数据。
4. 软件版本、关键参数、输入来源和输出位置的简要记录。
5. 需要进一步确认的未解决方法学细节清单。

Methods 文档应是整洁、可编辑、接近投稿稿件的文本，而不是充满对话备注的报告。如果仍有占位符，应清楚标记，并另附待确认事项清单。

### 6. 最终质量检查清单

- [ ] 文档是有效且可编辑的 `.docx` 文件。
- [ ] Methods 正文全部为英文。
- [ ] 全文使用 Times New Roman。
- [ ] 正文和标题均为 12 pt。
- [ ] 一级和二级标题为黑色加粗，并采用一致的编号。
- [ ] 使用 Word 原生标题样式，便于导航。
- [ ] 章节反映实际分析，而不是机械套用通用模板。
- [ ] 样本量、重复、数据来源、软件版本和参数均已核实。
- [ ] 统计检验、阈值和校正方法与实际分析一致。
- [ ] 没有将未执行的实验或分析写成已完成。
- [ ] 所有方法/软件/数据库引用真实存在，且确实支持相关描述。
- [ ] 缺失信息已明确标记并列入待确认清单。
- [ ] 文档内容与脚本、日志、表格、图片和最终结果一致。

**核心原则：Methods 必须依据经过核实的分析记录撰写，而不是依据理想化流程编写；文档风格应达到投稿要求，内容必须忠实反映实际执行的工作。**

## English Version

### 1. Document Language and File Format

- **File format:** Microsoft Word `.docx`.
- **Language:** The manuscript-ready Methods document must be entirely in English, including headings, tables, captions, notes, and methodological descriptions. Do not mix Chinese into the Methods text intended for submission.
- **Font:** Times New Roman throughout.
- **Font size:** 12 pt for body text and headings unless a journal-specific template explicitly requires otherwise.
- **Text color:** Black (`#000000`).
- **Body text:** Regular weight, not bold.
- **Heading 1:** Black, bold, Times New Roman, 12 pt; use a clear numbered hierarchy such as `1. Plant Materials and Experimental Design`.
- **Heading 2:** Black, bold, Times New Roman, 12 pt; number hierarchically, for example `1.1. Plant Materials` and `1.2. Experimental Design`.
- **Heading 3:** Avoid unless necessary. If required for a complex method, keep it black, bold, Times New Roman, 12 pt, and number consistently (e.g. `1.1.1.`).
- Use Word's actual Heading 1 and Heading 2 styles, not merely manually enlarged or bolded paragraphs, so the document remains navigable and editable.
- Keep paragraph spacing, indentation, line spacing, page margins, tables, and captions consistent and professional. Do not add decorative colors or unnecessary design elements.

### 2. Recommended Structure

Use only sections relevant to the actual analysis. Adapt, merge, split, or omit headings according to the project; do not force every project into an identical template.

A typical structure may include:

1. **Plant Materials and Experimental Design**
   - Plant materials, genotypes, biological materials, sample groups, tissues, developmental stages, treatments, biological/technical replicates, and experimental design.
2. **Data Sources and Data Acquisition**
   - Public accession numbers, repositories, download dates when relevant, raw data types, instruments/platforms, reference genomes, annotations, and metadata sources.
3. **Data Quality Control and Preprocessing**
   - Quality assessment, filtering, trimming, contamination checks, missing-value handling, normalization, transformation, imputation, and exclusion criteria.
4. **Sequence Processing and Quantification** (when applicable)
   - Alignment or pseudo-alignment, genome/transcriptome reference, annotation release, quantification method, and relevant settings.
5. **Differential Analysis and Statistical Testing**
   - Statistical model, contrasts, test type, multiple-testing correction, significance thresholds, effect-size criteria, and software/package versions.
6. **Functional Annotation and Enrichment Analysis**
   - Annotation databases and versions, background universe, enrichment methods, gene/protein/metabolite identifiers, correction method, and thresholds.
7. **Multi-Omics Integration** (when applicable)
   - Data matching, scaling, integration strategy, correlation or concordance analysis, quadrant/classification rules, and interpretation criteria.
8. **Network and Pathway Analysis** (when applicable)
   - Database/source and version, interaction confidence threshold, pathway definitions, and analysis settings.
9. **Statistical Analysis and Data Visualization**
   - Statistical tests, assumptions, replicate definition, error-bar definitions, software versions, plotting packages, and significance notation.
10. **Software Availability and Reproducibility**
    - Software names and versions, scripts or repository links when available, computational environment, and steps needed to reproduce the analysis.

Use scientifically appropriate headings for the specific project. For example, a GWAS, QTL, single-cell, promoter analysis, proteomics, metabolomics, or microscopy workflow should have methods sections that accurately reflect its own procedures.

### 3. Scientific Writing and Reporting Requirements

- Write in concise, formal, publication-ready academic English.
- Describe what was actually done, in the order needed to understand and reproduce the workflow.
- Include the biological materials, sample size, group structure, replicate type, and experimental conditions when applicable.
- Report data sources, accession IDs, reference assemblies, annotation versions, software/package names and versions, and database versions where available.
- Report important parameters, filtering criteria, normalization and transformation procedures, statistical models, test types, multiple-testing correction methods, significance thresholds, and relevant units.
- Define the experimental or statistical unit and distinguish biological replicates from technical replicates.
- Explain how missing data, outliers, batch effects, and low-quality samples/features were handled, if applicable.
- State the background/universe used for enrichment analyses and the identifier mapping procedure where relevant.
- Describe visualization choices only when they are part of the analytical method or needed to interpret reproducible outputs.
- Use consistent gene, protein, metabolite, species, cultivar, tissue, and developmental-stage nomenclature.
- Ensure that the methods described agree with the scripts, software logs, input data, tables, figures, and reported results.

### 4. Accuracy and Reproducibility

- **Never invent procedures.** Do not describe an analysis, experiment, parameter, software version, database release, sample size, or validation step that was not actually used or cannot be verified.
- Distinguish completed steps from proposed or recommended steps. Only completed and verified procedures belong in the definitive Methods text.
- If essential information is missing, mark it clearly as `[TO BE CONFIRMED]` in the working draft and list the missing items separately. Do not silently guess.
- If a value or parameter can be recovered from scripts, configuration files, logs, or source records, inspect those records before asking the user or writing the Methods section.
- Numerical values, units, thresholds, sample counts, and software versions must be checked against the actual analysis records.
- Statistical descriptions must match the actual tests and models used; do not substitute a more sophisticated method in the prose if it was not run.
- References cited for software, methods, and databases must follow the literature authenticity and claim-support verification standard in `reference-verification.md`.
- Do not overstate reproducibility if source data, scripts, or computational details are unavailable. State limitations clearly.

### 5. Deliverables

For a formal analysis task, provide:

1. The English Methods Word document (`.docx`).
2. The analysis scripts and relevant configuration files, where applicable.
3. The key output tables, figures, and processed data needed to support the analysis.
4. A concise record of software versions, important parameters, input sources, and output locations.
5. A list of any unresolved methodological details that require confirmation.

The Methods document should be a clean, editable manuscript-ready draft, not a report filled with conversational notes. If placeholders remain, clearly identify them and provide a separate checklist of items to confirm.

### 6. Final Quality-Control Checklist

- [ ] The document is a valid, editable `.docx` file.
- [ ] All Methods content is in English.
- [ ] Times New Roman is used throughout.
- [ ] Body text and headings are 12 pt.
- [ ] Heading 1 and Heading 2 are black and bold, with consistent numbering.
- [ ] Word heading styles are applied so the document is navigable.
- [ ] Sections reflect the actual analysis rather than a generic template.
- [ ] Sample sizes, replicates, data sources, software versions, and parameters are verified.
- [ ] Statistical tests, thresholds, and correction methods match the analysis actually performed.
- [ ] No unperformed experiment or analysis is described as completed.
- [ ] All method/software/database citations are authentic and support the relevant statements.
- [ ] Any missing information is explicitly marked and listed for confirmation.
- [ ] The document agrees with the scripts, logs, tables, figures, and final results.

**Core principle: write the Methods from the verified analysis record, not from an idealized workflow. The document must be publication-ready in style and faithful to what was actually performed.**
