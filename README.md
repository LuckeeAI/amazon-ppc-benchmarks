# Amazon PPC Benchmarks 2026

Look up Amazon PPC benchmarks for ACoS, CPC, CTR, conversion rate and ROAS across 10 product categories. Compare published figures and download source-linked CSVs for account analysis, reporting or research.

**English** · [简体中文](README.zh-CN.md)

![Data: CC BY 4.0](https://img.shields.io/badge/data-CC%20BY%204.0-15803d) ![Last reviewed 2026-11-11](https://img.shields.io/badge/last%20reviewed-2026--11--11-1f2937) ![Sources: 9](https://img.shields.io/badge/sources-9-0e7490)

Maintained by [Luckee](https://luckee.ai/?utm_source=github&utm_medium=readme&utm_campaign=amazon-ppc-benchmarks&utm_content=intro). Raw data is in [`data/`](data/) as CSV.

**Jump to:** [Category ACoS / CPC](#acos-and-cpc-by-category) · [Conversion rates](#conversion-rate-by-category) · [Account-wide figures](#account-wide-numbers) · [CSV files](#data-files)

## ACoS and CPC by category

Each cell is `ACoS / CPC`, with CPC in USD. Autron and Ryze AI cover Sponsored Products; Ad Badger does not split ad types. Ryze AI explicitly covers US sellers, while the other two do not specify geography. Measurement windows are listed under [Sources](#sources).

<!-- table:category:start -->
| Category | Ad Badger | Autron | Ryze AI | Pacvue Q2 CPC | ACoS spread | Agreement |
|---|---|---|---|---|---|---|
| Toys & Games | 28% / $0.78 | 26% / $0.83 | 27.3% / $1.41 | | 2.0 pts | Tight |
| Home & Garden | 31% / $0.88 | 32% / $0.74 | 27.7% / $1.52 | | 4.3 pts | Tight |
| Electronics | 29% / $1.45 | 30% / $1.11 | 25.1% / $1.89 | | 4.9 pts | Tight |
| Sports & Outdoors | 33% / $0.82 | 31% / $1.00 | 27.0% / $1.34 | | 6.0 pts | Loose |
| Books | 19% / $0.38 | 26% / $0.40 | 18.2% / $0.89 | | 7.8 pts | Loose |
| Pet Supplies | 26% / $0.91 | 31% / $1.23 | 36.9% / $1.67 | | 10.9 pts | None |
| Beauty & Personal Care | 24% / $1.18 | 31% / $1.18 | 36.0% / $2.47 | | 12.0 pts | None |
| Health & Household | 27% / $1.05 | 36% / $1.42 | 40.7% / $2.89 | $2.18 | 13.7 pts | None |
| Food & Grocery | 21% / $0.58 | 23% / $0.56 | 34.8% / $1.98 | | 13.8 pts | None |
| Clothing & Apparel | 42% / $0.72 | 57% / $0.69 | 29.9% / $2.15 | $0.55 | 27.1 pts | None |
<!-- table:category:end -->

**Agreement** describes only the numerical ACoS spread (highest minus lowest): Tight ≤ 5 percentage points, Loose > 5 and ≤ 10, None > 10. It is not a confidence rating. Ad Badger figures are averages, Autron's are medians, Ryze AI's are averages from US sellers with $25K+ monthly revenue. Category names were mapped to a common set; these mappings are approximate and the original names are in [`data/category_benchmarks.csv`](data/category_benchmarks.csv).

Within the categories shown:

- **Books has the lowest CPC in the three ten-category datasets:** Ad Badger, Autron and Ryze AI. Lower CPC alone does not establish lower acquisition cost.
- **The highest CPC category depends on the source.** Electronics leads Ad Badger ($1.45); Health & Household leads Autron ($1.42) and Ryze AI ($2.89). Pacvue reports $2.18 for Health & Household, but this repo includes only two of its category CPC values.
- **Ryze AI's CPCs are the highest in every category**, often twice the others. Its sample is limited to sellers doing $25K+ a month, which may explain part of the gap.
- **Apparel has the widest ACoS spread in this table.** The three figures range from 29.9% to 57% and mix averages with a median.

## Conversion rate by category

| Category | Ad Badger | Autron | Other |
|---|---|---|---|
| Books | 18.0% | 13.3% | |
| Food & Grocery | 16.5% | 13.7% | Pacvue Q2: 36.7% |
| Beauty & Personal Care | 15.2% | 13.4% | |
| Pet Supplies | 14.0% | 13.6% | Triple Whale: 16.33% |
| Health & Household | 13.8% | 13.2% | |
| Toys & Games | 12.1% | 13.1% | |
| Home & Garden | 11.4% | 9.2% | Pacvue Q2 (Home & Kitchen): 6.6% |
| Sports & Outdoors | 10.3% | 9.2% | |
| Electronics | 9.5% | 9.4% | Triple Whale: 5.04% |
| Clothing & Apparel | 8.6% | 7.3% | |

Pacvue's 36.7% for grocery is far outside the other numbers. The available evidence does not establish whether this reflects the sample, period, attribution or metric definition; treat it separately. Triple Whale's category figures are medians across blended Amazon ad activity, rather than Sponsored Products-only values.

## Account-wide numbers

| Source | ACoS | CPC | CTR | CVR | ROAS | Sample |
|---|---|---|---|---|---|---|
| Ad Badger | 29.6% | $1.22 | 0.58% | 11.1% | | Tool users, Jan–Aug 2026 |
| Autron | 34% | $1.13 | 0.56% | 10.5% | | Not stated |
| WisePPC (median) | 28.2% | $0.82 | 0.69% | 5.85% | 3.55 | 69 accounts; CPC: 19 US accounts; Apr 1–Jun 29, 2026 |
| Triple Whale | | | 0.56% | 10.77% | 3.08 | 2,800+ brands, Aug 2025–Jul 2026 |

The middle half of WisePPC's sampled accounts run **16.0%–63.1% ACoS**. Its metrics use account-level medians and 7-day attribution across 69 accounts in multiple marketplaces; CPC covers only 19 US accounts. This range describes that sample, so account for differences in population and statistical method when comparing it with other sources.

Ad Badger values follow its overview table; its prose contains different figures and dates, detailed in [Methods and source notes](METHODOLOGY.md). Autron's overall figures are averages, while its category figures are medians. Triple Whale's overall values blend Amazon ad types.

## Trends: spend is up, Sponsored Products CPC is flat

Tinuiti Q2 2026 advertising figures, all year over year:

| Ad type | Spend | Other |
|---|---|---|
| Sponsored Products | +38% (+23% without Prime Day) | Clicks +37%, CPC +1% |
| Sponsored Brands | +20% | Clicks +4%, CPC up double digits |
| Amazon DSP | +67% | Impressions +60% |

Spend figures come from Tinuiti's public pages; clicks, CPC and DSP impressions are quoted via Trellis. Row-level evidence links and primary-verification flags are in [`data/ad_type_trends.csv`](data/ad_type_trends.csv).

## What to do with this

**1. Work out your break-even ACoS before comparing yourself to anyone.**

```
break-even ACoS = (price − product cost − Amazon fees − shipping) ÷ price
```

A $30 product with $12 in the costs listed above has a 60% break-even ACoS under this simplified formula. A 35% ACoS covers those costs; it would not cover them if the pre-ad contribution margin were only 25%. Include other variable costs, such as returns, in your own calculation.

**2. Match the scope before using a benchmark.** Compare ad type, geography, period, attribution and statistic first. A "Tight" label only means the displayed numbers are close; it does not establish a target ACoS or a threshold for changing bids.

**3. Check Amazon's peer-brand benchmarks.** Amazon's May 18, 2026 announcement describes Benchmarks reporting for CTR, CPC, CPM and new-to-brand metrics, using comparable category brands. It requires Brand Registry and is available in the ad console and API (`crossProgramBenchmarks` for sponsored ads; `dspBenchmarks` for DSP). The peer set is selected by Amazon, rather than being a list of your chosen competitors.

## Analyze your Amazon ads with Luckee

After checking the category benchmarks, find the changes worth considering in your own account.

[Luckee](https://luckee.ai/features/amazon-ads?utm_source=github&utm_medium=readme&utm_campaign=amazon-ppc-benchmarks&utm_content=after-benchmarks) is your AI Amazon PPC expert. Connect your advertising data or upload a report to analyze campaigns, search terms and keywords. Review bid, budget and negative-keyword recommendations, and approve each change before it runs.

[Try free for 7 days →](https://luckee.ai/features/amazon-ads?utm_source=github&utm_medium=readme&utm_campaign=amazon-ppc-benchmarks&utm_content=after-benchmarks-cta)

## Reading a benchmark

Match these dimensions before comparing a benchmark with your own account:

- **Who's in the sample.** Vendor datasets mainly represent their customers; Autron also describes cross-checking industry data, Trellis compiles other reports, and Amazon provides first-party peer matching. None of these establishes a random sample of all sellers.
- **Average, median or weighted aggregate.** These answer different questions. Large accounts can dominate pooled metrics, while an account-level median gives each account equal rank; several publishers do not fully disclose weighting.
- **Attribution window.** 7-day and 14-day attribution give different ACoS for the same campaigns.
- **Ad type.** Sponsored Brands and DSP numbers are not comparable to Sponsored Products.
- **Date.** [Amazon scheduled US Prime Day for June 23–26, 2026](https://www.aboutamazon.com/news/retail/amazon-prime-day-june-2026), which affects comparisons involving Q2 and Q3.

## Sources

| ID | Publisher | Window | Sample | Access |
|---|---|---|---|---|
| `adbadger-2026` | [Ad Badger](https://www.adbadger.com/blog/amazon-advertising-stats/) | Jan–Aug 2026 | Not stated | Primary |
| `autron-2026` | [Autron](https://autron.ai/benchmark/amazon-ppc-benchmarks-by-category-2026) | 2026 | Not stated | Primary |
| `ryze-2026` | [Ryze AI](https://www.get-ryze.ai/blog/amazon-ads-benchmarks-acos-roas-and-cpc-by-category-2026) | 12 months | 850+ US accounts | Primary |
| `wiseppc-2026q2` | [WisePPC](https://wiseppc.com/blog/amazon-sponsored-products-benchmarks/) | Apr 1–Jun 29, 2026 | 69 accounts; US CPC: 19 | Primary |
| `triplewhale-2026` | [Triple Whale](https://www.triplewhale.com/blog/amazon-benchmarks) | Aug 2025–Jul 2026 | 2,800+ brands | Primary |
| `pacvue-2026q2` | [Pacvue](https://pacvue.com/guides-reports/2026-q2-commerce-media-benchmark-report/) | Q2 2026 | Not stated | Public primary excerpts; full report gated |
| `tinuiti-2026q2` | [Tinuiti](https://tinuiti.com/research-insights/research/digital-ads-benchmark-report-q2-2026/) | Q2 2026 | Amazon sample not disclosed | Primary spend figures; other trends via summaries |
| `trellis-2026` | [Trellis](https://gotrellis.com/resources/blog/amazon-advertising-benchmarks) | Compilation | | Primary |
| `amazon-benchmarks-reporting` | [Amazon Ads](https://advertising.amazon.com/en-ca/resources/whats-new/benchmarks-reporting-now-generally-available-worldwide) | Your account | Peer brands | Primary |

Publisher links, measurement windows, samples and methods are in [`data/sources.csv`](data/sources.csv). See [Methods and source notes](METHODOLOGY.md) for secondary citations and specific limitations. Figures are attributed to their original publishers; Luckee independently maintains this collection.

## Data files

| File | Contents |
|---|---|
| [`data/category_benchmarks.csv`](data/category_benchmarks.csv) | One row per category × source: ACoS, CPC, CTR, CVR, ROAS, and whether it's an average or median |
| [`data/overall_benchmarks.csv`](data/overall_benchmarks.csv) | Account-wide figures, including WisePPC's quartiles |
| [`data/ad_type_trends.csv`](data/ad_type_trends.csv) | Year-over-year changes by ad type |
| [`data/sources.csv`](data/sources.csv) | Publisher, URL, dates, sample, method, access and bias note for every source |

## Contributing

Found a newer report, a source we missed, or a number that doesn't match its page? Open an issue or PR with the link. Every row needs a public URL and the date you checked it. We don't accept figures we can't trace to a named source.

## License

Luckee's original text and compilation are licensed under [CC BY 4.0](LICENSE). Credit "Luckee, amazon-ppc-benchmarks" and retain the source links for each figure. Third-party material remains subject to its owners' rights; this license does not grant rights that Luckee does not hold.
