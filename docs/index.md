---
icon: material/home-outline
---

# Agent 新手教程

这份教程面向没有系统使用过命令行 Agent 工具的读者。

本教程的主线有两条：

- **Coding CLI**：以 Claude Code 为例，教你如何在本地项目里对话、计划、修改文件、管理上下文。
- **龙虾类应用 （OpenClaw / Hermes）**：把 Agent 放进聊天入口和定时任务里，用来做长期知识摄取和提醒。

## 学习路线 {#route}

1. [从头了解 Agent](01-agent/00-index.md)：什么是 Agent？它和大模型（LLM）有什么关系？Agent 是如何从 ReAct、workflow，演化到如今（2026年）以 Coding CLI、self-improve agent 为主要形式的？
2. [如何选择和购买 Agent 服务](02-choose/00-index.md)：根据自身需求和财力，选择合适的付费服务进行购买。
3. [开始之前](03-pre-agent/00-index.md)：确认你该如何让 Agent 读取项目，并学会先要求它说明范围。
4. [第一次任务](04-first-task/00-index.md)：跑通一次小范围修改，从查看差异到确认结果。
5. [Prompt 与计划](05-prompt-plan/00-index.md)：把需求拆成目标、范围、约束和验证方式。
6. [长任务与目标](06-goal-running/00-index.md)：让 Agent 维持上下文，并持续报告进度。
7. [Skill 与 MCP](07-skill-mcp/00-index.md)：理解可复用工作流和外部工具接口。
8. [创建自己的 Skill](08-create-skill/00-index.md)：把项目写作规范封装成可复用说明。
9. [Obsidian 实战](09-practice-obsidian/00-index.md)：用 Claude Code + Obsidian 管理个人知识库。

## 阅读建议 {#reading}

本文默认你能使用计算机进行简单的日常办公、会按照教程打开命令行，且有一定的好奇心和探索欲望。

如果你是完完全全的计算机小白，我建议你先自行速览 [Missing Semester / 计算机教育中缺失的一课](https://missing-semester-cn.github.io/) 的最新教程。这里面将为你补充一些关于现代计算机的基础知识。

不建议跳过第一章和第二章。否则后面看到 `MCP`、`Skill`、`CLAUDE.md`、`Bot`、`定时任务` 时，很容易只会照抄命令，不知道什么时候该用哪个。

## 常用链接入口 {#links}

- [Claude Code 文档](https://code.claude.com/docs/en/overview)
- [Claude Code 安装与设置](https://code.claude.com/docs/en/setup)
- [Claude Code 官方文档](https://code.claude.com/docs/en/overview)
- [OpenAI ChatGPT 定价](https://chatgpt.com/pricing/)
- [OpenAI Codex 与 ChatGPT 计划](https://help.openai.com/en/articles/11369540-using-codex-with-your-chatgpt-plan)
- [Anthropic Claude 定价](https://claude.com/pricing)
- [Claude Code 与 Pro / Max 计划](https://support.anthropic.com/en/articles/11145838-using-claude-code-with-your-pro-or-max-plan)
- [Obsidian CLI](https://help.obsidian.md/cli)

下一步：[从头了解 Agent](01-agent/00-index.md)
