# skill

个人常用指令库，用于集中保存和维护通用分析原则、写作、科研绘图、GitHub 推送、服务器任务及日常工作中的可复用指令。

## 指令分类

| 分类 | 内容 | 建议存放位置 |
| --- | --- | --- |
| 通用原则 | 独立判断、前提检查、逻辑审查、数字核实、证据与不确定性表达 | `principles/` |
| 写作 | 论文撰写与修改、分析方法 Word 文档、文献真实性与支撑性核查、中英文翻译、作者信息、基金与利益冲突声明、图例、投稿信、审稿回复 | `writing/` |
| 绘图 | 科研图片排版、字体与线条规范、参考图风格/配色/布局复现、热图、通路图、SVG 图标 | `plotting/` |
| GitHub 推送 | 文件上传、README 更新、提交整理、版本发布与页面更新 | `github/` |
| 服务器任务 | SSH 连接、默认工作目录、任务文件组织、软件安装与验证 | `server/` |
| 日常整理 | 文件命名、格式转换、资料归档及重复性任务 | `routine/` |

具体指令将按以上分类逐步补充。

## 已收录指令

- [独立判断与证据核查原则 / Independent Reasoning and Evidence Verification](principles/independent-reasoning-and-verification.md)：回答前检查错误前提、逻辑跳跃和信息缺失；保持独立判断，不迎合用户；核实数字来源和计算；发现错误时直接指出并提供依据。

- [分析方法 Word 文档规范 / Analysis Methods Word Document Standard](writing/analysis-methods-word-standard.md)：正式科研分析任务默认提供英文版可编辑 `.docx` 方法文档；Times New Roman、12 pt，一级和二级标题黑色加粗并使用真实 Word 标题样式；内容须忠实记录实际执行的分析流程、软件版本、参数和统计方法。

- [文献引用真实性与支撑性核查规范 / Reference Authenticity and Claim-Support Verification](writing/reference-verification.md)：引用前先确认文献真实存在，再检查原文是否能够支撑对应的具体语句；核对研究对象、实验条件、证据类型和结论强度，完成核查后才引用。

- [常用论文作者信息 / Standard Manuscript Author Information](writing/author-information.md)：记录常用作者顺序、单位、共同第一作者标记、邮箱及通讯作者信息，供论文初稿和投稿材料复用；具体稿件仍需核对实际作者贡献与期刊格式。

- [默认基金与利益冲突声明 / Default Funding and Conflict of Interest Statements](writing/funding-conflict-statements.md)：收录常用基金资助声明及默认无利益冲突声明，并提供逐篇论文核对规则。

- [GitHub 提交与推送身份规范 / GitHub Commit and Push Identity Policy（中英文）](github/commit-push-identity.md)：使用仓库持有账号提交和推送，不引入 bot、Codex 或其他 AI／自动化账号署名。

- [科研绘图统一标准 / Scientific Figure Standards（中英文）](plotting/figure-standards.md)：A4 竖版、Arial 7 pt、纯黑色文字与 0.5 pt 线条，优先输出各元素可编辑的 PDF 和 SVG；同时要求参考用户提供的图片，模仿其风格、配色和排版布局。

- [绘图参考图片库 / Plotting Reference Gallery](plotting/references/README.md)：归档原始参考图片，并记录图片来源、配色和布局特征，供后续绘图复用。

- [服务器连接与任务执行规范 / Server Access and Task Workflow](server/ssh-workflow.md)：记录默认 SSH 主机、端口、用户、普通任务保存目录，以及软件安装必须以安装成功并通过运行验证为目标的工作约定。

## 使用方式

1. 每条独立指令保存为一个 Markdown 文件，文件名应说明用途。
2. 使用时复制相应指令，并补充本次任务的文件、目标、参数及输出位置。
3. 对经常重复的要求持续修订，保留适用范围和必要的例外说明。
4. 处理事实判断、科研推理、定量结论和方案评估时，优先遵循 `principles/independent-reasoning-and-verification.md`。
5. 撰写论文或综述时，所有引用必须先遵循 `writing/reference-verification.md` 完成文献真实性和语句支撑性核查，再加入正文与参考文献列表。
6. 正式科研分析任务完成时，默认按照 `writing/analysis-methods-word-standard.md` 提供英文版 Word Methods 文档，并与实际脚本、日志、图表和结果核对一致。
7. 绘图前先检查 `plotting/references/` 中的参考图片；本次任务提供的新参考图片也应一并归档并推送到仓库。
8. 服务器普通任务默认遵循 `server/ssh-workflow.md`；软件安装任务按实际系统环境选择安装位置，并以运行验证通过为验收依据。

## 指令记录格式

每条独立指令建议包含：

- **用途**：适用于什么任务。
- **输入**：需要提供的文件、数据或背景信息。
- **指令正文**：可以直接复制使用的完整要求。
- **输出要求**：文件格式、命名、排版或提交方式。
- **检查要点**：完成后需要核对的内容。

## 维护原则

- 指令以清晰、具体、可复用为主，项目特定信息在使用时补充。
- 通用分析应优先检查前提和逻辑，保持独立判断；涉及数字时核实来源或计算，纠错时说明证据与依据。
- 写作引用必须核实文献真实性及其对具体语句的支撑程度；不得引用虚构文献、错误书目信息或仅因主题相似而不支持当前主张的文献。
- 分析方法文档必须依据真实执行记录撰写；缺失信息明确标记待核实，不得编造参数、软件版本、实验条件或未执行的步骤。
- 写作指令应保留原始数据、研究结果与引用的真实性。
- 作者信息模板仅作为常用起点；每篇论文均须按真实作者贡献、作者顺序、单位和期刊要求核对。
- 基金与利益冲突声明作为默认模板使用，但每篇论文均须核实真实资助关系、实际利益冲突及目标期刊要求。
- 绘图指令应明确尺寸、字体、字号、线宽、颜色及可编辑性，并优先遵循已归档参考图的视觉风格。
- 服务器任务应保留必要的运行记录和验证结果；密码、私钥、访问令牌等凭据不得写入仓库、脚本或日志。
- GitHub 操作指令应明确账号、仓库、分支和本次修改范围；保存的指令不代表已经执行相应操作。
- 不在仓库中保存密码、访问令牌或其他凭据。
