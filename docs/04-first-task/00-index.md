---
icon: material/play-circle-outline
---

# 第一次任务

!!! abstract "导言"

    第一次使用 Coding CLI 时，不要急着交给它复杂任务。最稳的练习方式，是先让它只读观察项目，再让它做一个小改动，最后一起验证结果。

## 目标 {#goal}

本章完成一个最小闭环：

1. 让 Agent 读取项目结构。
2. 让 Agent 只修改一个小文件。
3. 运行检查命令。
4. 查看 Git diff。

## 只读观察 {#read-only}

第一条请求应限制为只读：

```text
请阅读 README、mkdocs.yml 和 docs/ 目录，说明这个项目是做什么的。先不要修改任何文件。
```

好的回答应该包含项目类型、目录结构、构建命令和它暂时不确定的地方。

??? info "重点"

    只读观察能帮助你判断 Agent 是否进入了正确目录，也能避免它在不了解项目时直接动手。

## 小改动任务 {#small-change}

选择一个容易验证的小任务。例如补充 README 的一句说明：

```text
请在 README 的本地预览部分补充一句：修改 Markdown 后需要重新刷新浏览器。只改 README，完成后说明改了哪一行。
```

小任务的关键是范围清晰、文件明确、结果能看见。

## 运行验证 {#verify}

如果项目有构建命令，就让 Agent 运行。自己也可以手动执行：

```powershell
uv run mkdocs build --strict
```

然后查看改动：

```powershell
git diff -- README.md
git status --short
```

如果命令失败，先读错误信息，再决定是否继续让 Agent 修复。

## 复盘输出 {#review}

任务结束时，让 Agent 用固定格式复盘：

```text
请总结这次任务：
1. 修改了哪些文件。
2. 运行了哪些验证命令。
3. 还有哪些风险或未处理事项。
```

这个格式能帮你快速判断任务是否真的结束。

## 常见误区 {#pitfalls}

??? warning "第一次就让它批量重构"

    新手很难同时判断几十处改动。先用一处小改动建立信任，再扩大任务范围。

??? warning "忽略失败命令"

    构建失败、测试失败和格式检查失败都需要处理。不要只看最终回答是否流畅。

## 下一步 {#next}

下一章：[Prompt 与计划](../05-prompt-plan/00-index.md)。
