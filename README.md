# sales-revenue-dashboard
"Cleaned and analyzed a year of sales data to find a hidden category decline -Python, Pandas, Matplotlib"
# Sales & Revenue Performance Dashboard

A data analysis project that cleans a year of raw, messy sales order data and answers the questions a sales/ops manager would actually ask: how is revenue trending, which regions and channels are performing, and is any product category losing momentum.

## Business Question

Leadership wants a monthly read on sales performance across regions, channels, and categories — and an early warning if any category is declining before it shows up in the annual numbers.

## What This Project Does

1. **Cleans raw data** — handles duplicate rows, missing values, inconsistent text formatting, and invalid entries in a 9,000+ row order-level export (see the [Data Cleaning](#data-cleaning) section below for specifics).
2. **Analyzes trends** — monthly revenue/profit, performance by region and sales channel, and quarter-over-quarter category trends.
3. **Surfaces a real insight** — Office Supplies is the only category that shrank across 2025, while every other category grew; the analysis quantifies it and flags it for follow-up.
4. **Recommends next steps** — translates the findings into concrete actions (see Section 8 of the notebook).

## Files

| File | Description |
|---|---|
| `sales_analysis.ipynb` | Main analysis notebook — cleaning, EDA, charts, findings |
| `raw_sales_data.csv` | Raw input data (intentionally messy, mirrors a real export) |
| `clean_sales_data.csv` | Output of the cleaning step |
| `chart_*.png` | Exported chart images |

## Tools Used

Python · Pandas · NumPy · Matplotlib

## Data Cleaning

The raw data was generated with deliberate, realistic data quality issues to practice handling them:

- 35 exact duplicate rows
- 60 missing `region` values, 60 missing `discount_pct` values
- Inconsistent text casing/spacing in `region` (e.g. `" north"`, `"NORTH"`, `"North "`)
- 14 invalid negative `quantity` entries

Each issue is identified and resolved with a documented reason in the notebook (e.g. duplicates dropped, missing region dropped since geography can't be inferred, missing discount filled with 0, invalid quantities dropped).

## Key Finding

Office Supplies revenue declined ~5% from H1 to H2 2025 — the only category to shrink for the year, while Electronics, Furniture, and Home Appliances all grew. The decline is concentrated in Q3-Q4, which the notebook flags as worth investigating with the category team before next year's planning cycle.

## Note on the Data

This dataset is synthetically generated for portfolio/practice purposes (not real company data), but is structured and intentionally "messy" to mirror what a real sales export looks like — the cleaning and analysis techniques are the same ones used on real data.

## Author

Vijayasubramanya H M — [LinkedIn](https://www.linkedin.com/in/vijayasubramanyahm-dataanalyst) · [GitHub](https://github.com/vijayasubramaya21)
