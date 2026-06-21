# Agent 新手教程

这是一个面向新手的 Agent 教程站点。主线从概念、选型和本地环境开始，逐步进入 Coding CLI、Prompt、计划、长任务、Skill、MCP 和 Obsidian 实战。

教程写作参考并感谢 [LUG@USTC Linux 101](https://101.lug.ustc.edu.cn/) 及其 [Linux101-docs](https://github.com/ustclug/Linux101-docs) 仓库。Linux 101 以 CC BY-SA 4.0 授权发布，本项目沿用其中适合新手教程的写作规则。

## 本地预览

```powershell
uv run mkdocs serve
```

## 构建检查

```powershell
uv run mkdocs build --strict
```

## Markdown 格式检查

本项目按 Linux 101 仓库的 Prettier 配置建立 Markdown 格式规范。

```powershell
npm install
npm run check
npm run fix
```

## 目录

- `docs/01-agent/`：第 1 章，Agent 基础概念。
- `docs/02-choose/`：第 2 章，选型判断和购买前验证。
- `docs/03-pre-agent/` 到 `docs/08-create-skill/`：第 3 到第 8 章，Coding CLI 工作流。
- `docs/09-practice-obsidian/`：第 9 章，Obsidian 实战入口。
- `docs/01-agent/images/`：第 1 章图片资源。
