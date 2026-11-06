# GitHub 提交与推送身份规范 / GitHub Commit and Push Identity Policy

## 中文版

所有提交和推送必须使用仓库持有账号的身份与授权。提交作者（author）、提交者（committer）及推送账号均须对应仓库持有账号。不得引入 bot、Codex 或其他 AI／自动化账号作为作者、提交者、共同作者或推送者，也不得自动添加相关署名或提交尾注。操作前核验身份；无法满足时暂停推送，不得使用其他身份代替。

### 检查要点

- 核对目标仓库、仓库所有者、目标分支及当前认证账号。
- 核对提交作者和提交者，确保均对应仓库持有账号。
- 核对提交信息及共同作者尾注，不添加 bot、Codex 或其他 AI／自动化账号署名。
- 使用仓库持有账号的授权执行推送，不自动切换到其他已连接账号。
- 推送完成后核对实际提交的作者、提交者及提交信息。
- 对应账号未登录、授权不可用或身份无法确认时，暂停推送并说明原因。

## English Version

All commits and pushes must use the repository owner's identity and authorization. The commit author, committer, and pushing account must correspond to the repository owner. Do not introduce bots, Codex, or other AI or automation accounts as authors, committers, co-authors, or pushers, or automatically add their attribution or commit trailers. Verify identities before proceeding. If these requirements cannot be met, pause rather than substitute another identity.

### Verification checklist

- Check the target repository, repository owner, target branch, and currently authenticated account.
- Verify that both the commit author and committer correspond to the repository owner's account.
- Review commit messages and co-author trailers; do not add attribution to bots, Codex, or other AI or automation accounts.
- Push using the repository owner's authorization without automatically switching to another connected account.
- After pushing, verify the actual commit author, committer, and commit message.
- If the owner's account is not signed in, authorization is unavailable, or the identity cannot be verified, pause the push and explain why.
