---
icon: material/lightbulb-on-outline
---

# 写作启发

!!! abstract "导言"

    本章说明这份教程为什么要先讲写作规范。Agent 教程如果只堆命令，读者很容易照抄一遍后失去方向；如果每章都有目标、背景、步骤、验证和下一步，读者就能知道自己正在学什么，也能判断 Agent 的输出是否可靠。

    本教程参考并感谢 [LUG@USTC Linux 101](https://101.lug.ustc.edu.cn/) 及其 [Linux101-docs](https://github.com/ustclug/Linux101-docs) 仓库。Linux 101 以 [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/) 授权发布。

## 借鉴来源 {#source}

Linux 101 是一份面向新手的 Linux 课程讲义。它的写作规范强调章节导言、本地预览、提示框、标题 ID 和引用方式。这些规则很适合迁移到 Agent 教程，因为 Agent 学习也需要连续阅读和动手验证。

本项目把 Linux 101 的原始写作规范保存到项目局部 Skill：

```text
.codex/skills/linux101-writing/references/writing.md
```

## 本项目采用的规则 {#rules}

本教程采用以下写作规则：

- 每章开头都写导言，先交代本章为什么存在。
- 正文从 H2 开始组织，每个 H2 都有稳定标题 ID。
- 每个页面尽量包含目标、背景、步骤、验证、常见误区和下一步。
- 导言使用默认展开的三叹号 `abstract "导言"` 写法。
- 其他提示框全部使用折叠块，避免正文被彩色块切碎。
- Prompt、命令、代码、配置和模板放在普通代码块，方便读者复制。
- 每次修改后运行 Prettier 和 MkDocs strict 构建。

## Prettier 规范 {#prettier}

Linux 101 仓库根目录的 `.prettierrc.json` 只有两条核心配置：

```json
{
    "embeddedLanguageFormatting": "off",
    "tabWidth": 4
}
```

本项目沿用这两条配置，并提供同样的脚本入口：

```powershell
npm install
npm run check
npm run fix
```

## 提示框规则 {#admonitions}

导言保留展开状态。写法是三叹号加 `abstract "导言"`，标题行下方空一行，再缩进正文。

其他说明块使用折叠状态：

```markdown
??? info "重点"

    这里写补充说明。
```

如果内容需要读者复制，应放在普通代码块中：

```text
请先阅读 README、mkdocs.yml 和 docs/ 目录，只总结项目结构，先不要修改文件。
```

## 标题 ID 规则 {#heading-ids}

H1 不添加 ID。H2 和更低层级的标题需要添加稳定 ID：

```markdown
## 验证 {#check}
```

ID 使用小写字母、数字和短横线。纯中文标题依赖自动生成 ID 时，链接会变得不稳定。

??? warning "标题 ID 常见错误"

    `{#` 前面需要保留一个空格。若写成 `## 验证{#check}`，主题可能无法生成预期锚点。

## 本地预览 {#preview}

写作时需要随时预览当前主题下的效果：

```powershell
uv run mkdocs serve
```

正式提交前运行：

```powershell
npm run check
uv run mkdocs build --strict
```

## 下一步 {#next}

下一章：[从零理解 Agent](../01-agent/00-index.md)。
