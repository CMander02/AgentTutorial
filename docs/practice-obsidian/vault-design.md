---
icon: material/folder-outline
---

# Obsidian vault 设计

一个适合 Agent 维护的 vault 不需要复杂，但必须有明确分区。

## 推荐目录

```text
Vault/
├── CLAUDE.md
├── Inbox/
├── Notes/
├── MOCs/
├── Daily/
├── Sources/
└── Templates/
```

## 目录含义

| 目录 | 用途 |
| --- | --- |
| `Inbox/` | 临时内容，允许粗糙 |
| `Notes/` | 整理后的长期笔记 |
| `MOCs/` | 主题索引和知识地图 |
| `Daily/` | 每日记录、临时任务 |
| `Sources/` | 原文、摘录、来源记录 |
| `Templates/` | 固定笔记模板 |

## 最小 CLAUDE.md

```markdown
# Vault Rules

- 默认使用中文。
- 新内容先放入 `Inbox/`。
- 整理后的长期笔记放入 `Notes/`。
- 主题索引放入 `MOCs/`。
- 修改前先搜索相似笔记，避免重复创建。
- 长期笔记必须包含来源、摘要、关键观点和相关链接。
- 不确定分类时不要强行归档，先保留在 `Inbox/`。
```

下一步：[知识库接入方式](access.md)。
