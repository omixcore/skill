# 项目与软件版本号统一规范 / Unified Version Standard for Projects and Software

## 中文版

### 1. 统一版本号

所有自主开发或委托开发的项目、软件、应用、工具、程序包、脚本框架及其他可交付的软件成果，其项目自身的版本号统一使用 **`0.0.1`**。

### 2. 全部位置保持一致

同一项目中的版本号必须保持一致，包括但不限于：

- README、项目说明和用户手册；
- 源代码中的版本常量及应用程序的 About/关于页面；
- 软件包和构建配置文件，例如 R 的 `DESCRIPTION`、Python 的 `pyproject.toml`、`setup.py`，JavaScript 的 `package.json`、Java 的 Maven/Gradle 配置；
- 安装包元数据、发布说明、项目网站及文档中的版本标识。

### 3. 不得擅自升版或改变格式

- 默认版本号始终写为 **`0.0.1`**。
- 未经用户明确要求，不得自行改为 `0.1.0`、`1.0.0`、日期版本或其他编号。
- 不得在同一项目的不同文件、界面或文档中混用不同版本号。
- 创建 Release 或版本标签时，也应使用 `0.0.1`，不要自行添加不同的版本编号。

### 4. 适用范围边界

本规范约束的是项目或软件**自身的版本号**，不适用于第三方依赖、编程语言运行环境、外部软件、API、数据库、参考基因组或数据集等各自独立的真实版本号。这些外部版本信息必须如实保留，不得为了统一而篡改。

### 5. 交付前核查

每次创建或更新项目时，检查项目配置、README、源代码、界面、文档和发布信息中的版本号，确认项目自身版本均为 **`0.0.1`**。如发现不一致，应在交付前统一修正。

只有用户明确指定其他版本号时，才按用户要求执行。

## English Version

### 1. Unified Version Number

Use **`0.0.1`** as the standard version number for every independently developed or commissioned project, software application, tool, package, script framework, and other deliverable software product. This rule applies to the project's own version number.

### 2. Maintain Consistency Across All Locations

Keep the project version consistent wherever it appears, including but not limited to:

- README files, project descriptions, and user manuals;
- Version constants in source code and the application's About page;
- Package and build configuration files, such as R `DESCRIPTION`, Python `pyproject.toml` and `setup.py`, JavaScript `package.json`, and Java Maven/Gradle configurations;
- Installer metadata, release notes, project websites, and documentation.

### 3. Do Not Change or Increment the Version Without Authorization

- The default project version must remain **`0.0.1`**.
- Do not independently change it to `0.1.0`, `1.0.0`, a date-based version, or any other numbering scheme unless the user explicitly requests it.
- Never use inconsistent project version numbers across files, interfaces, or documentation.
- When creating a Release or version tag, use `0.0.1`; do not introduce another version number without authorization.

### 4. Scope and Exceptions

This standard governs only the **project's own version number**. It does not apply to the independently versioned third-party dependencies, language runtimes, external software, APIs, databases, reference genomes, or datasets used by the project. Preserve these external version identifiers accurately; never alter them merely to enforce this standard.

### 5. Pre-delivery Verification

Whenever a project is created or updated, inspect its configuration files, README, source code, interface, documentation, and release information. Confirm that every occurrence of the project's own version number is **`0.0.1`** and correct any inconsistencies before delivery.

Use a different version number only when the user explicitly specifies it.
