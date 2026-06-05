---
icon: material/source-branch
---

# Agent 交互形态演化

现代 LLM Agent 的形态，起源于[姚顺雨](https://ysymyth.github.io/) 的 [ReAct](https://arxiv.org/pdf/2210.03629) 一文，文章继承了上面的 Agent 的工作流程并将其扩展到了 LLM Agent 中。

## ReAct

ReAct 是 reasoning + acting （推理+执行）的缩写。它的核心思想是让模型先观察、再推理，最后调用工具，再观察工具执行的结果，根据结果继续推理。这种形式可以完成简单的单步任务。

我们可以很自然地为 ReAct Agent 添加一个固定次数的循环，或者要求 Agent 直到（自己觉得）完成了某个具体的要求才能结束循环。这样就能执行多步任务。

这个时期的 Agent 执行的步数可能只有固定的几步，而且没有从环境中获得反馈的能力。

## Coding Agent 与  Coding CLI

计算机命令行，是一个能够将输入和输出都统一为文本流的绝佳环境。从 GitHub Copilot 和  Cursor 开始，Agent 开始大规模在命令行中进行工作。

这个时期的 Agent 可以一口气参考大量文档，并连续执行十几步的工作，每一步工作都能直接从代码环境中获得最真实有效的反馈。

Coding CLI 相较于 Coding Agent，舍弃了图形界面，直接进入本地项目目录，获取信息的效率进一步提升，还能直接查看、修改项目文件夹和其中的文件。

## Self-improve Agent

Self-improve agent （自进化 Agent ）会根据运行结果和环境的反馈，调整自己的策略、规则或工具使用方式，并将调整的规则固化下来，形成未来可以复用的的文档、代码、规范等。

这个时期 Agent 能够执行几十步甚至上百步的任务。更好的衡量办法是稳定运行的时间，这个时期 Agent 开始以小时为单位自主稳定运行，自主纠错并沉淀经验教训。 Agent 开始进入“越用越好用”、“越用越懂你”的阶段。

## 类 OpenClaw Agent

严格来说 OpenClaw 不是一个良好的 Agent 类型，它只不过是首次将 Agent 接入了聊天软件，使得没有用过 Agent 的人也能比较易懂地用上 Agent. 其本质还是 Coding Agent 的一套逻辑，同时可以自行配置一些 self-improve 策略。但是鉴于 2026 开年以来的龙虾热潮，大量的 Agent 能够直接接入用户的聊天框了，此处将其记录进来。

下一步：[当前两类热门形态](current-mainstream.md)。
