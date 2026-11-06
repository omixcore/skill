# Analysis Methods Word Document Standard / 科研分析方法 Word 文档规范

适用于科研数据分析、生物信息学分析、转录组、蛋白组、代谢组、多组学整合、遗传学分析及其他需要形成论文级 Methods 描述的任务。

**默认要求：每项正式分析任务完成时，除分析结果、代码和图表外，另行提供一份英文版 Microsoft Word 方法文档（`.docx`）。** 文档应达到高水平 SCI 论文 Materials and Methods 部分的清晰度、准确性和可复现性。

## 1. Document Language and File Format / 文档语言与格式

- **File format:** Microsoft Word `.docx`.
- **Language:** English throughout the document, including headings, tables, captions, notes, and methodological descriptions. Do not mix Chinese into the manuscript-ready Methods text.
- **Font:** Times New Roman throughout.
- **Font size:** 12 pt for body text and headings unless a journal-specific template explicitly requires otherwise.
- **Text color:** Black (`#000000`).
- **Body text:** Regular weight, not bold.
- **Heading 1:** Black, bold, Times New Roman, 12 pt; use a clear numbered hierarchy such as `1. Plant Materials and Experimental Design`.
- **Heading 2:** Black, bold, Times New Roman, 12 pt; number hierarchically, for example `1.1. Plant Materials` and `1.2. Experimental Design`.
- **Heading 3:** Avoid unless necessary. If required for a complex method, keep it black, bold, Times New Roman, 12 pt, and number consistently (e.g. `1.1.1.`).
- Use Word's actual Heading 1 and Heading 2 styles, not merely manually enlarged or bolded paragraphs, so the document remains navigable and editable.
- Keep paragraph spacing, indentation, line spacing, page margins, tables, and captions consistent and professional. Do not add decorative colors or unnecessary design elements.

## 2. Recommended Structure / 推荐章节结构

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

## 3. Scientific Writing and Reporting Requirements / 科学写作与报告要求

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

## 4. Accuracy and Reproducibility / 准确性与可重复性

- **Never invent procedures.** Do not describe an analysis, experiment, parameter, software version, database release, sample size, or validation step that was not actually used or cannot be verified.
- Distinguish completed steps from proposed or recommended steps. Only completed and verified procedures belong in the definitive Methods text.
- If essential information is missing, mark it clearly as `[TO BE CONFIRMED]` in the working draft and list the missing items separately. Do not silently guess.
- If a value or parameter can be recovered from scripts, configuration files, logs, or source records, inspect those records before asking the user or writing the Methods section.
- Numerical values, units, thresholds, sample counts, and software versions must be checked against the actual analysis records.
- Statistical descriptions must match the actual tests and models used; do not substitute a more sophisticated method in the prose if it was not run.
- References cited for software, methods, and databases must follow the literature authenticity and claim-support verification standard in `reference-verification.md`.
- Do not overstate reproducibility if source data, scripts, or computational details are unavailable. State limitations clearly.

## 5. Deliverables / 交付要求

For a formal analysis task, provide:

1. The English Methods Word document (`.docx`).
2. The analysis scripts and relevant configuration files, where applicable.
3. The key output tables, figures, and processed data needed to support the analysis.
4. A concise record of software versions, important parameters, input sources, and output locations.
5. A list of any unresolved methodological details that require confirmation.

The Methods document should be a clean, editable manuscript-ready draft, not a report filled with conversational notes. If placeholders remain, clearly identify them and provide a separate checklist of items to confirm.

## 6. Final Quality-Control Checklist / 最终检查清单

- [ ] The document is a valid, editable `.docx` file.
- [ ] All content is in English.
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
