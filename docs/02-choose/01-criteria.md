---
icon: material/tune
---

# 选型维度

2026 年，Agent 项目和产品浩如烟海，萌新入坑时，非常容易被大量的名词和夸张的演示吓晕过去。本节给出我的推荐办法。

## 1. 写在最前面

若深入使用 Agent 项目，最好走稳定的官方渠道进行付费。

原因如下：

1.  免费的 Agent 产品，其提供的模型服务，要么限量，要么限速，要么模型能力低下，无法顺畅执行任务；
2.  所谓的“国外大模型中转站”，提供的模型服务，大部分时候不稳定，少部分时候会偷偷换用便宜模型，极个别情况下，还有注入恶意 Prompt 并控制你电脑的风险；
3.  已经有论文研究表明，在使用 Agent 完成任务的时候，强模型相比弱模型，不但花费的时间更少，还因为犯错次数更少，能省下更多的钱。

当然，如果你打算先熟悉 Agent 的使用，下面也有稳定的免费途径与低价途径，可供你初步使用和学习。

## 2. 免费 Coding Agent

当前只推荐 [OpenCode](https://opencode.ai/)。

OpenCode 是一个开源 Agent 框架。开发者社区火热，可以自行配置很多额外的插件。

OpenCode 的开发者和大量的开源模型服务商关系良好，因此总有多款开源模型可以免费试用。

免费 Agent 只推荐 OpenCode。个人不推荐其他任何免费 Agent，理由详见第 6 部分。

## 3. 付费 Coding Agent

### 3.1. 国产（开源）模型与服务

1.  [DeepSeek API](https://platform.deepseek.com/usage)。国模之光。截止2026年6月1日，除了没有视觉模型外，DeepSeek 有着极高的[缓存命中率](https://api-docs.deepseek.com/zh-cn/guides/kv_cache)，且[Pro 模型打25折](https://api-docs.deepseek.com/zh-cn/quick_start/pricing#%E6%A8%A1%E5%9E%8B%E7%BB%86%E8%8A%82)，这使得它成为2026年上半年的性价比一号。伟大，无需多言。

2.  [小米 Mimo API](https://platform.xiaomimimo.com/docs/zh-CN/welcome) 与 [Mimo Token Plan](https://platform.xiaomimimo.com/token-plan)。2026年上半年性价比二号。性能尚可，自带多模态，价格比起接下来两家稍低，服务稳定。

3.  [Kimi 会员](https://www.kimi.com/membership/pricing) 与 [GLM Coding Plan](https://bigmodel.cn/glm-coding)。模型能力均比 DeepSeek-v4-pro 稍强，同时自带多模态；但是价格比较贵，低价套餐 token 量不太够，高峰时段服务不稳定容易卡死。

4.  [Minimax Token Plan](https://platform.minimaxi.com/subscribe/token-plan)。2026上半年性价比三号。自带多模态。模型性能显著不如前面的各个模型，但是价格便宜量大管饱，适合驱动 Agent 执行简单任务。

5.  [OpenCode Go](https://opencode.ai/zh/go)。OpenCode 的初级付费套餐，可以以 $5/月的低价使用上述的各种国内开源模型。支持国内支付渠道如支付宝。

### 3.2. 美国模型

美国 OpenAI, Anthropic, Google 三家提供的订阅服务。

当前推荐顺序为 ChatGPT Plus > Claude Code Pro. 不推荐 Google Gemini。

如果用量超过套餐量，可以考虑升级各自的 $100 套餐。

#### 3.2.1. 关于付费套餐

| 厂商 \ 档位                                                    | 免费 | 尝鲜档                   | 基础档                   | 进阶1档 （5倍基础）  | 进阶2档（20倍基础）    |
| -------------------------------------------------------------- | ---- | ------------------------ | ------------------------ | -------------------- | ---------------------- |
| [OpenAI ChatGPT](https://chatgpt.com/pricing/)                 | Free | Go （8\$/月）            | Plus （20\$/月）         | Pro 5x（100\$/月）   | Pro 20x（200\$/月）    |
| [Anthropic Claude](https://claude.com/pricing)                 | Free | 无此档位                 | Plus （17\$/月）         | Max 5x（100\$/月）   | Max 20x（200\$/月）    |
| [Google Gemini](https://gemini.google/us/subscriptions/?hl=en) | Free | Google AI Plus（8\$/月） | Google AI Pro（20\$/月） | Ultra 5x（100\$/月） | Ultra 20x （200\$/月） |

美国三家 AI 厂商的订阅套餐如上所示。

基础档位是这三家能够满足一般 Agent 任务用量的最低档位。进阶档位的倍率均是相对于基础档位而言的。

所有进阶档位，都满足“买得越多，省得越多”的特性。以 ChatGPT 为例， Pro 5x （即$100档位）档位实际能产生的 GPT 5.5 xhigh Token 量，按照订阅价格计算，已经能和 DeepSeek-V4-Pro 持平。而 GPT 5.5 xhigh 的模型智能水平、Agent 能力都超过 DeepSeek 模型不少。

## 4. 其他 Agent 产品

### 4.1. 桌面端 Agent

1.  Cherry Studio。国人团队开发的桌面端 Agent，安装便捷，配置容易，界面直观好用，更新及时。
2.  OpenAI Codex Desktop。OpenAI Codex 团队自主开发。审美和交互设计很不错，使用体验也非常好。

## 4.2. 类 OpenClaw Agent

当前只推荐 Hermes。Hermes 安装和配置都比较容易，基本能做到开箱即用，而且自带的 Agent 进化机制效果不错。

## 5. 第三方聚合 API 服务

很多云厂商会提供聚合平台 API 服务，在单一平台注册并充值，就可以用较好的价格使用各种不同的开源模型，以及各个云厂商自有的其他模型服务。但考虑到国内主要的三个云厂家，对应的自己的顶级模型都不是非常强（字节火山云-豆包 Seed 系列，阿里云-千问 Qwen Max，腾讯云-混元 HY 系列），因此此处只推荐三个第三方 API 服务提供商：

1.  硅基流动。国内老牌聚合 API 服务提供商。一些小模型可以直接免费使用，白嫖党和需要简单的大模型智能接入的场合必选；
2.  AIHubMix。老牌国际模型聚合 API 服务提供商，支持支付宝付款。
3.  OpenRouter。全球最大、最知名的模型聚合 API 服务提供商。几乎所有的模型在公开发表之前，都会在上面遮住模型名发布预览版本，收集一手反馈，此时该模型使用是免费的。平台亦对一些热门模型提供免费低速访问接口，适合尝鲜和对比试用。

仅推荐需要大量不同的国产模型、且需要发票报销的情况下，使用国内云厂家的第三方服务。

## 6. 不推荐的 Agent 服务和行为

1.  薅各个模型平台的注册赠金。注册不同平台耗费时间长，获得赠金额度一般，消磨精力，反而难以体会 Agent 执行任务的乐趣；
2.  Gemini 订阅服务。近一年来的 Gemini 系列模型，其能力无论相较同期 OpenAI GPT 系列还是 Anthropic Opus/Fable 系列，都弱了很多；同时， Google 自己的 Agent 框架，不管是 Antigravity ，~~Gemini CLI （2026年6月已停止服务）~~ 还是 Antigravity CLI ，使用体验和性能都相对较差；
3.  除学生免费等级外，任何等级的 GitHub Copilot。微软自己没有 Agent 设计经验，作为二道贩子，接入其他厂家的 LLM 售卖，偏偏 Copilot 作为通用 Agent 框架，的工程设计又偏弱且扩展性不足，无法针对不同的模型进行优化和适配。
4.  国内外其他各种 Coding Agent 产品。原因和 GitHub Copilot 一样，二道贩子 + Agent 框架工程设计水平不足；
5.  OpenClaw。框架太重，安装繁琐，大部分时候部署云端 Agent 只需要它作为一个桥接器和一个具有基础智能水平即可，不需要 OpenClaw 这种笨重且更新不稳定的大型产品。
6.  中转站。中转站一定绕不开以下几个问题：以次充好无法感知，模型服务不稳定，店家随时跑路。除了价格全面劣于官方订阅。建议直接向你使用的模型的厂商进行一手订购。

## 7. 太长不看

| 月租/元 | 方案                                                        | 优点                                     | 缺点                                                               |
| ------- | ----------------------------------------------------------- | ---------------------------------------- | ------------------------------------------------------------------ |
| 0       | OpenCode 免费模型                                           | 具备全部常见功能和一部分免费开源模型     | 模型智能不够完成复杂任务<br />模型额度不够高强度使用               |
| 0~60    | 咸鱼低价 GPT Plus / 咸鱼低价 Claude Plus 账号 / OpenCode Go | 几乎没有缺点                             | 前两者的账号不能长时间存活，账号的对话信息随账号丢失，店家随时跑路 |
| 60~140  | Kimi / GLM 入门会员二选一                                   | 经济实惠，使用方便，购买简单             | 高峰时段输出速度降低且不稳定                                       |
| 140~700 | GPT Plus / Claude Pro 二选一                                | 几乎没有缺点，而且账号是自己的，非常安全 | 注册麻烦，额度稍低，大量复杂工作容易烧干周额度                     |
| >700    | GPT Pro $100 / Claude Max $100 二选一                       | 几乎没有缺点，而且账号是自己的，非常安全 | 除了可能引诱用量极大的用户购买 $200 套餐外，几乎没有风险           |
