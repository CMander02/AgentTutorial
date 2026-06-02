---
icon: material/connection
---

# 知识库接入方式

这一页合并讲 `obsidian-cli` 和 Obsidian MCP。它们都是让 Agent 接触 Obsidian vault 的方式，不需要拆成两条学习线。

## 三种方式

| 方式 | 优点 | 适合阶段 |
| --- | --- | --- |
| 直接读写 Markdown 文件 | 最简单、最透明 | 入门和排错 |
| obsidian-cli | 能调用 Obsidian 的搜索、读取、追加等能力 | 本地实战首选 |
| Obsidian MCP | 更像工具接口，适合复杂集成 | 规则稳定后再用 |

## 推荐顺序

```text
先直接读写 Markdown
再用 obsidian-cli
最后考虑 Obsidian MCP
```

这样做的好处是排错简单：你能清楚知道问题来自文件、CLI 还是 MCP。

## obsidian-cli 验证

官方入口：[Obsidian CLI](https://help.obsidian.md/cli)。

常用命令：

```powershell
obsidian help
obsidian search query="Claude Code" limit=10
obsidian read file="Claude Code"
obsidian daily:append content="- [ ] 整理 Inbox"
```

## MCP 适合什么时候

当你已经有稳定的 vault 结构和知识管理 Skill，并且需要更复杂的工具调用时，再接入 MCP。

接入 MCP 前先确认：

- MCP server 是否维护活跃。
- Windows 下启动命令是否正确。
- 它能访问的 vault 范围是否明确。
- 失败时能不能看到日志。

下一步：[知识管理 Skill 设计](knowledge-skill.md)。
