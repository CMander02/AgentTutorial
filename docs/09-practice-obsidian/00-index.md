---
icon: material/notebook-edit-outline
---

# Obsidian 实战

!!! abstract "导言"

    本章把前面的 Agent 工作流放到一个具体场景里：维护本地 Obsidian vault。这里先建立清楚的目录、规则、验证方式和可回滚流程，不追求复杂插件。

## 目标 {#goal}

完成本章后，你应该能设计一个 Agent 友好的 vault：

- 新内容先进入 Inbox。
- 长期笔记放入 Notes。
- 主题索引放入 MOCs。
- Agent 修改前先搜索相似内容。
- 每次修改后输出改动摘要。

## 建议目录 {#vault-structure}

可以从这个结构开始：

```text
Vault/
├── Inbox/
├── Notes/
├── MOCs/
├── Daily/
├── Sources/
└── Templates/
```

目录不用多，但职责要清楚。

| 目录         | 用途                 |
| ------------ | -------------------- |
| `Inbox/`     | 临时内容和待整理材料 |
| `Notes/`     | 整理后的长期笔记     |
| `MOCs/`      | 主题索引和知识地图   |
| `Daily/`     | 每日记录和临时任务   |
| `Sources/`   | 原文、摘录和来源记录 |
| `Templates/` | 固定笔记模板         |

## 写给 Agent 的规则 {#agent-rules}

在 vault 根目录放一份项目说明，例如 `AGENTS.md` 或 `CLAUDE.md`：

```markdown
# Vault Rules

- 新内容先放入 Inbox/。
- 长期笔记放入 Notes/。
- 主题索引放入 MOCs/。
- 修改前先搜索相似笔记。
- 不确定分类时留在 Inbox/ 并标记待确认。
- 每次修改后列出新增、修改和未处理事项。
```

规则越清楚，Agent 越容易稳定维护知识库。

## 第一次整理任务 {#first-task}

先给一个小任务：

```text
请阅读 vault 目录结构和 AGENTS.md，说明当前知识库规则。先不要修改文件。
```

确认它理解规则后，再给整理任务：

```text
请把 Inbox/ 里最近一篇笔记整理成 Notes/ 中的长期笔记。要求保留来源链接，列出关键观点，并在 MOCs/Agent 学习.md 中添加链接。完成后说明新增和修改的文件。
```

## 验证 {#check}

整理完成后检查：

- 新笔记是否放在正确目录。
- 来源链接是否保留。
- MOC 是否加入反向入口。
- 不确定内容是否标记待确认。
- Git diff 或备份是否能显示改动。

如果 vault 是 Git 仓库，可以运行：

```powershell
git status --short
git diff
```

## 常见误区 {#pitfalls}

??? warning "一开始就自动归档所有内容"

    先让 Agent 处理少量样本。分类规则稳定后，再扩大范围。

??? warning "让 Agent 覆盖原文"

    原文、摘录和总结应分层保存。原始材料要能追溯。

??? warning "没有待确认区"

    不确定信息需要有去处。没有待确认区时，Agent 容易把猜测写进长期笔记。

## 下一步 {#next}

到这里，你已经完成从概念、选型、Coding CLI 到 Skill 和 Obsidian 的入门闭环。遇到具体问题时，可以回到 [FAQ](../99-faq.md)。
