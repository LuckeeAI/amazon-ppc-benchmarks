# 亚马逊广告基准数据 2026

把 2026 年能找到的亚马逊 Sponsored Products 公开基准数据（ACoS、CPC、CTR、转化率）放在一起对比，每个数字都注明来源、样本量、时间和发布方。

[English](README.md) · **简体中文**

![Data: CC BY 4.0](https://img.shields.io/badge/data-CC%20BY%204.0-15803d) ![Last checked 2026-11-09](https://img.shields.io/badge/last%20checked-2026--11--09-1f2937) ![Sources: 9](https://img.shields.io/badge/sources-9-0e7490)

由 [Luckee](https://luckee.ai/?utm_source=github&utm_medium=readme&utm_campaign=amazon-ppc-benchmarks&utm_content=intro-zh) 整理维护。原始数据在 [`data/`](data/) 目录，CSV 格式。

## 为什么要再做一份

搜"Amazon PPC benchmarks"能搜到十几个页面，每个类目都给一个很肯定的数字。把它们摆在一起看，同一个类目的 ACoS 有时能差 25 个点以上。原因是每家统计的都是自己的客户，时间段不同，"平均"的算法也不同。

这个仓库不替你判断哪家对。我们只收录能追溯到具名来源的数字，并标出各家之间差了多少。几家数据接近的类目，基准值有参考意义；差得远的类目，说明没人真正知道这个类目的平均水平，这时你自己的盈亏平衡 ACoS 更重要。

## 各类目 ACoS 和 CPC

美国站，2026 年。Autron 和 Ryze AI 只统计 Sponsored Products，Ad Badger 没有区分广告类型。每格为 `ACoS / CPC`，按原文照录。

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

**一致程度**按 ACoS 最高值减最低值计算：5 点以内为高，10 点以内为一般，超过 10 点为低。Ad Badger 是平均值，Autron 是中位数，Ryze AI 是月销 2.5 万美元以上美国卖家的平均值。各家类目名称不完全相同，我们做了统一，原始名称见 [`data/category_benchmarks.csv`](data/category_benchmarks.csv)。

几家数据都能看出的规律：

- **图书是投放成本最低的类目**，在每份数据里 CPC 都最低。
- **健康和美妆的点击最贵。** Pacvue（$2.18）和 Ryze AI（$2.89）都把健康家居列为 CPC 最高的类目。
- **Ryze AI 的 CPC 在每个类目都是最高的**，常常是另外两家的两倍。它只统计月销 2.5 万美元以上的卖家，这可能是部分原因。
- **服装类的平均值参考价值最低**，三家的 ACoS 从 29.9% 到 57% 不等。

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

Pacvue 给出的食品转化率 36.7% 远高于其他几家，很可能用的是不同的转化率定义，建议单独看待。

## 账户整体数据

| 来源 | ACoS | CPC | CTR | 转化率 | ROAS | 样本 |
|---|---|---|---|---|---|---|
| Ad Badger | 29.6% | $1.22 | 0.58% | 11.1% | | 工具用户，2026 年 1–8 月 |
| Autron | 34% | $1.13 | 0.56% | 10.5% | | 未说明 |
| WisePPC（中位数） | 28.2% | $0.82 | 0.69% | 5.85% | 3.55 | 69 个账户，2026 Q2 |
| Triple Whale | | | 0.56% | 10.77% | 3.08 | 2,800+ 品牌，2025 年 8 月至 2026 年 7 月 |

WisePPC 是唯一公布了分布区间的来源，中间一半账户的 ACoS 在 **16% 到 63%** 之间。比起任何一个平均值，这个区间更能说明"正常"是什么样子。它的转化率（5.85%）只有其他几家的一半左右。这个数是各账户数值的中位数，每个账户不论大小权重相同，不要直接和上面的平均值比。

## 趋势：花费在涨，Sponsored Products 的 CPC 基本没变

数据来自 Tinuiti 2026 年 Q2 数字广告基准报告（管理广告花费超过 40 亿美元，同比变化）：

| 广告类型 | 花费 | 其他 |
|---|---|---|
| Sponsored Products | +38%（剔除 Prime Day 后 +23%） | 点击 +37%，CPC +1% |
| Sponsored Brands | +20% | 点击 +4%，CPC 两位数增长 |
| Amazon DSP | +67% | 曝光 +60% |

Tinuiti 公开页面上只能看到 DSP 花费这一个数字，其余来自对付费报告的二手转述，在 [`data/ad_type_trends.csv`](data/ad_type_trends.csv) 中标为 `verified_from_primary=no`。

## 怎么用这些数据

**1. 先算出你自己的盈亏平衡 ACoS，再去和别人比。**

```
盈亏平衡 ACoS = (售价 − 产品成本 − 亚马逊费用 − 运费) ÷ 售价
```

一个售价 30 美元、成本加费用 12 美元的产品，盈亏平衡 ACoS 是 60%。对它来说，35% 的 ACoS 即使"高于基准"也是赚钱的；同样的 35% 放到毛利 25% 的产品上就是亏损。

**2. 只在几家数据一致的类目里参考基准。** 在一致程度"高"的类目，如果你的 ACoS 比区间高出 10 个点以上，值得查一查。一致程度"低"的类目，这张表说明不了太多。

**3. 从亚马逊后台拿你自己的同行基准。** 2026 年 5 月 18 日起，亚马逊广告的 Benchmarks 报告已经全面上线。它把你的 CTR、CPC、CPM 和新客指标，与同类目的匹配品牌做对比，后台和 API（`crossProgramBenchmarks`）都能用，需要品牌备案。这是唯一一个用你真实竞品算出来的基准。

## 看基准数据时要注意

类目基准回答的其实是"这家服务商管理的账户大概是什么水平"。用一个数字之前，先看清楚：

- **样本是谁。** 这里每个来源都是工具或代运营公司统计自己的客户，而用工具的卖家并不是普通卖家。
- **平均值还是中位数。** 几个大账户就能把平均值拉得离普通卖家很远。
- **归因窗口。** 同一组广告，7 天归因和 14 天归因算出的 ACoS 不一样。
- **广告类型。** Sponsored Brands 和 DSP 的数据不能和 Sponsored Products 直接比。
- **时间。** 2026 年 Prime Day 挪到了 6 月，Q2 和 Q3 的对比会因此偏移。

## 数据来源

| ID | 发布方 | 时间段 | 样本 | 获取方式 |
|---|---|---|---|---|
| `adbadger-2026` | [Ad Badger](https://www.adbadger.com/blog/amazon-advertising-stats/) | 2026 年 1–8 月 | 未说明 | 原文 |
| `autron-2026` | [Autron](https://autron.ai/benchmark/amazon-ppc-benchmarks-by-category-2026) | 2026 年 | 未说明 | 原文 |
| `ryze-2026` | [Ryze AI](https://www.get-ryze.ai/blog/amazon-ads-benchmarks-acos-roas-and-cpc-by-category-2026) | 12 个月 | 850+ 美国账户 | 原文 |
| `wiseppc-2026q2` | [WisePPC](https://wiseppc.com/blog/amazon-sponsored-products-benchmarks/) | 2026 年 4–6 月 | 69 个账户 | 原文 |
| `triplewhale-2026` | [Triple Whale](https://www.triplewhale.com/blog/amazon-benchmarks) | 2025 年 8 月至 2026 年 7 月 | 2,800+ 品牌 | 经 Trellis 转引 |
| `pacvue-2026q2` | [Pacvue](https://pacvue.com/guides-reports/2026-q2-commerce-media-benchmark-report/) | 2026 Q2 | 未说明 | 经 Trellis 转引（报告需注册） |
| `tinuiti-2026q2` | [Tinuiti](https://tinuiti.com/research-insights/research/digital-ads-benchmark-report-q2-2026/) | 2026 Q2 | 40 亿美元以上花费 | 部分来自二手转述 |
| `trellis-2026` | [Trellis](https://gotrellis.com/resources/blog/amazon-advertising-benchmarks) | 汇编 | | 原文 |
| `amazon-benchmarks-reporting` | [Amazon Ads](https://advertising.amazon.com/en-ca/resources/whats-new/benchmarks-reporting-now-generally-available-worldwide) | 你自己的账户 | 同类品牌 | 原文 |

每个来源的完整信息，包括发布方可能存在的偏差，见 [`data/sources.csv`](data/sources.csv)。所有数字已于 2026-11-09 对照原页面核对。数据版权归各发布方所有，本仓库注明出处引用，与以上任何一家都没有合作关系。

## 数据文件

| 文件 | 内容 |
|---|---|
| [`data/category_benchmarks.csv`](data/category_benchmarks.csv) | 每行一个类目 × 来源：ACoS、CPC、CTR、转化率、ROAS，以及是平均值还是中位数 |
| [`data/overall_benchmarks.csv`](data/overall_benchmarks.csv) | 账户整体数据，含 WisePPC 的四分位数 |
| [`data/ad_type_trends.csv`](data/ad_type_trends.csv) | 各广告类型的同比变化 |
| [`data/sources.csv`](data/sources.csv) | 每个来源的发布方、链接、日期、样本、方法、获取方式和偏差说明 |

## 参与贡献

发现了更新的报告、漏掉的来源，或者某个数字和原页面对不上？欢迎提 issue 或 PR，附上链接。每一行数据都需要一个公开链接和你核对的日期。无法追溯到具名来源的数字，我们不收录。

## 你的数据和基准之间

基准告诉你别的账户做到了什么水平，但不会告诉你哪些搜索词在浪费预算，哪些出价该调。

[Luckee](https://luckee.ai/features/amazon-ads?utm_source=github&utm_medium=readme&utm_campaign=amazon-ppc-benchmarks&utm_content=after-benchmarks-zh) 是你的 AI 亚马逊广告专家。它读取你自己的广告数据，解释 ACoS 为什么变了，并给出出价、预算和关键词的调整建议。每一项改动都要经你确认才会执行。[免费试用 7 天 →](https://luckee.ai/features/amazon-ads?utm_source=github&utm_medium=readme&utm_campaign=amazon-ppc-benchmarks&utm_content=after-benchmarks-cta-zh)

## 许可

数据和文字采用 [CC BY 4.0](LICENSE)。引用时请注明"Luckee, amazon-ppc-benchmarks"，并保留每个数字的原始来源链接。
