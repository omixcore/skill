# 服务器连接与任务执行规范 / Server Access and Task Workflow

## 中文版

### 1. 默认服务器

| 项目 | 默认值 |
| --- | --- |
| 主机地址 | `192.168.188.110` |
| SSH 用户 | `liangfei` |
| SSH 端口 | `20229` |
| 默认工作目录 | `/home/data/liangfei/WorkBuddy/` |

默认 SSH 命令：

```bash
ssh -p 20229 liangfei@192.168.188.110
```

密码不应写入本仓库、README、脚本、命令历史或任务日志。优先使用 SSH 密钥认证；如使用密码认证，应通过 SSH 交互式提示输入，不要将密码嵌入命令或自动化脚本。

### 2. 默认任务目录

除软件安装任务外，任务过程文件和结果默认保存在：

```text
/home/data/liangfei/WorkBuddy/
```

建议每个任务使用独立目录，避免不同项目的文件混杂：

```text
WorkBuddy/
└── Project_or_Task_Name/
    ├── input/
    ├── scripts/
    ├── results/
    ├── logs/
    └── README.md
```

- `input/`：任务输入文件及必要的原始数据副本。
- `scripts/`：分析脚本、配置文件和可复用命令。
- `results/`：分析输出、图表、报告和最终结果。
- `logs/`：运行日志、错误信息和验证记录。
- `README.md`：记录任务目的、运行步骤、环境、输出位置和完成状态。

可根据任务规模简化目录结构，但应保持文件归属清楚。除非用户另有要求，不覆盖或删除原始输入数据。

### 3. 软件安装例外

软件安装任务不受默认工作目录限制。应根据软件类型、操作系统、权限和依赖选择合适的安装位置及安装方式。

**验收目标是软件成功安装并能够正常使用，而不是仅下载完成或安装命令执行结束。**

安装任务应尽可能完成以下步骤：

1. 检查操作系统、CPU 架构、可用磁盘空间、权限和依赖。
2. 选择兼容的软件版本及合适的安装方式。
3. 执行安装并处理依赖冲突、环境变量和权限问题。
4. 检查实际安装路径和软件版本。
5. 运行软件自带的版本检查、帮助命令或最小测试，确认可以正常启动和调用。
6. 对需要额外配置的程序，完成必要配置后再次验证。
7. 记录安装方式、版本、安装路径、关键依赖、验证命令及结果。

如果安装失败，应继续排查并尝试合理的替代安装方案；遇到权限不足、网络限制、资源不足或需要用户授权等无法自行解决的阻碍时，明确说明具体原因和下一步操作，不得将未验证的安装报告为成功。

### 4. 任务执行与交付

- 连接后先检查主机、用户、磁盘空间、目录权限及运行环境。
- 普通任务默认在 `WorkBuddy/` 下建立独立任务目录。
- 尽量保留可复现的脚本、关键参数、日志和结果。
- 完成后核对输出文件是否存在、是否可读取，以及关键结果是否通过必要验证。
- 向用户报告任务状态、结果目录、主要输出和验证情况；区分已完成、部分完成和未完成事项。
- 软件安装可以使用系统推荐或用户指定的安装路径，不强制放入 `WorkBuddy/`；但应记录安装位置和验证结果。

### 5. 凭据与安全

- 不在 Git 仓库、明文配置文件、脚本、README、日志或提交信息中保存密码、私钥、访问令牌及其他凭据。
- 不使用明文密码拼接 SSH 命令，也不将密码写入 shell history。
- 优先采用 SSH 密钥认证，并妥善保护私钥。
- 对服务器上的删除、覆盖、系统级修改等高影响操作，应先确认目标和影响范围；不得为了完成普通任务擅自清理无关文件。
- 本文件只记录非敏感的连接参数和工作约定，不代表已配置免密登录。

## English Version

### 1. Default Server

| Item | Default value |
| --- | --- |
| Host | `192.168.188.110` |
| SSH user | `liangfei` |
| SSH port | `20229` |
| Default working directory | `/home/data/liangfei/WorkBuddy/` |

Default SSH command:

```bash
ssh -p 20229 liangfei@192.168.188.110
```

Do not store passwords in this repository, README files, scripts, shell history, or task logs. Prefer SSH key authentication. If password authentication is used, enter the password through the interactive SSH prompt; never embed it in a command or automation script.

### 2. Default Task Directory

Except for software installation tasks, save task files and results by default under:

```text
/home/data/liangfei/WorkBuddy/
```

Create a separate directory for each task to keep project files organized:

```text
WorkBuddy/
└── Project_or_Task_Name/
    ├── input/
    ├── scripts/
    ├── results/
    ├── logs/
    └── README.md
```

- `input/`: task inputs and necessary copies of original data.
- `scripts/`: analysis scripts, configuration files, and reusable commands.
- `results/`: analysis outputs, figures, reports, and final results.
- `logs/`: execution logs, error messages, and verification records.
- `README.md`: task objectives, execution steps, environment, output locations, and completion status.

The directory structure may be simplified for small tasks, but file ownership and organization must remain clear. Do not overwrite or delete original input data unless the user requests it.

### 3. Software Installation Exception

Software installation tasks are exempt from the default working-directory requirement. Choose an appropriate installation location and method based on the software, operating system, permissions, and dependencies.

**The acceptance criterion is successful installation and normal operation—not merely a completed download or an installation command that exits.**

Where possible, complete the following steps:

1. Check the operating system, CPU architecture, available disk space, permissions, and dependencies.
2. Select a compatible software version and installation method.
3. Install the software and resolve dependency conflicts, environment variables, and permission issues.
4. Verify the actual installation path and software version.
5. Run the software's version check, help command, or a minimal test to confirm that it starts and can be invoked.
6. Complete any required configuration and test the software again.
7. Record the installation method, version, path, key dependencies, verification commands, and results.

If installation fails, continue troubleshooting and try reasonable alternative installation methods. If blocked by insufficient permissions, network restrictions, resource limitations, or required user authorization, explain the specific cause and next steps. Never report an unverified installation as successful.

### 4. Task Execution and Delivery

- After connecting, check the host, user, disk space, directory permissions, and runtime environment.
- Create a dedicated task directory under `WorkBuddy/` for ordinary tasks.
- Preserve reproducible scripts, key parameters, logs, and results whenever possible.
- Verify that output files exist, are readable, and pass the necessary checks.
- Report the task status, result directory, key outputs, and verification status; distinguish completed, partially completed, and unfinished work.
- Software may be installed in a system-recommended or user-specified location rather than `WorkBuddy/`, but its installation path and verification results must be recorded.

### 5. Credentials and Security

- Never store passwords, private keys, access tokens, or other credentials in Git repositories, plaintext configuration files, scripts, README files, logs, or commit messages.
- Do not concatenate plaintext passwords into SSH commands or write them to shell history.
- Prefer SSH key authentication and protect private keys appropriately.
- Before high-impact operations such as deletion, overwriting, or system-level changes, confirm the target and scope. Do not remove unrelated files to complete an ordinary task.
- This document records only non-sensitive connection settings and workflow conventions; it does not imply that passwordless login has been configured.
