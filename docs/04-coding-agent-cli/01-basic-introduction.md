---
icon: material/keyboard-outline
---

# 常用指令的简单介绍

本节我们列举各种常用的指令。

## 1. Hello World!

首先启动 Agent CLI.
如果使用较强的模型，我非常推荐所有读者，在启动的时候，就直接给 Agent 完全权限。
选取你想要启动的 Agent 并启动。

Claude Code:

```bash
claude --dagerously-skip-permissions
```

Codex 有两种等效的办法：

```bash
codex --dangerously-bypass-approvals-and-sandbox
codex --yolo
```

OpenCode 需要修改文件，输入

```bash
opencode
```

进入交互式命令行，然后粘贴下面这句给他：

```text
在 ~/.config/opencode/opencode.json 中，将 permission 设为 "allow" ，以配置全局 bypass 权限
```

然后你就进入到一个黑漆漆的交互式命令行了。给他敲一个 Hello World，Agent 就会回应你。

恭喜你，你已经初步掌握了如何使用 Agent了！
接下来的大部分教程，结构都会是：

- 我们问 Agent ”你会做什么？” ” 这个怎么做？“ ”这样行不行？”
- Agent 给我们一个简明的教程和解释
- 我们学会了更简单和实用的办法，就不用重复问了

让我们开始吧！

## 2. 如何让 Agent 听话： AGENTS.md / CLAUDE.md

先不提 Agent。相信读者大多数很反感 [AI 味很重的句子](https://www.bilibili.com/video/BV11xFDzqEkn/) ，比如 “不是……而是”，比如大而无当的比喻，等等。虽然可以从这个视频里面提炼出下面的

## 3. 基础指令

指令一般以 `/` 开头，直接输入并回车即可触发。

| 指令     | 指令功能                                          |
| -------- | ------------------------------------------------- |
| /model   | 列举并选择接下来使用的模型（和推理强度）          |
| /compact | 压缩过长的对话内容                                |
| /plan    | 切换到计划模式                                    |
| /goal    | 切换到目标模式                                    |
| /btw     | 在 Agent 工作期间，不打断工作状态，临时问一个问题 |
| /clear   | 清除当前的所有对话历史                            |
| /usage   | 查看当前的累计用量                                |
| /agent   | 查看当前对话中能够使用的 Agent                    |

其中重点讲一下 `/plan`，`/goal` 和 `/btw` 的使用方法。
一般的顺序是：

1. 开启计划模式确定工作计划

```bash
/plan [你的计划内容，可简可繁]
```

Agent随即进入计划模式，进行调研，与你交流，直到得出可行的执行计划；2. 开启目标模式让 Agent 向目标努力

```bash
/goal [计划方案，任务目标，验证任务完成的办法]
```

3. 在工作中，如果出现问题需要让 Agent 暂停并更改错误，需要
