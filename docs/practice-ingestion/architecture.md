---
icon: material/graph-outline
---

# Hermes + 知识库整体架构

自动知识摄取的关键是把“输入、处理、入库、回顾”分开。

## 架构

```text
互联网内容 / 手动内容 / Bot 消息
  -> Hermes
  -> 知识摄入 Skill
  -> 去重、总结、分类
  -> Obsidian Inbox / Sources / MOCs
  -> 定期回顾和整理
```

## 不要一开始全自动

推荐阶段：

1. 手动把链接交给 Claude Code。
2. Hermes 接收链接，但只放入 Inbox。
3. Hermes 自动总结，但需要人工确认归档。
4. 规则稳定后，再自动分类和更新 MOC。

下一步：[互联网内容摄取](web-ingestion.md)。
