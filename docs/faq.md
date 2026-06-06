---
icon: material/help-circle-outline
---

# 常见问题

!!! abstract "导言"

    这一页收集新手最容易卡住的问题。遇到问题时，先判断它属于概念、选型、终端、长任务、Skill、MCP 还是 Obsidian，再回到对应章节复查。

## 学习顺序 {#learning}

??? question "应该先学哪个工具"

    先学能在本地验证的 Coding CLI。网页聊天适合探索问题，Coding CLI 适合建立文件、命令和验证闭环。

??? question "可以跳过第 1、2 章吗"

    如果你已经理解 Agent 的环境、工具和反馈闭环，可以快速浏览。若这些概念还模糊，后面使用 Skill 和 MCP 时会更难判断边界。

## 选型购买 {#buying}

??? question "教程能给固定购买推荐吗"

    不建议依赖固定推荐。价格、额度、地区和产品功能变化很快，购买前应按 [购买前验证清单](choose/how-to-buy-us-services.md) 重新核对官方信息。

??? question "免费工具够用吗"

    足够做入门练习。进入真实项目后，要重点观察任务成功率、失败恢复、上下文额度和数据边界。

## 本地任务 {#local}

??? question "Windows 上命令找不到怎么办"

    先重新打开 PowerShell，再运行对应的版本检查命令。若仍然失败，回到工具官方安装文档检查 PATH。

??? question "路径包含中文或空格会影响使用吗"

    可能影响部分命令和脚本。新手练习建议使用短路径，例如 `C:\Work\AgentPractice`。

??? question "Agent 说完成了，我还要检查什么"

    看 `git diff`、验证命令输出和页面效果。长任务还要检查它是否列出剩余风险。

## Skill 与 MCP {#skill-mcp}

??? question "先学 Skill 还是 MCP"

    先学 Skill。Skill 让做事方法稳定下来，MCP 再把必要工具接入进来。

??? question "什么时候该写项目级 Skill"

    当你连续几次解释同一套项目规则、页面结构或验证命令时，就该沉淀成 Skill。

## Obsidian {#obsidian}

??? question "Obsidian vault 要先设计得很复杂吗"

    不需要。先用 Inbox、Notes、MOCs、Daily、Sources 和 Templates 这类简单结构，等真实使用后再扩展。

??? question "整理知识库时怎样降低风险"

    先小样本处理，保留来源，使用待确认标记，并通过 Git diff 或备份检查每次改动。
