---
icon: material/sitemap-outline
---

# 目标和架构

这个实战不追求复杂插件，而是先建立一个 Agent 友好的知识库。

## 目标

- Claude Code 能读懂 vault 结构。
- 新内容先进入 Inbox。
- 长期笔记进入 Notes。
- 主题索引进入 MOCs。
- Agent 修改前先搜索，避免重复笔记。
- 每次整理都有可验证结果。

## 架构

```text
Claude Code
  -> 读取 CLAUDE.md / AGENTS.md
  -> 通过文件系统、obsidian-cli 或 Obsidian MCP 操作 vault
  -> 按知识管理 Skill 整理内容
  -> 写入 Inbox / Notes / MOCs / Daily
```

## 为什么先做本地

本地知识库更适合新手，因为文件都在你能看到的位置。你可以直接检查 Markdown、Git diff、Obsidian 预览和链接关系。

下一步：[Obsidian vault 设计](vault-design.md)。
