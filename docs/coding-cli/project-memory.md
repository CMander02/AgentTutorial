---
icon: material/file-document-outline
---

# 管理 CLAUDE.md / AGENTS.md

`CLAUDE.md` 和 `AGENTS.md` 都可以理解成“写给 Agent 的项目说明书”。它们让 Agent 每次进入项目时不用从零理解你的约定。

## 应该写什么

- 项目目标
- 目录结构
- 常用命令
- 测试和构建方式
- 写作风格
- 不允许修改的范围
- 验收标准

## 最小模板

```markdown
# Project Guide

## Goal
这个项目用于编写 Agent 新手教程。

## Commands
- Preview: `uv run mkdocs serve`
- Build: `uv run mkdocs build --strict`

## Rules
- 文档默认使用中文。
- 修改前先说明计划。
- 不要伪造未验证的官方命令。
- 订阅价格和产品能力必须链接官方页面。
```

## CLAUDE.md 和 AGENTS.md 怎么选

- 主要使用 Claude Code：优先写 `CLAUDE.md`。
- 希望兼容多个 Coding CLI：可以再写 `AGENTS.md`。
- 两者都存在时，保持核心规则一致，避免互相矛盾。

## 维护方法

当你发现自己连续三次给 Agent 解释同一条规则，就应该把它写进项目记忆文件。

下一步：[使用 /plan、/goal 和历史记录](project-progress.md)。
