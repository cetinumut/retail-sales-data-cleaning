# Retail Sales Data Cleaning - Summary Report

## Dataset

- **Source:** Retail Store Sales (Dirty) - Kaggle
- **Raw rows:** 12,575
- **Cleaned rows:** 11,971
- **Columns:** 11

## Cleaning Steps

| Step | Action |
|---|---|
| Data Types | Transaction Date converted to datetime, Discount Applied to bool |
| Duplicates | 0 duplicate rows found |
| Price Per Unit | 609 missing values recovered via Total Spent / Quantity |
| Discount Applied | Filled missing values with False |
| Item | Filled missing values with Unknown Item |
| Rows dropped | 604 rows dropped (unrecoverable missing Quantity/Total Spent) |
| Data integrity | Total Spent validated against Price Per Unit x Quantity |
| Text standardization | Category, Payment Method, Location standardized with .title() |

## Result

- **Rows removed:** 604
- **Final dataset:** 11,971 clean rows
- **Remaining missing values:** 0

## Exports

- `data/processed/retail_sales_cleaned.csv`
- `outputs/retail_sales_summary.xlsx`
- `outputs/cleaning_summary.csv`
