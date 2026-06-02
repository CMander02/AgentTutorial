---
icon: material/download-outline
---

# 本地安装 Claude Code

本页以 Windows + PowerShell 为主。安装命令可能变化，执行前请以 [Claude Code 官方设置文档](https://code.claude.com/docs/en/setup) 为准。

## 前置条件

- Windows 10/11
- PowerShell
- Git for Windows
- Claude 账号或 Anthropic API Key

## 安装

在 PowerShell 中运行：

```powershell
irm https://claude.ai/install.ps1 | iex
```

验证：

```powershell
claude --version
```

启动：

```powershell
claude
```

首次启动按提示登录。

## 第一次进入项目

选择一个你愿意让 Claude Code 读取的目录：

```powershell
cd C:\Work\my-project
claude
```

先发一个只读任务：

```text
请阅读这个项目的目录结构和 README，说明它是做什么的。先不要修改任何文件。
```

## 新手安全习惯

- 第一次用新项目时，先让它只读。
- 涉及删除、迁移、批量修改时，要求先给计划。
- 不要在不了解后果时让它自动执行危险命令。
- 使用 Git 项目时，修改前先看 `git status`。

下一步：[第一次交互和提问方式](interaction.md)。
