# Verification notes / 核验记录

Reviewed on **2026-11-11 (Asia/Shanghai)**. This review checks the published numbers and the repository's interpretation of them; it does not audit publishers' underlying account data.

本次于 **2026-11-11（北京时间）**复核公开页面、CSV 和中英文说明，核验的是公开数字与本仓库的表述，不包括发布方的底层账户数据。

## Local consistency / 本地一致性

- 38 category rows, 6 overall rows, 9 trend rows and 9 source records. Existing benchmark numeric values are unchanged.
- Both README tables agree with the CSVs. The ten ACoS spreads were independently recalculated as maximum minus minimum; the ≤5 / >5–≤10 / >10 percentage-point bands agree.
- Primary keys, source references, numeric domains and date formats were checked. Missing metrics remain blank, not zero.
- 四张表的记录数分别为 38、6、9、9；原有基准数字未改动。中英文表格与 CSV 一致，十个类目的差距和分档重算无误；缺失指标仍为空值。

## Source findings / 来源结果

| Source | Evidence and remaining limits / 证据与限制 |
|---|---|
| [Ad Badger](https://www.adbadger.com/blog/amazon-advertising-stats/) | Stored values match the tables. Prose ACoS/CVR and page-wide dates conflict with table values/notes; we retain the tables and disclose the conflict. / 数字采用表格，保留与正文数值及日期不一致的说明。 |
| [Autron](https://autron.ai/benchmark/amazon-ppc-benchmarks-by-category-2026) | Category medians and overall averages confirmed. Publication and modification dates verified in Report JSON-LD. Exact sample count, geography and measurement window remain unspecified. / 类目为中位数、整体为平均值；具体样本量、地区和时间窗仍未明确。 |
| [Ryze AI](https://www.get-ryze.ai/blog/amazon-ads-benchmarks-acos-roas-and-cpc-by-category-2026) | Ten table rows confirmed; US sellers with $25K+ monthly revenue. The stated 12-month window has no endpoints. Category mapping is approximate. / 已核对十行表格；12 个月统计期未给起止日，类目映射不完全等同。 |
| [WisePPC](https://wiseppc.com/blog/amazon-sponsored-products-benchmarks/) | All quartile/median values confirmed: 69 accounts across marketplaces, CPC subset 19 US accounts, April 1–June 29, 7-day attribution. / 已核对四分位数和中位数；明确美国 CPC 子样本与归因窗口。 |
| [Triple Whale](https://www.triplewhale.com/blog/amazon-benchmarks) | Selected values now verified directly. Category CVR/ROAS are medians; overall weighting remains unspecified. The page shows August 20, 2026 without identifying the date type. / 当前可直接核对；类目指标为中位数，整体加权方法未说明，页面日期未标明类型。 |
| [Pacvue](https://pacvue.com/guides-reports/2026-q2-commerce-media-benchmark-report/) | All six selected category values are public. [Official holiday article](https://pacvue.com/blog/how-to-build-a-winning-holiday-ecommerce-strategy/) confirms SB CVR +26.5% YoY. Exact sample/method are unspecified; July 15 publication date is attributed to Trellis. / 已核对六个类目值和 SB 转化率同比；发布日期仅经 Trellis 转引。 |
| [Tinuiti](https://tinuiti.com/research-insights/research/digital-ads-benchmark-report-q2-2026/) | Four spend rows have primary support; four other trend rows remain secondary. $4B is annual cross-platform managed spend, not an Amazon Q2 sample. A previously stored July 15 publication date was unconfirmed and removed. / 四条花费数据可查原文，其余四条仍为转引；删去无法确认的发布日期。 |
| [Trellis](https://gotrellis.com/resources/blog/amazon-advertising-benchmarks) | Read as a secondary compilation; March 11 publication and October 2 update dates confirmed. / 是汇编发布方，不是被引用数据的原始测量方。 |
| [Amazon Ads](https://advertising.amazon.com/en-ca/resources/whats-new/benchmarks-reporting-now-generally-available-worldwide) | May 18 announcement, Brand Registry eligibility and API report types confirmed. / 已核对上线公告、品牌备案要求和两类 API 报告名。 |

## Trend provenance / 趋势追溯

Each row in [`data/ad_type_trends.csv`](data/ad_type_trends.csv) includes `evidence_url`. `verified_from_primary=yes` means the selected value and period were found in a publisher's public page; it does not imply access to the full report or raw data.

The four rows still marked `no` are Tinuiti Sponsored Products clicks (+37%) and CPC (+1%), Sponsored Brands clicks (+4%), and DSP impressions (+60%). Their reviewed evidence is the [Trellis compilation](https://gotrellis.com/resources/blog/amazon-advertising-benchmarks).

Primary support for spend figures is split across Tinuiti's [Prime Day recap](https://tinuiti.com/blog/amazon/prime-day-recap/), [ROAS article](https://tinuiti.com/blog/measurement/defining-calculating-return-on-ad-spend-roas/) and report page. Pacvue's separate trend uses its holiday article above.

趋势表逐行保留证据链接。`yes` 表示本次在发布方公开页面找到相应数值及时间口径，不代表取得完整报告或原始数据。仍标为 `no` 的四条 Tinuiti 记录为 SP 点击 +37%、SP CPC +1%、SB 点击 +4% 和 DSP 曝光 +60%，本次通过 Trellis 汇编核实。

## Scope and changes / 口径与改动

There is no common verified geography, ad type, attribution window or weighting scheme across these sources. A small numerical spread is not statistical confidence or proof of an industry average. The repository retains original category labels and distinguishes blended ads, category medians and metric-specific samples. Publication-date gaps and source conflicts remain explicit in [`data/sources.csv`](data/sources.csv).

各来源不存在已证实的统一地区、广告类型、归因窗口或加权方法。数值差距小不代表统计可信度高，也不能证明行业平均值。已保留原始类目名，并补充混合广告类型、类目中位数及指标子样本说明；缺失发布日期和来源内部冲突继续明确记录。

CSV changes are additive except for corrected metadata: `sources.csv` adds `geography` and `verification_note`; `ad_type_trends.csv` adds `evidence_url`; WisePPC scope labels use `p25`/`p75` rather than ambiguous Q1/Q3; Triple Whale category `stat` is corrected to `median`. No benchmark metric value was replaced.

新增 CSV 字段为地区、核验备注及趋势证据链接；修正 WisePPC 四分位标签和 Triple Whale 类目统计标签，并更新已核实的来源元数据。没有替换任何基准指标数值。
