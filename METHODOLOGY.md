# Methods and source notes / 统计方法与来源说明

Source review date / 来源复核日期：**2026-11-11**

This collection contains published Amazon advertising figures across ten product categories. It includes 38 category rows, 6 overall rows, 9 trend rows and 9 source records. Each value retains its publisher and statistical label. Blank cells mean the metric is not included for that source/category; they do not mean zero.

本数据集汇集十个产品类目的亚马逊广告公开数字，包含 38 条类目记录、6 条整体记录、9 条趋势记录和 9 条来源记录。各数值保留发布方和统计标签；空白表示未收录该项指标，不代表零。

## Comparing figures / 比较口径

Sources differ in geography, ad type, measurement period, attribution and weighting. Category names are mapped for navigation; `category_as_published` preserves the original label because the underlying categories may differ. Figures are not pooled into a single industry average.

`ACoS spread` is the highest minus lowest reported ACoS within a mapped category, in percentage points. Tight is ≤5, Loose is >5 and ≤10, and None is >10. These labels describe numerical distance, not statistical confidence, sample representativeness or recommended performance targets.

各来源的地区、广告类型、统计时间、归因及加权方法不同。统一类目名称便于查询，原始名称保存在 `category_as_published`，实际类目范围可能不同；本仓库不将这些数值合成为行业平均值。

ACoS 差距为同一映射类目最高值减最低值，单位是百分点：≤5 为高，>5 且 ≤10 为一般，>10 为低。分档只描述数值距离，不代表统计可信度、样本代表性或推荐目标。

## Source-specific notes / 各来源说明

