---
name: linux101-writing
description: Use when writing or editing AgentTutorial MkDocs pages with the Linux 101-inspired tutorial structure, Prettier Markdown formatting, heading IDs, admonition rules, and Chinese prose cleanup.
---

# Linux 101 Writing

Use this project-local skill when editing `docs/**/*.md`, `mkdocs.yml`, or tutorial writing rules in this repository.

## Source Reference

The original LUG@USTC Linux 101 writing guide is stored at `references/writing.md`. Read it when you need the source wording or want to compare a proposed rule with Linux 101.

## Required Page Shape

- Use exactly one H1 per page; do not add an ID to H1.
- Start正文页面 with `!!! abstract "导言"` and leave one blank line before its body.
- Add stable IDs to H2 and lower headings, such as `## 验证 {#check}`.
- Prefer this sequence: 目标, 背景, 步骤, 验证, 常见误区, 下一步.
- Keep chapter pages practical. A reader should know what to do, how to check it, and where to continue.

## Admonitions

- Keep `!!! abstract "导言"` expanded.
- Use folded blocks for all other admonitions: `??? info`, `??? warning`, `??? example`, and similar.
- Leave one blank line after every admonition title line.
- Do not put copyable Prompt, commands, code, config, or templates inside admonitions. Put them in ordinary fenced code blocks.

## Prose Rules

- For chapter 3 onward, avoid repeated translated patterns such as `不是……而是……`, `是……不是……`, `……而非……`, and `而不是`.
- Avoid comma splices. When two short clauses have a relationship, name the relationship with words such as `因此`, `当……时`, `如果……就`, `并`, `以及`, or `从而`.
- Favor stable criteria and validation checklists over time-sensitive product recommendations.

## Validation

Run these checks before finishing meaningful edits:

```powershell
npm run fix
npm run check
uv run mkdocs build --strict
```

Useful scans:

```powershell
rg -n "!!! " docs -g "*.md"
rg -n "不是|而是|而不是|而非" docs/pre-agent docs/first-task docs/prompt-plan docs/goal-running docs/skill-mcp docs/create-skill docs/practice-obsidian -g "*.md"
```
