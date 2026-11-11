# 亚马逊广告基准数据 2026

查询亚马逊广告的 ACoS、CPC、CTR、转化率和 ROAS，按 10 个产品类目对照公开参考数据。提供附有来源的 CSV，方便你分析账户表现、制作报告或开展研究。

[English](README.md) · **简体中文**

![Data: CC BY 4.0](https://img.shields.io/badge/data-CC%20BY%204.0-15803d) ![Last reviewed 2026-11-11](https://img.shields.io/badge/last%20reviewed-2026--11--11-1f2937) ![Sources: 9](https://img.shields.io/badge/sources-9-0e7490)

由 [Luckee](https://luckee.ai/?utm_source=github&utm_medium=readme&utm_campaign=amazon-ppc-benchmarks&utm_content=intro-zh) 整理维护。原始数据在 [`data/`](data/) 目录，CSV 格式。

**快速查看：** [类目 ACoS / CPC](#各类目-acos-和-cpc) · [类目转化率](#各类目转化率) · [账户整体数据](#账户整体数据) · [CSV 文件](#数据文件)

## 各类目 ACoS 和 CPC

每格为 `ACoS / CPC`，CPC 单位为美元。Autron、Ryze AI 统计 Sponsored Products，Ad Badger 未拆分广告类型。Ryze AI 明确覆盖美国卖家，另外两家未明确地区；各来源时间窗见[数据来源](#数据来源)。

| 类目 | Ad Badger | Autron | Ryze AI | Pacvue Q2 CPC | ACoS 差距 | 一致程度 |
|---|---|---|---|---|---|---|
| 玩具游戏 | 28% / $0.78 | 26% / $0.83 | 27.3% / $1.41 | | 2.0 点 | 高 |
| 家居园艺 | 31% / $0.88 | 32% / $0.74 | 27.7% / $1.52 | | 4.3 点 | 高 |
| 电子产品 | 29% / $1.45 | 30% / $1.11 | 25.1% / $1.89 | | 4.9 点 | 高 |
| 运动户外 | 33% / $0.82 | 31% / $1.00 | 27.0% / $1.34 | | 6.0 点 | 一般 |
| 图书 | 19% / $0.38 | 26% / $0.40 | 18.2% / $0.89 | | 7.8 点 | 一般 |
| 宠物用品 | 26% / $0.91 | 31% / $1.23 | 36.9% / $1.67 | | 10.9 点 | 低 |
| 美妆个护 | 24% / $1.18 | 31% / $1.18 | 36.0% / $2.47 | | 12.0 点 | 低 |
| 健康家居 | 27% / $1.05 | 36% / $1.42 | 40.7% / $2.89 | $2.18 | 13.7 点 | 低 |
| 食品杂货 | 21% / $0.58 | 23% / $0.56 | 34.8% / $1.98 | | 13.8 点 | 低 |
| 服装 | 42% / $0.72 | 57% / $0.69 | 29.9% / $2.15 | $0.55 | 27.1 点 | 低 |

**一致程度**只描述 ACoS 数值差距，即最高值减最低值：≤5 个百分点为高，>5 且 ≤10 为一般，>10 为低，不是可信度评级。Ad Badger 是平均值，Autron 是中位数，Ryze AI 是月销 2.5 万美元以上美国卖家的平均值。类目名称的统一只是近似映射，原始名称见 [`data/category_benchmarks.csv`](data/category_benchmarks.csv)。

在本表收录的类目中：

- **图书的 CPC 在三份十类目数据中最低：** Ad Badger、Autron 和 Ryze AI。较低的 CPC 本身不代表较低的获客成本。
- **CPC 最高的类目因来源而异。** Ad Badger 是电子产品（$1.45），Autron 和 Ryze AI 是健康家居（分别为 $1.42、$2.89）。Pacvue 的健康家居为 $2.18，但本仓库只收录了它的两个类目 CPC 值。
- **Ryze AI 的 CPC 在每个类目都是最高的**，常常是另外两家的两倍。它只统计月销 2.5 万美元以上的卖家，这可能是部分原因。
- **服装类在本表中的 ACoS 差距最大**，三家的数字从 29.9% 到 57% 不等，其中混有平均值和中位数。

## 各类目转化率

| 类目 | Ad Badger | Autron | 其他 |
|---|---|---|---|
| 图书 | 18.0% | 13.3% | |
| 食品杂货 | 16.5% | 13.7% | Pacvue Q2：36.7% |
| 美妆个护 | 15.2% | 13.4% | |
| 宠物用品 | 14.0% | 13.6% | Triple Whale：16.33% |
| 健康家居 | 13.8% | 13.2% | |
| 玩具游戏 | 12.1% | 13.1% | |
| 家居园艺 | 11.4% | 9.2% | Pacvue Q2（Home & Kitchen）：6.6% |
| 运动户外 | 10.3% | 9.2% | |
| 电子产品 | 9.5% | 9.4% | Triple Whale：5.04% |
| 服装 | 8.6% | 7.3% | |

Pacvue 给出的食品转化率 36.7% 远高于其他几家。现有证据无法判断差距来自样本、时间、归因还是指标定义，应单独看待。Triple Whale 的类目数字是混合亚马逊广告类型的中位数，并非只统计 Sponsored Products。

## 账户整体数据

| 来源 | ACoS | CPC | CTR | 转化率 | ROAS | 样本 |
|---|---|---|---|---|---|---|
| Ad Badger | 29.6% | $1.22 | 0.58% | 11.1% | | 工具用户，2026 年 1–8 月 |
| Autron | 34% | $1.13 | 0.56% | 10.5% | | 未说明 |
| WisePPC（中位数） | 28.2% | $0.82 | 0.69% | 5.85% | 3.55 | 69 个账户；CPC 为美国 19 个账户；2026 年 4 月 1 日至 6 月 29 日 |
| Triple Whale | | | 0.56% | 10.77% | 3.08 | 2,800+ 品牌，2025 年 8 月至 2026 年 7 月 |

WisePPC 样本中间一半账户的 ACoS 为 **16.0%–63.1%**。其指标采用账户中位数和 7 天归因，覆盖多个市场的 69 个账户；CPC 仅覆盖美国 19 个账户。这个区间描述该样本的分布，使用时需留意它与其他来源的样本和统计方法差异。

Ad Badger 采用概览表数值，其正文存在不同数值和日期，详见[统计方法与来源说明](METHODOLOGY.md)。Autron 整体数字为平均值、类目数字为中位数；Triple Whale 整体数字混合不同广告类型。

## 趋势：花费在涨，Sponsored Products 的 CPC 基本没变

Tinuiti 2026 年 Q2 广告数据，以下均为同比变化：

| 广告类型 | 花费 | 其他 |
|---|---|---|
| Sponsored Products | +38%（剔除 Prime Day 后 +23%） | 点击 +37%，CPC +1% |
| Sponsored Brands | +20% | 点击 +4%，CPC 两位数增长 |
| Amazon DSP | +67% | 曝光 +60% |

花费数据来自 Tinuiti 公开页面；点击、CPC 和 DSP 曝光数据经 Trellis 转引。逐行出处和原文核验标记见 [`data/ad_type_trends.csv`](data/ad_type_trends.csv)。

## 怎么用这些数据

**1. 先算出你自己的盈亏平衡 ACoS，再去和别人比。**

```
盈亏平衡 ACoS = (售价 − 产品成本 − 亚马逊费用 − 运费) ÷ 售价
```

一个售价 30 美元、上述成本合计 12 美元的产品，按这个简化公式算出的盈亏平衡 ACoS 是 60%。35% 的 ACoS 可以覆盖这些成本；如果扣除广告费前的贡献毛利率只有 25%，同样的 35% 就无法覆盖。实际判断时还需计入退货等其他变动成本。

**2. 先匹配统计口径，再参考基准。** 核对广告类型、地区、时间、归因和统计方法。一致程度“高”只表示表中的数字接近，不能据此确定目标 ACoS 或调整出价的阈值。

**3. 查看亚马逊的同行品牌基准。** 亚马逊 2026 年 5 月 18 日的公告介绍了 Benchmarks 报告，用同类目的可比品牌对照 CTR、CPC、CPM 和新客指标。该功能需要品牌备案，可通过广告后台和 API 使用：Sponsored Ads 对应 `crossProgramBenchmarks`，DSP 对应 `dspBenchmarks`。同行品牌由亚马逊匹配，不等于你自行指定的竞品名单。

## 用 Luckee 分析你的广告账户

查完类目基准，下一步是找出自己账户里值得调整的地方。

[Luckee](https://luckee.ai/features/amazon-ads?utm_source=github&utm_medium=readme&utm_campaign=amazon-ppc-benchmarks&utm_content=after-benchmarks-zh) 是你的 AI 亚马逊广告专家。连接广告数据或上传报表，分析广告活动、搜索词和关键词，查看出价、预算及否定关键词建议，并在执行前逐项确认。

[免费试用 7 天 →](https://luckee.ai/features/amazon-ads?utm_source=github&utm_medium=readme&utm_campaign=amazon-ppc-benchmarks&utm_content=after-benchmarks-cta-zh)

## 看基准数据时要注意

比较自己的广告表现时，先对齐以下口径：

- **样本是谁。** 服务商数据主要代表自己的客户；Autron 还说明使用行业数据交叉核对，Trellis 汇编其他报告，亚马逊提供第一方同行匹配。这些都不能视为全体卖家的随机样本。
- **平均值、中位数还是加权汇总。** 它们回答的问题不同。大账户可能主导汇总指标，账户中位数则给各账户相同的排序权重；部分来源没有完整披露加权方法。
- **归因窗口。** 同一组广告，7 天归因和 14 天归因算出的 ACoS 不一样。
- **广告类型。** Sponsored Brands 和 DSP 的数据不能和 Sponsored Products 直接比。
- **时间。** [亚马逊公布美国 2026 年 Prime Day 为 6 月 23–26 日](https://www.aboutamazon.com/news/retail/amazon-prime-day-june-2026)，涉及 Q2、Q3 的比较需要考虑活动时间变化。

## 数据来源

| ID | 发布方 | 时间段 | 样本 | 获取方式 |
|---|---|---|---|---|
| `adbadger-2026` | [Ad Badger](https://www.adbadger.com/blog/amazon-advertising-stats/) | 2026 年 1–8 月 | 未说明 | 原文 |
| `autron-2026` | [Autron](https://autron.ai/benchmark/amazon-ppc-benchmarks-by-category-2026) | 2026 年 | 未说明 | 原文 |
| `ryze-2026` | [Ryze AI](https://www.get-ryze.ai/blog/amazon-ads-benchmarks-acos-roas-and-cpc-by-category-2026) | 12 个月 | 850+ 美国账户 | 原文 |
| `wiseppc-2026q2` | [WisePPC](https://wiseppc.com/blog/amazon-sponsored-products-benchmarks/) | 2026 年 4 月 1 日至 6 月 29 日 | 69 个账户；美国 CPC：19 个 | 原文 |
| `triplewhale-2026` | [Triple Whale](https://www.triplewhale.com/blog/amazon-benchmarks) | 2025 年 8 月至 2026 年 7 月 | 2,800+ 品牌 | 原文 |
| `pacvue-2026q2` | [Pacvue](https://pacvue.com/guides-reports/2026-q2-commerce-media-benchmark-report/) | 2026 Q2 | 未说明 | 公开原文摘录；完整报告需登记 |
| `tinuiti-2026q2` | [Tinuiti](https://tinuiti.com/research-insights/research/digital-ads-benchmark-report-q2-2026/) | 2026 Q2 | Amazon 样本规模未披露 | 花费数据来自原文；其余趋势经转引 |
| `trellis-2026` | [Trellis](https://gotrellis.com/resources/blog/amazon-advertising-benchmarks) | 汇编 | | 原文 |
| `amazon-benchmarks-reporting` | [Amazon Ads](https://advertising.amazon.com/en-ca/resources/whats-new/benchmarks-reporting-now-generally-available-worldwide) | 你自己的账户 | 同类品牌 | 原文 |

每个来源的链接、统计时间、样本和方法见 [`data/sources.csv`](data/sources.csv)；转引方式和具体限制见[统计方法与来源说明](METHODOLOGY.md)。各项数字归其原发布方，本仓库由 Luckee 独立整理。

## 数据文件

| 文件 | 内容 |
|---|---|
| [`data/category_benchmarks.csv`](data/category_benchmarks.csv) | 每行一个类目 × 来源：ACoS、CPC、CTR、转化率、ROAS，以及是平均值还是中位数 |
| [`data/overall_benchmarks.csv`](data/overall_benchmarks.csv) | 账户整体数据，含 WisePPC 的四分位数 |
| [`data/ad_type_trends.csv`](data/ad_type_trends.csv) | 各广告类型的同比变化 |
| [`data/sources.csv`](data/sources.csv) | 每个来源的发布方、链接、日期、样本、方法、获取方式和偏差说明 |

## 参与贡献

发现了更新的报告、漏掉的来源，或者某个数字和原页面对不上？欢迎提 issue 或 PR，附上链接。每一行数据都需要一个公开链接和你核对的日期。无法追溯到具名来源的数字，我们不收录。

## 许可

Luckee 原创文字和汇编采用 [CC BY 4.0](LICENSE)。引用时请注明“Luckee, amazon-ppc-benchmarks”，并保留每个数字的来源链接。第三方材料仍受其权利人权利约束，本许可不授予 Luckee 不拥有的权利。
