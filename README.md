# Love & Light House — Operations, Delivery & Customer Experience Analysis

**Excel Capstone Project | BoyCode Africa**

## Business problem
Management needs to understand delivery performance, cancellations, returns, and customer satisfaction so operational issues can be prioritised. This project uses Excel to identify service-risk areas and recommend where management should investigate first.

## Dataset
A **simulated Nigerian e-commerce dataset** supplied by BoyCode Africa for educational and portfolio use. It contains 1,812 raw order records. It must not be presented as real company or customer data.

## Results at a glance
Based on 1,800 cleaned orders:

| KPI | Result |
|---|---:|
| On-time / late delivery | 66.9% / 33.1% |
| Cancellation / return rate | 16.5% / 18.2% |
| Average delivery time | 3.26 days |
| Average customer rating | 3.63 / 5 |

## Key findings
- Ogun had the highest late-delivery rate among named regions (38.2%); Kaduna had the highest return rate (22.5%); Kano had the highest cancellation rate (19.7%).
- Express delivery averaged 2.41 days versus 4.10 for Standard, but Express had a higher late rate (40.7% versus 25.6%).
- Rated late orders averaged 3.66/5 versus 3.61/5 for rated on-time orders. This is an observed association, not evidence of causation.

## Recommendations
Investigate courier coverage and dispatch delays in Ogun; analyse the products and categories behind Kaduna returns; review stock and processing issues behind Kano cancellations; reassess Express delivery targets; and monitor delivery and customer-experience measures together.

## Data preparation and methods
The workbook preserves raw data separately, removes 12 exact duplicate rows from analysis, flags 10 missing regions, 7 missing acquisition channels, and 314 missing ratings, and recalculates late status because the source field contained 227 logic mismatches. Missing values are not invented. Analysis uses Excel Tables, formulas, validation, conditional formatting, pivot summaries, charts, KPI cards, and a regional priority matrix.

## Project files
- `workbook/` — completed Excel workbook, including raw and cleaned data, quality log, analysis, pivots, dashboard, and recommendations.
- `data/` — supplied simulated source dataset.
- `docs/metric-definitions.md` — KPI definitions and data-quality decisions.

## Limitations
The data is synthetic. Findings are descriptive or associational and cannot establish causes. Some regional summaries exclude the 10 records with missing region values; overall KPIs use all 1,800 cleaned orders. Average ratings exclude blank ratings.
