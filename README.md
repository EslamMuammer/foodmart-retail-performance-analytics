# Food Mart Retail Performance Analytics

**End-to-end retail analytics project** — data cleaning (Python), dimensional data modeling, and an interactive 4-page Power BI dashboard analyzing sales, profitability, customer behavior, and product returns across a multi-region grocery retail chain.

![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=flat&logo=powerbi&logoColor=black)
![Python](https://img.shields.io/badge/Python-3.10%2B-3776AB?style=flat&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Cleaning-150458?style=flat&logo=pandas&logoColor=white)

---

## Project Summary

Food Mart is a multi-region grocery retail chain (supermarkets, deluxe supermarkets, gourmet supermarkets, mid-size and small grocery formats) operating across **North West, South West, Central West, Mexico Central, Mexico South, Mexico West, and Canada West** sales regions. Leadership needed a single source of truth to answer four recurring business questions:

1. **How is the business performing overall** — revenue, profitability, and margin trends?
2. **Which products, brands, and price points drive sales and profit** — and which underperform?
3. **Who are our customers and which stores/regions generate the most value?**
4. **Where is the business losing money to returns, and is product quality a risk?**

This project takes raw transactional CSV extracts (sales, returns, customers, products, stores, regions) through **cleaning and preparation in Python/Pandas**, builds a **star-schema data model**, and delivers a **4-page interactive Power BI dashboard** with cross-filtering, KPI cards, and drill-down visuals for each of the four business questions above.

---

## Business Objectives

| # | Objective | Dashboard Page |
|---|-----------|-----------------|
| 1 | Track top-line KPIs (units sold, revenue, gross profit, margin, customers, return rate) at a glance | `Overview` |
| 2 | Identify best/worst performing products, brands, and price-to-profit relationships | `Sales & Product Performance` |
| 3 | Segment customers (demographics, income) and compare store/regional performance | `Customer & Store Analytics` |
| 4 | Monitor returns volume, return rate, and quality issues by product/brand/store | `Returns & Quality` |

---

## Dashboard Preview

### Overview
![Overview](assets/screenshots/01_overview.png)

### Sales & Product Performance
![Sales & Product Performance](assets/screenshots/02_sales_product_performance.png)

### Customer & Store Analytics
![Customer & Store Analytics](assets/screenshots/03_customer_store_analytics.png)

### Returns & Quality
![Returns & Quality](assets/screenshots/04_returns_quality.png)

---

## Key KPIs (as of latest refresh)

| KPI | Value |
|---|---|
| Units Sold | 825K |
| Revenue (Net Sales Value) | 1.7M |
| Gross Profit | 1.1M |
| Gross Margin % | 59.7% |
| Customers | 8.84K |
| Return Rate % | 0.99% |
| Sales Value per Customer | 199.56 |
| Units per Customer | 94.26 |
| Returned Units | 8.3K |

---

## Data Model

Star schema with **2 fact tables** and **4 dimension tables**, built in Power BI's internal model after cleaning in Python:

- **Fact tables:** `fact sales`, `fact returns`
- **Dimension tables:** `dim date`, `dim products`, `dim stores`, `dim customers`

![Data Model](assets/screenshots/05_data_model_relationships.png)

Full relationship cardinalities, keys, and measure list: **[`powerbi/model_documentation.md`](powerbi/model_documentation.md)**.

---

## Tech Stack

| Layer | Tool |
|---|---|
| Data cleaning & preparation | Python (Pandas, NumPy), Jupyter Notebook |
| Storage format for cleaned data | Parquet |
| Data modeling & DAX measures | Power BI (Power Query + Tabular model) |
| Visualization / reporting | Power BI Desktop (4-page interactive report) |
| Exploratory profiling (optional) | Matplotlib, Seaborn |
