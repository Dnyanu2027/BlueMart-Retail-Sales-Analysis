# Retail Analytics: Sales, Profit, Product and Inventory Analysis

**Author:** Dnyaneshwari Madake
**Role:** Data Analyst
**Project type:** Portfolio project

---

## Overview

This project analyzes retail data for **BlueMart**, a chain of **50 stores across 3 UAE cities** (Dubai, Abu Dhabi and Sharjah). It covers sales from **January 2021 to October 2025** and answers common business questions about sales, profit, products, stores, channels and inventory.

The analysis is done in Python (Jupyter Notebook). The final results are presented as an interactive executive dashboard (`retail_dashboard.html`) that opens in any browser.

## Business Questions

**Main analysis**
1. How are sales changing over time?
2. Which categories generate the highest sales and profit?
3. Which products are the most profitable?
4. Which stores and cities are performing best?
5. Which sales channel contributes the most revenue?

**Ad hoc analysis**
1. Which best-selling products are at risk of running out of stock?
2. Which products are below their reorder point?
3. Which products have high sales but low profit?

## Datasets

| File | Description | Rows |
|---|---|---|
| `bm_sales.csv` | Sales transactions (date, store, product, customer, quantity, price, total value, channel, discount) | 641,843 |
| `bm_skus.csv` | Product details (name, category, subcategory, price, cost price, brand) | 200 |
| `bm_stores.csv` | Store details (name, city, store type, opening date) | 50 |
| `bm_inventory.csv` | Stock snapshot as of 31 Oct 2025 (stock on hand, reorder point, safety stock, last restock date) | 8,735 |

## Approach

1. **Data checks:** reviewed structure, missing values, duplicates and data types, and confirmed every store and product in the sales data exists in the store and product files.
2. **Data cleaning:** converted dates to date format and removed 45 duplicate sales records. Missing customer IDs (about 25% of transactions) were kept, since they do not affect sales or profit totals.
3. **Data preparation:** joined sales, product and store data into one table. Profit was calculated as `total_value - (quantity x cost_price)`.
4. **Analysis and visualization:** answered each business question using grouped summaries and charts.
5. **Inventory analysis:** the inventory file was analyzed on its own and matched to total units sold per product.
6. **Dashboard:** summarized the results in a clean executive dashboard for management.

## Key Findings

- Total sales are about **73.2M** and total profit about **21.1M** (roughly 29% of sales).
- **Electronics** produces more than half of all sales and profit.
- The most profitable product groups are **Batteries, Cables, Chargers and Mobile Accessories**.
- **Dubai** is the largest city by sales, followed by Abu Dhabi and Sharjah.
- Store sales are close together. The gap between the best and weakest store is about 5%.
- **Stores** are the largest sales channel, followed by Website, MobileApp, Amazon.ae and Noon.
- Sales follow a yearly pattern: strongest in January and February, weakest from September to November.
- No store-product record is below its reorder point. About **2,098** store-product combinations have high sales with lower stock.
- **8 products** sell well but earn lower profit, with Rice (product 1121) having the lowest profit share.

*Totals and chart-based values are rounded from the notebook's charts.*

## Tools and Skills

- **Python:** pandas, NumPy
- **Visualization:** Matplotlib, Seaborn
- **Dashboard:** HTML, Claude
- **Skills shown:** data cleaning, data merging, KPI calculation, trend analysis, inventory analysis, business storytelling

## Project Structure

```
.
├── Retail.ipynb              # Full analysis notebook
├── retail_dashboard.html     # Executive dashboard (open in a browser)
├── data/
│   ├── bm_sales.csv
│   ├── bm_skus.csv
│   ├── bm_stores.csv
│   └── bm_inventory.csv
└── README.md
```

## How to Run

1. Clone or download this repository.
2. Install the required libraries:
   ```bash
   pip install pandas numpy matplotlib seaborn jupyter
   ```
3. Update the CSV file paths in the first cells of `Retail.ipynb` to point to your `data/` folder.
4. Run the notebook:
   ```bash
   jupyter notebook Retail.ipynb
   ```
5. To view the dashboard, open `retail_dashboard.html` in any web browser.

## Author

**Dnyaneshwari Madake**
Data Analyst

- LinkedIn: www.linkedin.com/in/dnyaneshwari-madake
- GitHub: 
- Email: dnyaneshwarimadake4@gmail.com
