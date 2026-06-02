---
icon: material/puzzle-outline
---

# MCP 和 Skill 是什么

新手经常把 MCP 和 Skill 混在一起。可以这样区分：

```text
MCP = 给 Agent 工具
Skill = 教 Agent 怎么做事
```

## MCP

MCP 让 Agent 能调用外部工具或服务。

例子：

- 读 Obsidian vault
- 查数据库
- 控制浏览器
- 调用飞书 API
- 访问内部系统

官方入口：[Claude Code MCP](https://code.claude.com/docs/en/mcp)。

## Skill

Skill 是一套操作手册。它告诉 Agent 在某类任务里应该怎么判断、怎么执行、怎么验收。

例子：

- 知识管理 Skill
- 周报 Skill
- 文献综述 Skill
- 数据分析 Skill

官方入口：[Claude Code Skills](https://code.claude.com/docs/en/skills)。

## 组合使用

一个完整任务经常两者都用：

```text
MCP 负责连接 Obsidian
Skill 负责规定怎么写笔记、怎么建 MOC、怎么避免重复
```

下一步：[安装常用 MCP 和 Skill](install-extensions.md)。
