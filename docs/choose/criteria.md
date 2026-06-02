---
icon: material/tune
---

# 选型维度

2026 年，Agent 项目和产品浩如烟海，萌新入坑非常容易被大量的名词和夸张的演示吓晕过去。本节给出我的推荐办法。



## 1. 写在最前面

若深入使用 Agent 项目，最好走稳定的官方渠道进行付费。原因如下：

1.   免费的 Agent 产品，其提供的模型服务，要么限量，要么限速，要么模型能力低下，无法顺畅执行任务；
2.   所谓的“国外大模型中转站”，提供的模型服务，大部分时候不稳定，少部分时候会偷偷换用便宜模型，极个别情况下，还有注入恶意 Prompt 并控制你电脑的风险；
3.   已经有论文研究表明，在使用 Agent 完成任务的时候，强模型相比弱模型，不但花费的时间更少，还因为犯错次数更少，能省下更多的钱。

当然如果你打算先熟悉 Agent 的使用，下面也有稳定的免费途径可以使用和初步学习。



## 2. 免费 Coding Agent

当前只推荐 [OpenCode](https://opencode.ai/)。 OpenCode 是一个开源  Agent 框架。开发者和大量的开源模型服务商关系良好，因此总有一些开源免费模型可以进行试用。 

免费 Agent 只推荐这个。个人不推荐其他任何免费 Agent，理由详见第 6 部分。



## 3. 付费 Coding Agent

### 3.1. 国内模型

1.   [DeepSeek API](https://platform.deepseek.com/usage)。国模之光。截止2026年6月1日，除了没有视觉模型外，极高的[缓存命中率](https://api-docs.deepseek.com/zh-cn/guides/kv_cache)，[Pro 模型打25折](https://api-docs.deepseek.com/zh-cn/quick_start/pricing#%E6%A8%A1%E5%9E%8B%E7%BB%86%E8%8A%82)，使得它成为2026年上半年的性价比一号。伟大，无需多言。

2.   [小米 Mimo API](https://platform.xiaomimimo.com/docs/zh-CN/welcome) 与 [Mimo Token Plan](https://platform.xiaomimimo.com/token-plan)。2026年上半年性价比二号。性能尚可，自带多模态，价格比起接下来二位稍低，服务稳定。

3.   [Kimi 会员](https://www.kimi.com/membership/pricing) 与 [GLM Coding Plan](https://bigmodel.cn/glm-coding)。模型能力比 DeepSeek-v4-pro 稍强，自带多模态，但是价格比较贵，低价套餐 token 量不太够，高峰时段服务不稳定容易卡死。

4.   [Minimax Token Plan](https://platform.minimaxi.com/subscribe/token-plan)。2026上半年性价比三号。自带多模态。模型性能显著不如前面的各个模型，但是价格便宜量大管饱，适合驱动 Agent 执行简单任务。

5.   [OpenCode Go](https://opencode.ai/zh/go)。OpenCode 的初级付费套餐，可以以 $5/月的好价使用上述的各种国内开源模型。支持国内支付渠道如支付宝。

     

### 3.2. 国外（美国）模型

北美御三家的订阅服务，当前推荐顺序为 OpenAI Plus > Claude Code Pro. 如果需求超过用量，则可以考虑升级各自的 $100 套餐。



## 4. 其他 Agent 产品

### 4.1. 桌面端 Agent

1.   Cherry Studio。国人团队开发的桌面端 Agent，安装便捷，配置容易，界面直观好用，更新及时。
2.   OpenAI Codex Desktop。OpenAI 团队的审美和交互设计很不错，使用体验也非常好。



## 4.2. 类 OpenClaw Agent

当前只推荐 Hermes. Hermes 安装和配置都比较容易，同时基本能做到开箱即用，而且自带的 Agent 进化机制效果不错。



## 5. 第三方聚合 API 服务

很多云厂家会给出第三方平台，在单一平台注册并充值，就可以以较好的价格使用各种不同的开源模型，以及他们自有的模型服务。但考虑到国内主要的三个云厂家，对应的自己的顶级模型都不是非常强（字节火山云-豆包Seed系列，阿里云-千问 Qwen Max，腾讯云-混元 HY系列），因此此处只推荐三个第三方 API 服务提供商：

1.   硅基流动。国内老牌聚合 API 服务提供商。一些小模型可以直接免费使用，白嫖党和需要简单的大模型智能接入的场合必选；
2.   AIHubMix。老牌国际模型聚合 API 服务提供商，支持支付宝付款。
3.   OpenRouter。全球最大、最知名的模型聚合 API 服务提供商。几乎所有的模型在公开发表之前，都会在上面遮住模型名发布预览版本，收集一手反馈，此时该模型使用是免费的。平台亦对一些热门模型提供免费低速访问接口，适合尝鲜和对比试用。



## 6. 不推荐的 Agent 服务和行为

1.   到处薅各个模型平台的注册赠金。注册不同平台耗费时间过长，而获得的赠金额度一般，消磨精力，反而无法体会 Agent 执行任务的乐趣。
2.   Gemini 订阅服务。Gemini 系列模型近年来能力相较 OpenAI  GPT 系列和 Anthropic Opus 系列模型弱了很多，同时 Google 自己的 Agent 框架，无论是  Antigravity 还是 Gemini CLI 还是 Antigravity CLI 都一言难尽；
3.   GitHub Copilot。微软自己没有 Agent 设计经验，作为二道贩子，接入他人的 LLM 额度来卖，偏偏 Copilot 作为 Agent 的工程设计又偏弱且扩展性不足；
4.   其他各种 Coding Agent 产品。原因和 GitHub Copilot 一样，二道贩子 + Agent框架工程设计水平不足；
5.   OpenClaw。框架太重，安装繁琐，大部分时候部署云端 Agent 只需要它作为一个桥接器和一个具有基础智能水平即可，不需要 OpenClaw 这种笨重且更新不稳定的大型产品。



## 7. 太长不看，无脑买法

| 月付价格/元 | 方案                                  | 优点                                     | 风险                                                       |
| ----------- | ------------------------------------- | ---------------------------------------- | ---------------------------------------------------------- |
| 0           | OpenCode 免费模型                     | 具备全部常见功能和一部分免费开源模型     | 模型智能不够完成复杂任务，模型额度不够高强度使用           |
| 0~60        | 咸鱼低价 GPT / Claude Pro 账号        | 除了账号不是自己的，几乎没有缺点         | 账号不能长时间存活，账号的对话信息随账号丢失，店家随时跑路 |
| 60~140      | Kimi / GLM 入门会员二选一             | 经济实惠，使用方便，购买简单             | 高峰时段输出速度降低，甚至可能不可用                       |
| 140~700     | GPT Plus $20 / Claude Pro $20 二选一  | 几乎没有缺点，而且账号是自己的，非常安全 | 注册麻烦，额度稍低，大量复杂工作容易烧干周额度             |
| >700        | GPT Pro $100 / Claude Max $100 二选一 | 几乎没有缺点，而且账号是自己的，非常安全 | 除了可能引诱用量极大的用户购买 $200 套餐外，几乎没有风险   |

下一节：[如何订阅美国 AI](how-to-buy-us-services.md)
