---
icon: material/download-box-outline
---

# 安装常用 MCP 和 Skill

本页只讲安装思路。具体命令请以对应工具的官方文档为准。

## 安装前先问三件事

1. 这个扩展解决什么任务？
2. 它需要哪些权限？
3. 它失败时如何排错？

## 常见 MCP 类型

| 类型     | 用途                          |
| -------- | ----------------------------- |
| 文件系统 | 读写指定目录                  |
| 浏览器   | 打开网页、截图、点击          |
| 知识库   | 读写 Obsidian、Notion、Zotero |
| 协作工具 | 飞书、Slack、GitHub           |
| 数据工具 | 数据库、表格、BI              |

## Windows 注意事项

很多 Node MCP server 在 Windows 下需要通过 `cmd /c` 启动。配置前先看 server 文档。

检查 MCP 状态常用：

```powershell
claude mcp list
```

## Skill 安装思路

Skill 通常包含：

```text
skill-name/
├── SKILL.md
├── scripts/
└── templates/
```

安装后不要急着用于真实任务，先用一个小样本测试它是否按预期触发。

下一章：[类龙虾应用与 Hermes](../hermes/index.md)。
