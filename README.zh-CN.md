<div align="center">

# awesome-oss-sponsorship（中文版）

**一份让开源项目真正收到钱的手册——赞助商、广告平台、返佣合作,以及真正能成交的主动拓展。**

精选平台 · 核实过的报价锚点 · 可直接复制的模板 · 真实案例 · 7 天冷启动计划。

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)
[![License: CC BY 4.0](https://img.shields.io/badge/License-CC_BY_4.0-blue.svg)](LICENSE)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](CONTRIBUTING.md)

</div>

> **赞助是一条销售渠道,不是 star 数的奖赏。** Star 只是热度代理——真正决定报价的是
> **月独立访客**(GitHub Traffic)、**包下载量**(npm / PyPI / Docker Hub)和**受众与赞助商的匹配度**。
> 本仓库就是专业运营这条销售渠道的手册:用哪个平台、卖哪个位、定什么价、找谁、发什么。

本仓库英文为主([README.md](README.md)),本中文版面向国内开发者,重点补充**国内视角**:
怎么卖赞助位、怎么找国内 AI API 平台/云厂商/开发者工具商、怎么用 V2EX/掘金/知乎/微信群/公众号找
sponsor、怎么报人民币价、怎么做"固定费用 + 返佣"、怎么避免显得 low、怎么写中文合作私信、
怎么拿下 1000 stars 仓库的第一个赞助。

所有价格均为**经验估算 / 仅供参考**,不是报价,不承诺收益。详见[免责声明](#免责声明)。

---

## 目录

- [这是给谁看的](#这是给谁看的)
- [国内 maintainer 的现实约束](#国内-maintainer-的现实约束)
- [5 分钟快速开始](#5-分钟快速开始)
- [平台对比](#平台对比)
- [报价参考（估算）](#报价参考估算)
- [国内赞助商去哪找](#国内赞助商去哪找)
- [国内渠道怎么发](#国内渠道怎么发)
- [人民币怎么报价 + 固定+返佣怎么设计](#人民币怎么报价--固定返佣怎么设计)
- [怎么避免显得 low 或像接广告](#怎么避免显得-low-或像接广告)
- [中文合作私信模板](#中文合作私信模板)
- [1000 stars 仓库的首个赞助成交](#1000-stars-仓库的首个赞助成交)
- [7 天冷启动计划](#7-天冷启动计划)
- [模板与工具](#模板与工具)
- [文档与数据](#文档与数据)
- [真实案例锚点](#真实案例锚点)
- [免责声明](#免责声明)

---

## 这是给谁看的

| 你是 | 从哪开始 |
|------|---------|
| **100 star 维护者**(早期 CLI/SDK) | GitHub Sponsors(0% 手续费)+ `.github/FUNDING.yml`。先抓势头,别盯着钱。→ [100-star 示例](examples/100-stars-repo.md) |
| **1000 star 维护者**(甜点区) | GitHub Sponsors + Open Collective + 一页报价卡。跑首批 50 封私信。→ [1000-star 方案](docs/1000-stars-playbook.md) · [示例](examples/1000-stars-repo.md) |
| **10000 star 维护者** | 分档赞助体系 + 独立赞助页 + 文档站 EthicalAds。→ [10000-star 示例](examples/10000-stars-repo.md) |
| **独立开发者 / 个人维护者** | GitHub Sponsors(月度)+ Buy Me a Coffee(一次性打赏)。不必用 fiscal host。 |
| **Devtool / CLI / SDK 维护者** | GitHub Sponsors + thanks.dev(依赖树自动入金)+ 返佣混合模式。 |
| **同时运营公众号 / Newsletter 的维护者** | Paved(Newsletter 广告,$/曝光最高)+ 公众号互推。 |
| **仓库本身在卖付费 SaaS / AI 产品** | Polar(Merchant-of-Record,处理全球税务)。**不是**用来拉赞助的。 |

---

## 国内 maintainer 的现实约束

先把坑说清楚,免得走弯路:

- **GitHub Sponsors 不支持中国大陆**。支持列表里有香港特别行政区、澳门特别行政区,但没有中国大陆(原文规则:必须在受支持地区居住才能收款)。国内 maintainer 收美元的可行路径:
  - **Open Collective**(走欧洲/美国 fiscal host,如 Open Collective Europe),有公开账本;
  - **Buy Me a Coffee / Ko-fi**(Stripe 收款,需有可收美元的 Stripe 账户);
  - **Polar**(如果你的项目本身卖付费产品,做 Merchant-of-Record);
  - 或**直接对公转账 / 跨境收款工具**(国内 sponsor 常用人民币对公/微信/支付宝,见下)。
- **国内 sponsor 更习惯人民币对公转账**。很多国内 AI API 平台、云厂商、开发者工具商走"签协议 + 对公月付 + 转化返佣",而不是 GitHub Sponsors 订阅。把这条当成**主渠道**,把 GitHub Sponsors/Open Collective 当成**面向海外 sponsor 的窗口**。
- **国内大多数大模型 API 平台没有公开 affiliate 程序**(智谱、零一、Kimi、百炼等均无),国内返佣通常**一对一谈**而非挂联盟链接。详见 [docs/affiliate-programs.md](docs/affiliate-programs.md) 第 9 节国内说明。

---

## 5 分钟快速开始

1. **选平台。** 个人 → [GitHub Sponsors](docs/github-sponsors.md)(0% 个人手续费,但你得在受支持地区;国内见上)。多人协作 → [Open Collective](docs/open-collective.md)(fiscal host + 公开账本)。
2. **加 `.github/FUNDING.yml`。** 给仓库挂上"Sponsor"按钮。复制 [带注释模板](templates/funding-yml-example.md)(当前 12 个 key;`otechie`/`givebutter`/`lfx_crowdfunding` **不支持**)。
3. **设档位。** GitHub Sponsors:最多 10 个一次性 + 10 个月度,最高 $12,000/月;**价格发布后不可改**(要改得下架重建)。参考真实阶梯——Vite `$5/$15/$50/$150/$500`、Astro `$10/$100/$200/$250/$1,000/$10,000`——但自己的数字标**仅供参考**。
4. **列出你的库存位。** 你卖的是**曝光**,不是 star。位类型见 [`data/sponsor-types.yml`](data/sponsor-types.yml):README 顶 banner、README 底 logo 网格(主流做法——动态 SVG,永不手改 README)、文档站广告、Release note、Newsletter。
5. **开始主动拓展。** 做一页 [报价卡](templates/rate-card.md)锚定**你自己的**流量,然后用 [中文私信模板](#中文合作私信模板)发给依赖树里的国内公司、或你的 Popular Referrers 里出现的公司。**先按估算区间低端报价**,成交 3 单后再涨。

> 5 分钟路径详见 [docs/getting-started.md](docs/getting-started.md)。

---

## 平台对比

状态于 2026-06-29 核实自官方站点。手续费均为**仅供参考**。

| 平台 | 类型 | 状态 | 手续费(参考) | 适合 |
|---|---|---|---|---|
| [GitHub Sponsors](docs/github-sponsors.md) | 赞助 | ✅ 在营 | 个人 0% / 机构 ≤6% | 个人维护者;原生 GitHub 按钮。⚠ **中国大陆不支持** |
| [Open Collective](docs/open-collective.md) | fiscal host | ✅ 在营 | $0/$60/$320 方案;或 5% | 公开账本;多人/多供应商 |
| Open Source Collective | fiscal host | ✅ 在营 | 走 OC | 美国 501(c)(6),部分可抵税 |
| [Polar](docs/polar.md) | 计费 MoR | 🔄 转型 | 5%+50¢ → 3.40%+30¢ | 付费 SaaS/AI 计税。**非赞助** |
| Buy Me a Coffee | 打赏 | ✅ 在营 | 5% + Stripe 处理费 | 一次性打赏 |
| Ko-fi | 打赏 | ⚠ 未核实 | 打赏 0%;Gold ~$12/月(需自行核实) | 直连 PayPal/Stripe 打赏 |
| Patreon | 订阅 | ✅ 在营 | 10% | 长期会员订阅 |
| thanks.dev | 打赏 | ✅ 在营 | 5% | 自动资助整棵依赖树 |
| StackAid | 打赏 | ✅ 在营 | 订阅 $15/月起 | 资助直接+间接依赖 |
| Tidelift | 订阅 | ❌ 被收购 | — | 已被 Sonar 收购(2024-12) |
| IssueHunt | 悬赏 | ⚠ 停滞 | 未披露 | issue 悬赏——用 **oss.issuehunt.io**,自核存活 |
| Algora | 招聘 | 🔄 转型 | 未披露 | OSS 招聘 + 悬赏边栏 |
| [EthicalAds](docs/ad-networks.md) | 广告(CPM) | ✅ 在营 | 70% 分成,~$2.50 CPM | 开发者文档站(5 万+月 PV) |
| Carbon Ads | 广告(CPC) | ✅ 在营 | 销售对接 | 精选开发者站(广告主 $5–10k/月起) |
| BuySellAds | 广告(多形态) | ✅ 在营 | 托管 | 邮件/原生/赞助/播客 |
| Passionfroot | 广告/市场 | 🔄 转型→Zest | 2% / 15% | Newsletter 品牌合作 |
| Paved | 广告(Newsletter) | ✅ 在营 | 固定 + PPC | Newsletter(2.5 万订阅 / 100 万 PV) |

完整结构化数据:[`data/platforms.yml`](data/platforms.yml)。

---

## 报价参考（估算）

> **经验估算 / 仅供参考。** 没有把"$/月"和"star 数"挂钩的公开市场标准。Star 只是热度代理,不是定价指标。请按**你自己的流量**重算:文档站广告 ≈ `月 PV / 1000 × ~$2.50`(EthicalAds 发布者 CPM);Newsletter ≈ `订阅数 × 打开率 × CTR × 目标 CPC`,可锚定 [JavaScript Weekly 18 万订阅 $3,590/期](https://cooperpress.com/files/cooperpress-media-kit-q2-2024.pdf)。**没有流量/转化数据时按低端报价**;成交 3 单后再涨。

月度美元,按 star 档 × 位类型(估算):

| Stars | README 顶 banner | README 底 logo | README 底文字 | 文档站广告 | Release note | Newsletter/期 |
|------:|---:|---:|---:|---:|---:|---:|
| 100 | $100–300 | $50–150 | $20–75 | $10–40 | $50–150 | $30–100 |
| 500 | $200–500 | $100–300 | $50–150 | $25–80 | $100–300 | $100–250 |
| 1,000 | $400–1,000 | $200–600 | $100–300 | $50–200 | $200–600 | $200–500 |
| 5,000 | $1,000–3,000 | $500–1,500 | $250–750 | $150–600 | $500–1,500 | $500–1,500 |
| 10,000 | $2,000–6,000 | $1,000–3,000 | $500–1,500 | $300–1,500 | $1,000–3,000 | $1,000–2,500 |
| 50,000 | $5,000–15,000 | $3,000–10,000 | $1,500–5,000 | $1,000–5,000 | $2,500–8,000 | $2,500–7,000 |

交易模式加成(估算):一次性 12 个月展示 ≈ 月价的 8–10 倍(打 15–20% 折);年付 ≈ 月价的 10–12 倍(15–20% 折);纯返佣 = 0 固定 + 10–30% 递归;**固定 + 返佣混合** = 较低月费 + 转化分成(最优模式)。完整网格 + 人民币国内区间见 [`data/pricing-benchmarks.yml`](data/pricing-benchmarks.yml);可复制报价卡见 [`templates/rate-card.md`](templates/rate-card.md)。

---

## 国内赞助商去哪找

不要群发。建一份评分过的 50 家名单。按优先级来源(完整方法见 [docs/outreach.md](docs/outreach.md)):

1. **依赖树里的国内公司**——谁的软件在用你的项目?他们的 DevRel/增长/商务团队最对口。对国内 AI/云/工具商,找**商务 BD / 开发者关系 / 增长负责人**。
2. **star/fork 你的公司账号**——GitHub 上给你 star/fork 的组织(Org);顺藤摸瓜找对口人,LinkedIn/即刻/脉脉/微信。
3. **相邻厂商**——和你一起部署的产品(托管、ORM、可观测、CI、代理)。
4. **实物赞助商(in-kind)**——托管/CI/密钥/监控厂商用额度换 logo(Homebrew 做法:MacStadium、1Password)。
5. **重度用户的 issue 报告者**——请他们引荐其雇主。

**国内典型 sponsor 类型:**
- **国内大模型 API 平台**(智谱 GLM、零一万物、Kimi/Moonshot、百炼/通义、DeepSeek、讯飞)——想触达用 API 的开发者,常做"API 额度 + 现金"组合赞助或分销。
- **云厂商**(阿里云、腾讯云、华为云、火山引擎)——开发者增长/云市场合作,可谈资源置换 + 现金。
- **开发者工具商**(JetBrains 中国、各类 SaaS、低代码/自动化厂商)——想在你仓库的决策时刻曝光。
- **独立开发者社区 / 出海工具商**——受众重合度高,谈返佣混合最实在。

用 [Sponsor Fit Score](tools/sponsor-fit-score.md) 给每家打分(0–100)。**61–100** 主攻;**0–30** 跳过。

---

## 国内渠道怎么发

| 渠道 | 怎么用 | 注意 |
|------|--------|------|
| **V2EX** | 发"分享创造"节点;技术真诚、先给价值再提合作,反软文 | 别当广告板,一次只发一个高质量帖 |
| **掘金** | 写技术深度专栏(非标题党),文末自然带仓库 + 赞助入口 | 标题党会被踩;内容要有干货 |
| **知乎** | 技术问答(你的仓库能解决的问题)+ 专栏文章 | 别硬广,先答问题建立可信度 |
| **微信群** | 开发者群/架构群/出海群里,先贡献再私信 | 别群发,一对一私信,尊重群规 |
| **公众号** | 自己写技术公众号;与同量级技术公众号互推 | 互推比硬投广告有效且不 low |
| **即刻 / 少数派** | 开发者密度高的社区,适合冷启动曝光 | 适合早期,量小但质高 |
| **X / Twitter** | 英文 thread + 截图,面向海外 sponsor | 配合 Product Hunt / HN 一起发 |

> 详见 [docs/launch-plan.md](docs/launch-plan.md) 第 7–8 节(V2EX / 掘金-知乎-公众号)。

---

## 人民币怎么报价 + 固定+返佣怎么设计

**人民币报价:** 美元价 × ~6–7 得到人民币"面值",但**国内 sponsor 常按国内行情付,不是简单 ×7**。1000 star 仓库国内常见区间是 **¥500–¥5,000/月**(README 底 logo / Release note 档);对国内 prospect 先按这个区间报,别一上来就报美元 ×7 的高价吓走人。人民币报价卡见 [`templates/rate-card.md`](templates/rate-card.md) 的 RMB 版本。

**固定费用 + 返佣(国内 BD 最常用模式):**

> "¥[X]/月 固定合作费,保证你的 logo/位曝光 + 基础流量;**外加**通过你的专属链接/口令转化的用户,按 [Y]% 返佣。双方按月对账,数字透明。"

为什么这个模式好:
- 对 sponsor:**下行风险封顶**(固定费可控),上行有动力。
- 对你:**保底现金流** + 转化好时不对称收益。
- 适合对象:`founder_growth`(增长负责人)、`ecosystem`(生态厂商)。

设计要点:
- 固定费按 [Sponsor Fit Score](tools/sponsor-fit-score.md) 评出的**转化路径**定——转化路径差就别加返佣腿,纯卖固定。
- 返佣比例国内常见 **10–30% 递归**或**¥X/注册**;给专属口令/链接便于归因。
- **签订书面合作协议**(对公走账需要),约定 term、对账周期、最低保证、取消条款。
- 国内走对公转账;海外 sponsor 走 Open Collective/GitHub Sponsors(需在受支持地区)。

---

## 怎么避免显得 low 或像接广告

赞助做不好会掉 star、掉口碑。守住这几条:

- **不接灰产/博彩/标题党/擦边广告。** 一条 [vetting policy](docs/sponsor-kit.md) 写明拒收类别,既保护口碑也方便对内拒绝。
- **README 赞助位克制。** 主流做法是一个底部 logo 网格(Vue/Vite/Astro/Homebrew 都这样),不是满屏 banner。Logo 网格用动态 SVG,永不手改 README。详见 [templates/readme-sponsor-block.md](templates/readme-sponsor-block.md)。
- **透明披露。** 赞助商标"赞助商",返佣链接标"返佣链接可能产生佣金",两者**分开标注**,别把返佣伪装成中立推荐。见 [templates/readme-sponsor-block.md](templates/readme-sponsor-block.md#affiliate-disclosure) 的 disclosure 片段。
- **只接你会无偿推荐的东西。** 一次坏推荐损失的可信度远超那点佣金。
- **别群发私信。** 50 家名单、3 次触达后即关单,不第四次骚扰。见 [tools/outreach-checklist.md](tools/outreach-checklist.md)。
- **调性匹配。** 隐私工具别接追踪广告商;安全工具别接可疑厂商。
- **把赞助和项目价值绑定。** 赞助页写清楚钱用在哪(维护工时、CI、文档托管),公开账本(Open Collective)让钱不进"黑箱"。

---

## 中文合作私信模板

可直接复制,填 `[方括号]`。完整版(微信私信、V2EX/掘金公开帖、回复有意向、回复拒绝)在 [`templates/dm-template.md`](templates/dm-template.md);中文邮件 + 跟进 + 被拒回复在 [`templates/cold-email.md`](templates/cold-email.md)。

**微信私信(示例,≤150 字):**

> [对方称呼]你好,我是 [你的项目] 的维护者。我们是个 [N] star 的 [项目定位] 工具,月下载约 [X] 万,用户和你们 [对方产品] 的开发者高度重合。我们在找合适的长期赞助伙伴,合作形式可以是 README/文档站 logo 位 + 专属口令返佣的混合模式,首月可以免费试。方便聊 15 分钟吗?

要点:先说**受众重合**而非 star 数;一个具体切入点;一个低门槛请求(15 分钟/首月免费);不堆形容词。

---

## 1000 stars 仓库的首个赞助成交

1000 star 是甜点区:有真实用户、真实下载、真实采购对话,但还能自己卖。完整方案见 [docs/1000-stars-playbook.md](docs/1000-stars-playbook.md),首个成交的关键:

1. **第一个 sponsor 往哪找:** 依赖树里**用你项目做产品**的国内公司(最对口),其次是 issue 里报重度用例的公司用户。别先去找大厂冷门部门。
2. **怎么定价:** 按 [报价表低端](#报价参考估算),1000 star 国内常见 ¥500–¥5,000/月。别开高价,目标是**先成交一单拿到案例**,不是一单吃撑。
3. **怎么包装:** 一页 [sponsor kit](templates/sponsor-kit.md)——下载量(可核实)、GitHub Traffic(标注"自报、14 天滚动窗口")、用户画像、空位、报价。一页就够。
4. **怎么发首批 50 封:** 见 [examples/1000-stars-repo.md](examples/1000-stars-repo.md#5-the-first-50-dms-plan) 的首批 50 计划;10 封一批,3 次触达后关单。
5. **首月低价测试:** 给前 3 家 prospect 报**首月半价或免费**,消除风险。一旦有人接受,你就有市场信号涨价。
6. **从第一单到第二单:** 用第一个 sponsor 的 logo + 一句话案例做**社会证明**,放进下一批私信——"XX 已经在赞助我们"。社会证明是成交第二单最强的加速器。
7. **别伤口碑:** 守 [vetting policy](docs/sponsor-kit.md),透明披露,不群发。1000 star 还很脆,一次烂赞助能掉几十个 star。

---

## 7 天冷启动计划

一周从"没赞助体系"到"首批私信已发 + 仓库已上线"。每天对应 [docs/launch-plan.md](docs/launch-plan.md) 与 [docs/1000-stars-playbook.md](docs/1000-stars-playbook.md) 里的清单。

| 天 | 做什么 | 产出 |
|---|---|---|
| **1** | 选平台;加 `.github/FUNDING.yml`;设 3–5 档(低端) | Sponsor 按钮上线 + 档位阶梯 |
| **2** | 列库存位;做一页 [报价卡](templates/rate-card.md) | 报价卡(内部锚点) |
| **3** | 拉 GitHub Traffic + npm/PyPI/Docker 下载量;做一页 [sponsor kit](templates/sponsor-kit.md) | 带"自报流量"声明的 kit |
| **4** | 建 50 家名单(依赖树、star 公司、相邻厂商);用 [Sponsor Fit Score](tools/sponsor-fit-score.md) 打分 | 评分过的名单 |
| **5** | 发第一批(10 家)用 [中文私信](templates/dm-template.md)/[邮件](templates/cold-email.md) | 10 封已发,已记录 |
| **6** | 发第二批(10 家);写发布稿(HN / Reddit / V2EX / X) | 发布素材就绪 |
| **7** | 上线 + 发独立赞助页;全部记进 [outreach checklist](tools/outreach-checklist.md) | 仓库上线,管线运行 |

第 7 天后:保持滚动 50 家管线,跑 3 次触达,持续更新让 star 自然增长(见 [docs/launch-plan.md](docs/launch-plan.md) 第 12 节)。

---

## 模板与工具

可直接复制,填 `[方括号]` 即用。

| 文件 | 是什么 |
|---|---|
| [templates/funding-yml-example.md](templates/funding-yml-example.md) | 带注释的 `.github/FUNDING.yml`——全部 12 个 key + 3 个完整示例 |
| [templates/rate-card.md](templates/rate-card.md) | 一页报价卡(美元 + 人民币,star 档 × 位网格) |
| [templates/cold-email.md](templates/cold-email.md) | 冷邮件 + 跟进 + 接受/拒绝回复(英文 + 中文) |
| [templates/dm-template.md](templates/dm-template.md) | LinkedIn / X / Discord / **微信私信** / V2EX-掘金 私信 |
| [templates/sponsor-kit.md](templates/sponsor-kit.md) | 完整 sponsor kit(填空 + 示例) |
| [templates/media-kit.md](templates/media-kit.md) | TLDR 式 media kit(全组件 + 示例) |
| [templates/readme-sponsor-block.md](templates/readme-sponsor-block.md) | README 顶/底/logo/文字/返佣披露 片段 |
| [templates/affiliate-tracker.csv](templates/affiliate-tracker.csv) | 返佣交易追踪 CSV |
| [tools/sponsor-fit-score.md](tools/sponsor-fit-score.md) | 0–100 prospect 评分模型 + 示例 |
| [tools/outreach-checklist.md](tools/outreach-checklist.md) | 50 家管线追踪(markdown + CSV) |

---

## 文档与数据

| 文档 | 内容 |
|---|---|
| [docs/getting-started.md](docs/getting-started.md) | 导览 + 5 分钟路径 + 链接地图 |
| [docs/github-sponsors.md](docs/github-sponsors.md) | 资格、地区(中国坑)、开通、档位、手续费、README 展示 |
| [docs/open-collective.md](docs/open-collective.md) | fiscal host、OSC 501(c)(6)、公开账本、方案/费 |
| [docs/polar.md](docs/polar.md) | 转型为 AI 计费/MoR——何时用、何时不 |
| [docs/ad-networks.md](docs/ad-networks.md) | EthicalAds、Carbon、BuySellAds、Passionfroot、Paved |
| [docs/affiliate-programs.md](docs/affiliate-programs.md) | 已核实返佣程序 + 辟谣清单 + 联盟网络 |
| [docs/pricing.md](docs/pricing.md) | 怎么定价(看流量不看 star)+ 估算网格 |
| [docs/sponsor-kit.md](docs/sponsor-kit.md) | 怎么搭 sponsor kit(指南)+ GitHub Traffic 事实 |
| [docs/readme-monetization.md](docs/readme-monetization.md) | README + 各表面变现(每个位) |
| [docs/outreach.md](docs/outreach.md) | 主动找赞助商 |
| [docs/1000-stars-playbook.md](docs/1000-stars-playbook.md) | 1000 star 十节方案 |
| [docs/launch-plan.md](docs/launch-plan.md) | 冷启动分发(HN/Reddit/PH/V2EX/掘金/X) |
| [docs/case-studies.md](docs/case-studies.md) | 已核实披露数字(Astro/Vue/Vite/Tailwind/Sentry/…) |
| [docs/faq.md](docs/faq.md) | 15+ 问答 |

数据(事实源):[`data/platforms.yml`](data/platforms.yml) · [`data/pricing-benchmarks.yml`](data/pricing-benchmarks.yml) · [`data/sponsor-types.yml`](data/sponsor-types.yml) · [`data/affiliate-programs.yml`](data/affiliate-programs.yml)。

英文版:[README.md](README.md)。

---

## 真实案例锚点

公开披露的数字(引用见 [docs/case-studies.md](docs/case-studies.md))。估算已标注。

| 项目 | 披露(来源) | 启示 |
|---|---|---|
| [Astro](https://opencollective.com/astrodotbuild) | OpenCollective 累计 $836k;档位到 $10,000/月 | 干净阶梯 + 赞助页 + fiscal host = 上限 |
| [Vue.js](https://opencollective.com/vuejs) | 累计 $852k | 自建赞助页 + BACKERS.md 也行 |
| [Vite](https://opencollective.com/vite) | 累计 $162k;Bronze $50 → Gold $500 | 简单阶梯也成立 |
| [Homebrew](https://opencollective.com/homebrew) | 累计 $486k | 实物(MacStadium/1Password)+ 现金混搭 |
| [Tailwind CSS](https://tailwindcss.com/sponsor) | Partner $5,000/月(估约 $200k/月,~70 家) | 旗舰规模下档位有效;商业收入 ≠ 赞助 |
| [Sentry](https://blog.sentry.io) | OSS 年支出 $155k→$750k;每工程师 $2,000/年承诺 | **赞助商**的预算口径 |
| [Caleb Porzio](https://calebporzio.com/i-just-hit-dollar-100000yr-on-github-sponsors-heres-how-i-did-it) | GitHub Sponsors $112,680/年 | 真实足迹上主动卖 |
| [komorebi(~10k★)](https://lgug2z.com/articles/github-sponsorship-breakdown-for-2024/) | $1,861/年(约 $155/月) | **10k star 不主动卖也才 $155/月** |

---

## 免责声明

本仓库所有价格、手续费、返佣比例、收入数字均为**经验估算 / 仅供参考**,不是报价、
不承诺收益、不构成财务/法律/税务建议。真实价格取决于垂直领域、流量、用户质量、转化率、
受众地区和赞助商预算。**使用前请向各平台核实当前条款。** 平台状态核实于 2026-06-29,会随时变化。
本项目不承诺任何收益,不是"割韭菜"教程——它是给想专业运营赞助的维护者的实战手册。

许可证:内容 [CC-BY-4.0](LICENSE);内嵌代码片段 MIT。详见 [LICENSE](LICENSE)。
