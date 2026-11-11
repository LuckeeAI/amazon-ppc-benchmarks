# Amazon PPC Benchmarks 2026

Public 2026 benchmarks for Amazon Sponsored Products ACoS, CPC, CTR and conversion rate, side by side, with the sample size, date and vendor behind each number.

**English** · [简体中文](README.zh-CN.md)

![Data: CC BY 4.0](https://img.shields.io/badge/data-CC%20BY%204.0-15803d) ![Last checked 2026-11-09](https://img.shields.io/badge/last%20checked-2026--11--09-1f2937) ![Sources: 9](https://img.shields.io/badge/sources-9-0e7490)

Maintained by [Luckee](https://luckee.ai/?utm_source=github&utm_medium=readme&utm_campaign=amazon-ppc-benchmarks&utm_content=intro). Raw data is in [`data/`](data/) as CSV.

## Why another benchmark page

Search "Amazon PPC benchmarks" and you get a dozen pages, each with one confident number per category. Put them next to each other and they disagree, sometimes by more than 25 ACoS points for the same category. Each publisher measures its own customers, over its own window, with its own definition of "average".

This repo doesn't pick a winner. It lists every number we could trace to a named source and shows how far apart they are. When the sources agree, the benchmark is useful. When they don't, the honest answer is that nobody knows the category average, and your own break-even ACoS matters more.

## ACoS and CPC by category

US, 2026. Autron and Ryze AI cover Sponsored Products only; Ad Badger doesn't split by ad type. Each cell is `ACoS / CPC` as published.

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

**Agreement** is based on the ACoS spread (highest minus lowest): Tight ≤ 5 pts, Loose ≤ 10 pts, None above that. Ad Badger figures are averages, Autron's are medians, Ryze AI's are averages from $25K+/month US sellers. Category names were mapped to a common set; the original names are in [`data/category_benchmarks.csv`](data/category_benchmarks.csv).

Some patterns hold across every source:

- **Books is the cheapest category to advertise.** It has the lowest CPC in every dataset.
- **Health and beauty clicks cost the most.** Health & Household is the most expensive category for Pacvue ($2.18) and Ryze AI ($2.89).
- **Ryze AI's CPCs are the highest in every category**, often twice the others. Its sample is limited to sellers doing $25K+ a month, which may explain part of the gap.
- **Apparel is where averages mean least.** The three ACoS figures range from 29.9% to 57%.

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

Pacvue's 36.7% for grocery is far outside the other numbers, which suggests a different definition of conversion. Treat it as its own measure.

## Account-wide numbers

| Source | ACoS | CPC | CTR | CVR | ROAS | Sample |
|---|---|---|---|---|---|---|
| Ad Badger | 29.6% | $1.22 | 0.58% | 11.1% | | Tool users, Jan–Aug 2026 |
| Autron | 34% | $1.13 | 0.56% | 10.5% | | Not stated |
| WisePPC (median) | 28.2% | $0.82 | 0.69% | 5.85% | 3.55 | 69 accounts, Q2 2026 |
| Triple Whale | | | 0.56% | 10.77% | 3.08 | 2,800+ brands, Aug 2025–Jul 2026 |

WisePPC is the only source that publishes a spread, not just a midpoint. The middle half of its accounts run **16% to 63% ACoS**. That range is a better picture of "normal" than any single average. Its conversion rate (5.85%) is about half the others. It's the median of per-account values, where every account counts equally regardless of size, so don't compare it directly with the averages above.

## Trends: spend is up, Sponsored Products CPC is flat

From Tinuiti's Q2 2026 Digital Ads Benchmark Report (more than $4B in managed spend, year over year):

| Ad type | Spend | Other |
|---|---|---|
| Sponsored Products | +38% (+23% without Prime Day) | Clicks +37%, CPC +1% |
| Sponsored Brands | +20% | Clicks +4%, CPC up double digits |
| Amazon DSP | +67% | Impressions +60% |

Only the DSP spend figure appears on Tinuiti's public page. The rest comes from secondary summaries of the gated report, so it's marked `verified_from_primary=no` in [`data/ad_type_trends.csv`](data/ad_type_trends.csv).

## What to do with this

**1. Work out your break-even ACoS before comparing yourself to anyone.**

```
break-even ACoS = (price − product cost − Amazon fees − shipping) ÷ price
```

A $30 product with $12 in costs and fees has a 60% break-even ACoS. A 35% ACoS is profitable for that product even if it is "above benchmark". The same 35% loses money on a product with a 25% margin.

**2. Use the benchmark only where the sources agree.** In a "Tight" category, an ACoS 10+ points above the band is worth a look. In a "None" category, the table tells you very little.

**3. Pull your own peer benchmark from Amazon.** Since May 18, 2026, Amazon Ads Benchmarks reporting compares your CTR, CPC, CPM and new-to-brand metrics with matched peer brands in your category, in the ad console and the API (`crossProgramBenchmarks`). It needs Brand Registry. It's the only benchmark built from your actual competitors.

## Reading a benchmark

A category benchmark answers "what do accounts like the ones this vendor manages look like". Before you rely on a number, check:

- **Who's in the sample.** Every source here is a tool or agency measuring its own customers. Tool users are not average sellers.
- **Average or median.** A few large accounts can pull an average far from the typical seller.
- **Attribution window.** 7-day and 14-day attribution give different ACoS for the same campaigns.
- **Ad type.** Sponsored Brands and DSP numbers are not comparable to Sponsored Products.
- **Date.** Prime Day moved to June in 2026, which shifts any Q2 vs Q3 comparison.

## Sources

| ID | Publisher | Window | Sample | Access |
|---|---|---|---|---|
| `adbadger-2026` | [Ad Badger](https://www.adbadger.com/blog/amazon-advertising-stats/) | Jan–Aug 2026 | Not stated | Primary |
| `autron-2026` | [Autron](https://autron.ai/benchmark/amazon-ppc-benchmarks-by-category-2026) | 2026 | Not stated | Primary |
| `ryze-2026` | [Ryze AI](https://www.get-ryze.ai/blog/amazon-ads-benchmarks-acos-roas-and-cpc-by-category-2026) | 12 months | 850+ US accounts | Primary |
| `wiseppc-2026q2` | [WisePPC](https://wiseppc.com/blog/amazon-sponsored-products-benchmarks/) | Apr–Jun 2026 | 69 accounts | Primary |
| `triplewhale-2026` | [Triple Whale](https://www.triplewhale.com/blog/amazon-benchmarks) | Aug 2025–Jul 2026 | 2,800+ brands | Via Trellis |
| `pacvue-2026q2` | [Pacvue](https://pacvue.com/guides-reports/2026-q2-commerce-media-benchmark-report/) | Q2 2026 | Not stated | Via Trellis (gated) |
| `tinuiti-2026q2` | [Tinuiti](https://tinuiti.com/research-insights/research/digital-ads-benchmark-report-q2-2026/) | Q2 2026 | $4B+ spend | Partly via summaries |
| `trellis-2026` | [Trellis](https://gotrellis.com/resources/blog/amazon-advertising-benchmarks) | Compilation | | Primary |
| `amazon-benchmarks-reporting` | [Amazon Ads](https://advertising.amazon.com/en-ca/resources/whats-new/benchmarks-reporting-now-generally-available-worldwide) | Your account | Peer brands | Primary |

Full details, including each vendor's possible bias, are in [`data/sources.csv`](data/sources.csv). All figures were checked against the linked pages on 2026-11-09. The numbers belong to their publishers. This repo quotes them with attribution and isn't affiliated with any of them.

## Data files

| File | Contents |
|---|---|
| [`data/category_benchmarks.csv`](data/category_benchmarks.csv) | One row per category × source: ACoS, CPC, CTR, CVR, ROAS, and whether it's an average or median |
| [`data/overall_benchmarks.csv`](data/overall_benchmarks.csv) | Account-wide figures, including WisePPC's quartiles |
| [`data/ad_type_trends.csv`](data/ad_type_trends.csv) | Year-over-year changes by ad type |
| [`data/sources.csv`](data/sources.csv) | Publisher, URL, dates, sample, method, access and bias note for every source |

## Contributing

Found a newer report, a source we missed, or a number that doesn't match its page? Open an issue or PR with the link. Every row needs a public URL and the date you checked it. We don't accept figures we can't trace to a named source.

## Your number vs. the benchmark

A benchmark tells you where other accounts landed. It doesn't tell you which of your search terms are wasting spend or which bids to change.

[Luckee](https://luckee.ai/features/amazon-ads?utm_source=github&utm_medium=readme&utm_campaign=amazon-ppc-benchmarks&utm_content=after-benchmarks) is your AI Amazon PPC expert. It reads your own campaign data, explains why ACoS moved, and proposes bid, budget and keyword changes. Nothing runs until you approve it. [Try free for 7 days →](https://luckee.ai/features/amazon-ads?utm_source=github&utm_medium=readme&utm_campaign=amazon-ppc-benchmarks&utm_content=after-benchmarks-cta)

## License

Data and text: [CC BY 4.0](LICENSE). Credit "Luckee, amazon-ppc-benchmarks" and keep the original source links for each figure.