| Source | Scope and limitations / 口径与限制 |
|---|---|
| [Ad Badger](https://www.adbadger.com/blog/amazon-advertising-stats/) | The overview table gives ACoS 29.6% and CVR 11.1%; prose gives 30.67% and 11.72%. This collection uses the table, whose window is January–August 2026, while the introduction says through September. Ad types are not split and geography/weighting are unspecified. / 采用概览表数值；正文数值与日期存在冲突。广告类型未拆分，地区和加权方式未明确。 |
| [Autron](https://autron.ai/benchmark/amazon-ppc-benchmarks-by-category-2026) | Category figures are medians; overall figures are averages. Covers Sponsored Products, combining industry data with checks against managed accounts. Exact sample count, geography and measurement dates are unspecified. Report metadata gives publication June 3 and modification June 29, 2026. / 类目为中位数、整体为平均值；样本量、地区和统计起止日未明确。 |
| [Ryze AI](https://www.get-ryze.ai/blog/amazon-ads-benchmarks-acos-roas-and-cpc-by-category-2026) | Sponsored Products averages for 850+ US seller accounts with $25K+ monthly revenue. The stated 12-month window has no endpoints. The visible table has ten categories, although the methodology mentions fifteen. / 样本为月销 2.5 万美元以上的美国卖家；12 个月统计期未给起止日；本仓库收录页面可见的十个类目。 |
| [WisePPC](https://wiseppc.com/blog/amazon-sponsored-products-benchmarks/) | Account-level quartiles/medians for 69 accounts across marketplaces; CPC covers 19 US accounts. April 1–June 29, 2026, with 7-day attribution. The sample is not random. `p25` and `p75` mean percentiles, not calendar quarters. / 跨市场 69 个账户，CPC 限美国 19 个账户；统计期止于 6 月 29 日，7 天归因；四分位标签不表示季度。 |
| [Triple Whale](https://www.triplewhale.com/blog/amazon-benchmarks) | Blended Amazon ad activity, 2,800+ brands, August 2025–July 2026. Category CVR/ROAS are medians; overall weighting is unspecified. The page displays August 20, 2026 without labeling it as publication or update date. / 混合广告类型，类目指标为中位数；整体加权方法未说明，页面日期未标明类型。 |
| [Pacvue](https://pacvue.com/guides-reports/2026-q2-commerce-media-benchmark-report/) | Six selected category values come from the public report page. Its [holiday strategy article](https://pacvue.com/blog/how-to-build-a-winning-holiday-ecommerce-strategy/) explicitly identifies SB CVR +26.5% as Q2 2026 YoY. Sample size and aggregation are unspecified. July 15 publication date is attributed to Trellis. / 类目值来自公开报告页，SB 转化率同比来自官方文章；样本与汇总方法未披露，发布日期经 Trellis 转引。 |
| [Tinuiti](https://tinuiti.com/research-insights/research/digital-ads-benchmark-report-q2-2026/) | Four spend rows have primary support; four other trends use Trellis. Its $4B scale statement is annual managed spend across digital platforms, not an Amazon Q2 sample. The full report requires registration; publication date is unconfirmed. / 四条花费数据可查原文，其余四条趋势经转引；年度跨平台管理花费不等于 Amazon 样本规模。 |
| [Trellis](https://gotrellis.com/resources/blog/amazon-advertising-benchmarks) | Secondary compilation, posted March 11 and updated October 2, 2026. It publishes the compilation, rather than measuring the quoted vendors' datasets. / 汇编发布方，不是所引用数据的原始测量方。 |
| [Amazon Ads](https://advertising.amazon.com/en-ca/resources/whats-new/benchmarks-reporting-now-generally-available-worldwide) | First-party peer-brand reporting described in its May 18, 2026 announcement. Requires Brand Registry; sponsored ads use `crossProgramBenchmarks`, DSP uses `dspBenchmarks`. / 第一方同行品牌报告，需要品牌备案；不同广告体系使用相应 API 报告类型。 |

## Trend evidence / 趋势证据

Each row in [`data/ad_type_trends.csv`](data/ad_type_trends.csv) includes `evidence_url`. `verified_from_primary=yes` means its value and period are supported by a public page from the original publisher; it does not imply access to the full report or underlying account data.

Tinuiti spend figures are supported by its [Prime Day recap](https://tinuiti.com/blog/amazon/prime-day-recap/), [ROAS article](https://tinuiti.com/blog/measurement/defining-calculating-return-on-ad-spend-roas/) and Q2 report page. Four rows use the [Trellis compilation](https://gotrellis.com/resources/blog/amazon-advertising-benchmarks) and remain `verified_from_primary=no`: SP clicks +37%, SP CPC +1%, SB clicks +4%, and DSP impressions +60%. Pacvue's separate trend uses its holiday strategy article.

趋势表逐行保留证据链接。`yes` 表示发布方公开页面支持相应数值和时间口径，不表示取得完整报告或底层账户数据。仍标为 `no` 的四条 Tinuiti 记录为 SP 点击 +37%、SP CPC +1%、SB 点击 +4% 和 DSP 曝光 +60%，出处为 Trellis 汇编。

## CSV fields / 数据字段

- `_pct` fields contain percentages, not decimal fractions; `yoy_change_pct` is a relative year-over-year change. `_usd` fields contain US dollars; `roas` is a ratio. / 百分比字段采用百分数，同比字段为相对增幅；美元字段以美元计，ROAS 为倍数。
- `stat` distinguishes average, median, reported and percentile values. / `stat` 区分平均值、中位数、按原文报告值及分位数。
- [`data/sources.csv`](data/sources.csv) records the window, sample, ad types, geography, access route, vendor context and specific limitations. / 来源表记录时间窗、样本、广告类型、地区、获取方式、发布方背景及具体限制。
- [`data/overall_benchmarks.csv`](data/overall_benchmarks.csv) retains metric-specific sample and attribution notes. / 整体数据表保留指标子样本与归因说明。

For numerical comparisons, use the cited source's definition and the closest available match to your account. This repository reproduces published figures with attribution; it does not independently audit their underlying measurements.

实际比较时，应使用原发布方的指标定义，并选择与自己账户口径最接近的数据。本仓库注明出处整理公开数字，不对发布方的底层测量进行独立审计。
