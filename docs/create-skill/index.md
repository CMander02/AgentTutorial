---
icon: material/hammer-wrench
---

# 创建自己的 Skill

!!! abstract "导言"

    当你连续几次给 Agent 解释同一套规则时，就可以把这些规则写成 Skill。Skill 的价值在于减少重复沟通，并让 Agent 在相似任务中保持一致做法。

## 目标 {#goal}

本章会创建一个项目级 Skill。完成后，你应该知道：

- Skill 放在哪里。
- `SKILL.md` 需要哪些字段。
- 什么时候把长资料放进 `references/`。
- 如何验证 Skill 没有写偏。

## 目录结构 {#structure}

项目级 Skill 可以放在仓库内：

```text
.codex/
└── skills/
    └── linux101-writing/
        ├── SKILL.md
        └── references/
            └── writing.md
```

`SKILL.md` 放核心流程，`references/` 放较长的参考资料。这样 Agent 只有在需要时才读取大文件。

## 最小 SKILL.md {#minimal}

一个最小 Skill 需要 frontmatter 和正文：

```markdown
---
name: linux101-writing
description: Use when writing or editing AgentTutorial MkDocs pages with the Linux 101-inspired tutorial structure, Prettier Markdown formatting, heading IDs, admonition rules, and Chinese prose cleanup.
---

# Linux 101 Writing

Use this project-local skill when editing docs/**/*.md.

## Required Page Shape

- Use exactly one H1 per page.
- Start正文页面 with the project intro admonition.
- Add stable IDs to H2 and lower headings.
- Run npm run check and uv run mkdocs build --strict before finishing.
```

描述字段要写清触发场景。正文要短，优先写流程、规则和验证命令。

## 引用资料 {#references}

当资料很长时，不要全部塞进 `SKILL.md`。可以放到：

```text
.codex/skills/linux101-writing/references/writing.md
```

然后在 `SKILL.md` 中写明何时读取它。

## 验证 Skill {#check}

创建后做一次快速验证：

```powershell
Get-ChildItem .codex\skills\linux101-writing -Recurse
npm run check
uv run mkdocs build --strict
```

再用一个小任务试触发：

```text
请按 linux101-writing 规则检查 docs/pre-agent/index.md，只给问题清单，先不要修改文件。
```

## 常见误区 {#pitfalls}

??? warning "把 Skill 写得太长"

    Skill 应优先提供操作方法。长篇背景、完整资料和示例库应放进引用文件。

??? warning "缺少验证命令"

    没有验证命令时，Skill 很难形成稳定闭环。每个项目级 Skill 都应写明最小检查方式。

## 下一步 {#next}

下一章：[Obsidian 实战](../practice-obsidian/index.md)。
