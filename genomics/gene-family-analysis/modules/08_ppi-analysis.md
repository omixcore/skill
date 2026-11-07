# 08. Protein–Protein Interaction Analysis / 蛋白质互作分析

## 中文版

### 目的

构建目标家族成员及其候选互作蛋白的网络，探索潜在功能联系和网络模块，并明确网络证据的来源。

### 输入与工具

需要标准化的蛋白或基因 ID、物种信息和目标家族成员表。可使用 STRING、BioGRID、IntAct 等资源检索；网络可使用 Cytoscape 展示和分析。

### 流程

1. 将目标 ID 映射到数据库中的物种特异蛋白 ID，记录无法映射的成员。
2. 检索互作或功能关联，记录数据库版本、物种、置信度阈值和证据通道。
3. 区分实验支持的物理互作、数据库整理的互作、共表达、共现、基因邻近和同源转移等证据。
4. 根据研究目的决定仅展示家族成员间关系，还是加入第一层候选互作蛋白；避免无控制扩展网络。
5. 在 Cytoscape 中按证据类型、置信度、家族亚群或功能模块设置节点和边属性。
6. 可计算 degree、betweenness 等网络指标，但应说明网络规模、阈值和拓扑指标的局限。
7. 对重要候选互作，提出可验证的实验设计，例如 Y2H、BiFC、Co-IP 或 pull-down。

### 质量控制与解释边界

- STRING 的“functional association”不等同于直接物理结合。
- 预测、共表达和同源转移证据应与实验验证证据分开标识。
- 网络高度依赖数据库覆盖范围、物种映射和置信度阈值。
- Hub 节点不一定是生物学上的关键调控因子。
- 不得将预测网络描述为已经验证的蛋白质互作。

### 输出

ID 映射表、互作边表、节点属性表、证据来源表、Cytoscape 网络文件和网络图。

## English Version

### Objective

Build a network of target family members and candidate interacting proteins to explore potential functional relationships and network modules while documenting the evidence behind each connection.

### Inputs and Tools

Use standardized protein or gene IDs, species information, and the family-member list. Resources may include STRING, BioGRID, and IntAct. Cytoscape can be used for network visualization and analysis.

### Workflow

1. Map target IDs to species-specific protein identifiers and record members that cannot be mapped.
2. Retrieve interaction or functional-association data and record database versions, species, confidence thresholds, and evidence channels.
3. Distinguish experimentally supported physical interactions, curated interactions, co-expression, co-occurrence, genomic neighborhood, and homology-transfer evidence.
4. Decide whether to display only relationships among family members or include first-shell candidate interactors. Avoid uncontrolled network expansion.
5. In Cytoscape, encode evidence type, confidence, subfamily, or functional module as node and edge attributes.
6. Network metrics such as degree and betweenness may be calculated, but document network size, thresholds, and metric limitations.
7. Propose experimental tests for important candidate interactions, such as Y2H, BiFC, Co-IP, or pull-down assays.

### Quality Control and Interpretation Limits

- A STRING functional association is not necessarily direct physical binding.
- Keep predicted, co-expression, and homology-transfer evidence separate from experimental validation.
- Networks depend strongly on database coverage, species mapping, and confidence thresholds.
- A hub node is not automatically a biologically essential regulator.
- Never describe a predicted network as experimentally validated protein interaction.

### Outputs

ID mapping table, interaction edge table, node-attribute table, evidence-source table, Cytoscape network file, and network figure.
