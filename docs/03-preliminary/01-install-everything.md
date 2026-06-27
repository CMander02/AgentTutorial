---
icon: material/package-variant-closed
---

# 配置环境并安装 Agent

## 1. 包管理工具

首先需要为电脑配置常见的编程语言的环境和包管理工具。

Agent 通过书写并执行具体的计算机程序进行流程化、确定性的工作，计算机程序需要对应的编程语言的工作环境才能正常编译成可执行的文件。

这里我们安装 Python 和 TypeScript 两种语言的包管理器。Python 是深度学习和人工智能的母语，以其开发便捷、支持的包足够多而深受广大程序员的喜爱；TypeScript 是一种强类型语言，可以使用配套的语法检查器便捷地检查程序的大部分格式和书写问题，同时也是现代前端界面的母语，以及相当一部分 Agent CLI 的使用语言。

### 1.1. Python 包管理器：uv

`uv` 是目前 Python 最热门的包管理器，以其环境管理便捷、下载迅速而逐渐成为当下 Python 环境管理的标配。

若你使用 Linux / MacOS ，使用下面的指令安装：

```bash
curl -LsSf https://astral.sh/uv/install.sh | sh
```

或：

```bash
wget -qO- https://astral.sh/uv/install.sh | sh
```

若你使用 Windows ，则使用下面的指令进行安装：

```powershell
powershell -ExecutionPolicy ByPass -c "irm https://astral.sh/uv/install.ps1 | iex"
```

安装过程一路回车即可。安装完成后输入 `uv help` ，正常弹出 Help 信息就算是安装完成了。

包管理器的包下载来源默认是国外服务器，为了加速下载，需要切换到国内服务器，一般常见换成清华源或中科大源。这里以中科大源为例。

若你使用 Linux / MacOS，修改 `~/.config/uv/uv.toml` 这个文件；若你使用 Windows，修改这个文件 `%AppData%\uv\uv.toml` 。修改内容并保存：

```bash
[[index]]
url = "https://mirrors.ustc.edu.cn/pypi/simple"
default = true
```

> [!NOTE] Windows 如何获取 %AppData% 路径
> 可以直接在 Powershell 输入
> `notepad "$env:APPDATA\uv\uv.toml"`
> 即可在记事本打开并编辑。

uv 的使用教程可以参考[菜鸟教程-uv](https://www.runoob.com/python3/uv-tutorial.html)。本文此处不赘述。

### 1.2. TypeScript / Node.js 包管理器：npm

TypeScript 本身不是一个独立的运行环境。实际使用时，需要先安装 Node.js；Node.js 负责运行 JavaScript / TypeScript 工具，npm 负责下载和管理相关软件包。

若使用 Windows，推荐直接从 [Node.js 官网](https://nodejs.org/zh-cn/download) 下载`.msi` 格式的安装包，一路默认安装即可。

若使用 Linux / macOS，可以从 [Node.js 官网](https://nodejs.org/zh-cn/download) 下载安装包，也可以使用自己系统常用的包管理器安装。安装时选择 LTS 版本即可。

安装完成后，重新打开终端，输入：

```powershell
node --version
npm --version
npx --version
```

若三条命令都正常输出版本号，就说明 Node.js 和 npm 已经安装完成。

同样，为了加速下载，把 npm 的默认下载源切换到国内镜像。这里推荐使用淘宝源，也就是现在的 npmmirror 源：

```powershell
npm config set registry https://registry.npmmirror.com/
npm config get registry
```

第二条命令正常输出 `https://registry.npmmirror.com/` 即表示配置成功。

> [!NOTE] 如何恢复官方 npm 源
> 如果后续需要发布 npm 包，或遇到国内源同步问题，可以切回官方源：
>
> ```powershell
> npm config set registry https://registry.npmjs.org/
> ```

同样的， npm 的详细使用教程可以参考[菜鸟教程-npm](https://www.runoob.com/nodejs/nodejs-npm.html)。

## 1.3. 安装 Git

Git 是版本管理工具，可以方便地管理文件夹下面的文件变更情况，避免 Agent 删库之后无从恢复文件。

Git 可以直接从 [Git 官网](https://git-scm.com/install/)安装。

Git 的使用相对前面二者会稍微复杂一点，建议至少了解 [菜鸟教程 - Git 教程 - Git 基本操作](https://www.runoob.com/git/git-basic-operations.html) ，了解工作目录、暂存区、本地仓库是三个不同的文件空间，以及最基础的连招

```bash
git init
git add <filename>
git commit -m "first commit"
```

## 2. 安装 Agent

选取你喜欢的/已订阅 Agent 进行安装即可：

- [Claude Code](https://code.claude.com/docs/en/quickstart)
- [Codex](https://developers.openai.com/codex/quickstart?setup=cli)
- [OpenCode](https://opencode.ai/)

注意：

1. 这三个都有 GUI，但是我推荐先从 TUI / CLI 开始学习如何使用。
2. 如果你安装的是 Claude Code，强烈推荐再安装下面的插件：
    1. [cc-swtich](https://github.com/farion1231/cc-switch)：快速配置、切换第三方 API。同时支持 Codex，OpenCode
    2. [ccusage](https://github.com/ccusage/ccusage)：快速查看近期模型用量
