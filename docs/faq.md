---
icon: material/help-circle-outline
---

# 常见问题（FAQ）

## 新手学习

??? question "我应该先学 Claude Code 还是 Hermes"
先学 Claude Code。它更容易理解 Agent 如何读文件、执行命令、修改内容。Hermes 更适合在你已经有稳定工作流后，把任务放进聊天入口和定时任务里长期运行。

??? question "MCP 和 Skill 哪个先学"
先学 Skill 的思维，再学 MCP。Skill 是“怎么做事”的操作手册，MCP 是“能调用什么工具”的接口。

## 订阅和购买

??? question "订阅价格可以直接照教程买吗"
不建议。价格、额度、地区和可用功能经常变化，购买前以 [OpenAI 定价](https://chatgpt.com/pricing/) 和 [Anthropic 定价](https://claude.com/pricing) 为准。

??? question "只想学 Coding CLI，买哪个更稳"
先看你准备主要使用哪个产品。Claude Code 直接看 Anthropic 的 Pro / Max / Console 说明；Codex 看 OpenAI 的 ChatGPT 计划和 Codex rate card。

## 本地安装

??? question "Windows 上 `claude` 命令不存在"
先重新打开 PowerShell，再运行 `claude --version`。如果仍然找不到，回到 [官方安装文档](https://code.claude.com/docs/en/setup) 检查安装路径。

??? question "路径包含中文或空格会不会有问题"
新手建议把项目和 Obsidian vault 放在短路径下，例如 `C:\Work\Vault`。等熟悉后再处理复杂路径。

## Obsidian

??? question "先用 obsidian-cli 还是 Obsidian MCP"
先用 obsidian-cli。它更直观，命令可见，便于排错。等知识库结构稳定后，再考虑 MCP。

??? question "`obsidian` 命令不可用"
确认 Obsidian 已打开，并且当前版本支持 [Command line interface](https://help.obsidian.md/cli)。然后重新打开终端运行 `obsidian help`。
