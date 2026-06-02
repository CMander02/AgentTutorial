---
icon: material/inbox-arrow-down-outline
---

# 知识摄入 Skill 设计

知识摄入 Skill 负责把外部内容变成知识库可处理的中间格式。

## Skill 草案

```markdown
---
name: knowledge-ingestion
description: Intake web links, pasted content, bot messages, and scheduled sources into an Obsidian knowledge vault.
---

# Workflow

1. Preserve original source.
2. Extract title, source, time, and content type.
3. Check whether similar content already exists.
4. Summarize in Chinese.
5. Extract key points and action items.
6. Assign status: raw, inbox, review, note, or discarded.
7. Write to Inbox or Sources.
8. Suggest MOC links without inventing files.
```

## 输出模板

```markdown
---
type: intake
source:
source_type:
captured_at:
status: inbox
tags:
---

# 标题

## 一句话摘要

## 关键观点

## 可行动项

## 推荐链接

## 原始内容
```

## 与知识管理 Skill 的关系

知识摄入 Skill 负责“进来”；知识管理 Skill 负责“整理好”。不要让一个 Skill 同时做抓取、总结、归档、重构 MOC 和周回顾。

下一步：[定时摄取和回顾](schedule.md)。
