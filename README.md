# 📊 E-Commerce Profit Leak Analyzer

A Power BI dashboard that digs into an e-commerce company's order data to find **where profit is leaking** — through discounts, loss-making products, and underperforming regions/categories — using DAX measures and Power Query transformations.

## 🎯 Project Overview

Retail and e-commerce businesses often lose margin quietly: a discount band that's too generous, a sub-category that sells well but loses money on every order, a region whose returns eat the profit. This dashboard turns raw order-level data into an interactive tool for spotting exactly where that's happening.

**Built with:** Power BI Desktop · DAX · Power Query (M)

## 📑 Report Pages

### 1. Executive Overview
A high-level summary for quick decision-making:
- KPI cards: **Total Sales, Total Profit, Total Orders, Average Order Value** (each with year-over-year comparison)
- Sales & Profit trend over time (line chart, by month)
- Sales & Profit by Category (clustered column chart)
- Profit by Region (pie chart)
- Profit by Sub-Category (clustered column chart)
- Slicers: Year, Region, Sub-Category, Category

### 2. Profit Leak Detector
The diagnostic page for finding the source of margin loss:
- KPI cards: **Profit, Profit Margin %, Loss-Making Products**
- Profit by Sub-Category (bar chart) — spot which sub-categories underperform
- Profit by Discount Band (column chart) — see how discounting erodes margin
- Profit & Sales over Discount Band (line chart) — trend of the discount/profit relationship
- Detail table for row-level investigation
- Slicers: Date (Year/Quarter/Month/Day), Region, Sub-Category

## 🧮 Data Model

| Table | Role |
|---|---|
| `Orders` | Fact table — order-level sales, profit, discount, category, region data |
| `DateTable` | Date dimension table with a Year → Quarter → Month → Day hierarchy, used for time intelligence |

### Key Measures (DAX)

| Measure | Purpose |
|---|---|
| `Total sales` | Sum of order sales |
| `Total Profit` | Sum of order profit |
| `Total Orders` | Count of orders |
| `Average Order Value` | Total sales ÷ Total orders |
| `Profit Margin %` | Total profit ÷ Total sales |
| `Loss-Making Products` | Count/flag of products with negative profit |
| `Sales YoY Display` / `Sales YoY Color` | Year-over-year % change and conditional formatting for sales |
| `Profit YoY Display` / `Profit YoY Color` | Year-over-year % change and conditional formatting for profit |
| `Orders YoY Display` | Year-over-year % change in order count |
| `AOV YoY Display` / `AOV YoY Color` | Year-over-year % change and conditional formatting for average order value |

### Key Columns Used

`Category`, `Sub-Category`, `Product Name`, `Region`, `Discount`, `Discount Band`, `Sales`, `Profit`, `Year`, `Quarter`, `Month`

## 🔍 Key Insights This Dashboard Surfaces

- Which **discount bands** correlate with shrinking or negative profit margins
- Which **sub-categories / products** are consistently loss-making despite having sales volume
- How **profit trends** compare across regions and time periods
- Year-over-year movement in sales, profit, orders, and average order value at a glance

## 🛠️ How to Use

1. Clone or download this repository.
2. Open `E-Commerce-Profit-Leak-Analyzer.pbix` in [Power BI Desktop](https://powerbi.microsoft.com/desktop/) (free).
3. If prompted, point the data source to your own dataset, or explore with the data already embedded in the file.
4. Use the slicers on each page to filter by year, region, category, and sub-category.

## 📂 Repository Structure

```
E-Commerce-Profit-Leak-Analyzer/
├── E-Commerce-Profit-Leak-Analyzer.pbix   # Power BI report file
├── README.md                              # Project documentation
└── screenshots/                           # Dashboard preview images
```

## 📸 Screenshots

> Add exported screenshots of the two report pages here (Power BI Desktop → File → Export → Export to image, or a simple screen capture) and reference them below:
>
> ```markdown
> ![Executive Overview](screenshots/executive-overview.png)
> ![Profit Leak Detector](screenshots/profit-leak-detector.png)
> ```

## 👤 Author

**Aman Kumar**
Aspiring Data Analyst | SQL · Power BI · Tableau · Excel
📧 amanprajapati1882@gmail.com

---
*Part of a portfolio of data analytics projects built while completing a Data Analytics program (SQL, Power BI, Tableau, Excel, ETL, Data Visualization).*
