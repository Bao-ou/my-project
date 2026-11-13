# My Project

个人工作仓库。目前处于起步阶段，先把本地开发环境和 GitHub 通道跑通，后续再填充实际内容。

## 环境状态

本仓库已配置 SSH 认证，克隆与推送全程免密：

| 项目 | 值 |
| --- | --- |
| 认证方式 | SSH（ed25519） |
| 私钥位置 | `~/.ssh/id_ed25519` |
| 提交身份 | `Bao-ou <355868472+Bao-ou@users.noreply.github.com>` |
| 默认分支 | `main` |

机器环境：macOS 13.7.8（arm64），git 2.39.2（Apple Git-143）。

> 提交邮箱使用的是 GitHub 官方 noreply 地址（`<用户ID>+<用户名>@users.noreply.github.com`）。好处是不必公开真实邮箱，同时提交仍能正确归属到账号并计入贡献图。

## 常用操作

```bash
# 克隆
git clone git@github.com:Bao-ou/my-project.git

# 日常提交
git add -A
git commit -m "feat: 说明这次改了什么"
git push

# 从远端同步
git pull --no-rebase
```

在 WorkBuddy 对话里也能直接操作这个仓库：创建分支、读写文件、提 Issue 和 PR 都支持，不依赖本地 git 环境。

## 环境备忘

**GitHub 资源下载**：直连 `github.com/.../releases/download/...` 经常超时，前面加 `https://gh-proxy.com/` 可显著加速（实测 5.3 MB/s）：

```bash
curl -L -o gh.zip \
  "https://gh-proxy.com/https://github.com/cli/cli/releases/download/v2.104.0/gh_2.104.0_macOS_arm64.zip"
```

**gh CLI**：已安装 2.104.0 至 `~/.local/bin/gh`（该目录已在 PATH 中）。当前未登录，需要终端操作时执行：

```bash
gh auth login --git-protocol ssh --web
```

**Homebrew**：本机未安装。如需用它管理软件包，需要先安装 brew。

## 目录结构

```
.
├── README.md    # 本文件：环境说明与操作备忘
└── .gitignore   # 忽略系统文件、依赖目录与构建产物
```

## 后续计划

- [ ] 确定项目方向，填充实际代码
- [ ] 按需补充 CI 配置
- [ ] 视项目类型完善 `.gitignore`
