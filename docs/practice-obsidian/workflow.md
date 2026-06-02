---
icon: material/play-circle-outline
---

# 完整工作流

下面三个任务可以直接复制给 Claude Code。

## 1. 初始化 vault

```text
这是一个 Obsidian vault。请先阅读目录结构，创建或更新 CLAUDE.md。
规则：
1. 使用 Inbox / Notes / MOCs / Daily / Sources / Templates。
2. 新内容先进入 Inbox。
3. 修改前先说明计划。
4. 完成后列出修改过的文件。
```

## 2. 摄入一篇文章

```text
请把下面这篇文章整理进 Obsidian vault：

<粘贴文章链接或正文>

要求：
1. 先搜索是否已有相关笔记。
2. 新建一篇 Inbox 笔记，包含来源、摘要、关键观点、相关链接和待确认。
3. 给出应链接到哪些 MOC 的建议。
4. 完成后用 obsidian-cli 或文件读取方式验证内容。
```

## 3. 更新主题 MOC

```text
请搜索 vault 中所有和 Agent、Claude Code、MCP、Skill、Obsidian 相关的笔记，更新 MOCs/Agent 学习 MOC.md。
要求：
1. 只链接真实存在的笔记。
2. 按主题分组。
3. 标出还缺哪些关键笔记。
4. 不要移动文件，先只更新 MOC。
```

## 复盘

每次工作结束，让 Agent 输出：

```text
请总结本次知识库修改：
1. 新增或修改了哪些文件；
2. 哪些内容还在 Inbox；
3. 哪些 MOC 被更新；
4. 下一步应该整理什么。
```

下一章：[实战二：自动知识摄取](../practice-ingestion/index.md)。
