---
icon: material/book-cog-outline
---

# 知识管理 Skill 设计

这个 Skill 的目标不是“让 Agent 多写一点”，而是让它按固定规则维护知识库。

## 触发场景

当用户说：

- 整理这篇文章
- 把这段内容放入知识库
- 建一个主题索引
- 整理 Inbox
- 做本周知识回顾

就应该触发知识管理 Skill。

## Skill 规则

```markdown
---
name: knowledge-manager
description: Organize Obsidian vault notes, intake new content, update MOCs, and maintain wikilinks.
---

# Workflow

1. Read `CLAUDE.md` and vault structure.
2. Search existing notes before creating new notes.
3. Put raw or uncertain content into `Inbox/`.
4. Promote stable notes into `Notes/`.
5. Update relevant `MOCs/` pages.
6. Preserve sources and links.
7. Report changed files and unresolved questions.
```

## 笔记模板

```markdown
---
type: note
source:
tags:
created:
status: inbox
---

# 标题

## 摘要

## 关键观点

## 相关链接

## 待确认
```

## 验收标准

- 没有重复创建明显同义笔记。
- 新笔记有来源。
- 主题笔记有 wikilink。
- 修改过的文件清楚列出。
- 不确定的内容进入 `待确认`，而不是编造。

下一步：[完整工作流](workflow.md)。
