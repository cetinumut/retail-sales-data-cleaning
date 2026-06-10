# Retail Sales Data Cleaning & Analysis

End-to-end data cleaning and analysis project on a dirty retail sales dataset using Python and Pandas.

**Dataset:** [Retail Store Sales (Dirty) - Kaggle](https://www.kaggle.com/datasets/ahmedmohamed2003/retail-store-sales-dirty-for-data-cleaning)
**Rows:** 12,575 raw -> 11,971 cleaned
**Columns:** 11

---

## What This Project Does

1. Loads a real-world dirty retail dataset with missing values, wrong data types, and inconsistent text
2. Cleans the data systematically using Pandas
3. Validates data integrity (Total Spent = Price Per Unit x Quantity)
4. Analyzes cleaned data and produces business visualizations
5. Exports the cleaned dataset to CSV and Excel

---

## Cleaning Steps

| Step | Action | Result |
|------|--------|--------|
| Fix data types | Transaction Date to datetime, Discount Applied to bool | Correct types for analysis |
| Remove duplicates | Checked full rows and Transaction IDs | No duplicates found |
| Recover missing values | Price Per Unit derived from Total Spent / Quantity | 609 values recovered |
| Fill missing text | Item filled as Unknown Item, Discount Applied filled as False | 1,213 + 4,199 values filled |
| Drop unrecoverable rows | Rows where Quantity and Total Spent were both missing | 604 rows removed |
| Integrity check | Validated Total Spent == Price Per Unit x Quantity | 0 mismatches |
| Standardize text | strip and title case on Category, Payment Method, Location | Consistent casing |

**Key decision:** Quantity and Total Spent missing values could not be recovered because they were missing together in the same rows. No formula could reconstruct them. Only Price Per Unit was recoverable.

---

## Analysis & Visualizations

- Revenue by Category (bar chart)
- Top 10 Products by Revenue (horizontal bar chart)
- Monthly Sales Trend (line chart with area fill)

Charts are saved to .

---

## Project Structure



---

## Results

| Metric | Value |
|--------|-------|
| Raw rows | 12,575 |
| Cleaned rows | 11,971 |
| Rows dropped | 604 |
| Price Per Unit recovered | 609 |
| Discount Applied filled | 4,199 |
| Item filled (Unknown Item) | 1,213 |
| Remaining missing values | 0 |

---

## Technologies

- Python 3
- Pandas
- NumPy
- Matplotlib
- Seaborn
- OpenPyXL
- Jupyter Notebook

---

## How to Run

```bash
pip install -r requirements.txt
jupyter notebook notebooks/retail_sales_data_cleaning_analysis.ipynb
```

The notebook automatically sets the working directory to the project root, so it runs correctly regardless of where Jupyter was launched from.
