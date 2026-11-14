# IndiaKart-Data-Analytics-Project

Python and Power BI analysis of a simulated Indian e-commerce marketplace: data quality checks, exploratory analysis, 10 business KPIs, a 5-page dashboard and a management report.

**Business question:** Where does IndiaKart make its money, and where is it losing revenue to cancellations, returns, payment failures and stockouts?

## Key findings

| KPI | Result | Target |
| --- | --- | --- |
| Gross merchandise value (GMV) | **₹31.47 Cr** (₹3,147,385,545) | n/a |
| Net revenue (delivered orders) | ₹20.54 Cr (₹2,053,858,612) | n/a |
| Average order value (AOV) | ₹63,198 | n/a |
| Cancellation rate | **11.99%** | below 10% |
| Return rate | **30.77%** | below 8% |
| Payment failure rate | 3.50% | below 2% |
| Inventory fill rate | 92.20% | above 95% |
| Top category revenue share | **Electronics 57.41%**, then Sports & Fitness 17.38% | no category above 60% |
| Customer lifetime value | Premium ₹532,735 vs Regular ₹361,871 (about 1.5x) | about 3x |

Revenue is concentrated in Electronics, and cancellations, returns, payment failures and stock availability all miss their targets.

## Project phases

| Phase | What I did | File |
| --- | --- | --- |
| 1. Data quality checks | Checked table shapes, missing values, duplicates, date logic and referential integrity across 8 tables. Found a 3.5% payment failure rate, no orphan returns and 457 customers who have never ordered. | `Phase1_DataCleaning_Mayuri_Maneguldhe.ipynb` |
| 2. Exploratory data analysis | 10 charts: monthly orders and GMV, category revenue share, order status, customers by state, segments, payment methods, age, return reasons and AOV by segment. | `Phase2_EDA_Mayuri_Maneguldhe.ipynb` |
| 3. KPI calculation | 10 KPIs with documented formulas, plus a cohort analysis of customer order activity. | `Phase3_KPIs_Mayuri_Maneguldhe.ipynb` |
| 4. Dashboard and report | 5-page Power BI dashboard (Revenue Overview, Category Performance, Customer Insights, Operations, Inventory Alert) with 12 DAX measures, and a management report with risks and recommendations. | `Phase4_IndiaKart_Mayuri_Maneguldhe.pbix`, `Phase4_Report_Mayuri_Maneguldhe.docx` |

## Dashboard

[View the dashboard](Phase4_IndiaKart_Mayuri_Maneguldhe.pbix)

## Data

The dataset is simulated: 50,000 orders and 10,000 customers across 8 tables (customers, orders, order_items, payments, products, inventory, returns, suppliers), stored as sheets in `data/All_CSV_Converted_Into_Sheets.xlsx`.

Notes on the data and metrics:
- **Return rate** is 10,000 return records divided by 32,499 delivered orders.
- **Month-over-month GMV growth** for July 2023 (+370.77%) and the earliest cohort values above 100% come from the partial first month of data (June 2023), so read them as a data artefact, not real growth.
- Customer lifetime value is the average `total_spent` per segment.

## How to run

1. Install the packages: `pip install -r requirements.txt`
2. Keep the Excel file in the `data/` folder.
3. Run the notebooks in order, Phase 1 to Phase 3, with Jupyter or VS Code.
4. Open the `.pbix` file in Power BI Desktop to explore the dashboard.

## Tech stack

Python (pandas, NumPy, Matplotlib, Seaborn) · Excel · Power BI (DAX) · Jupyter Notebook

## Author

Mayuri Maneguldhe · [GitHub](https://github.com/mayurimaneguldhe-a11y) · [LinkedIn](https://www.linkedin.com/in/mayuri-maneguldhe-558621309)
