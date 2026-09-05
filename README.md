# 🍕 Pizza Sales Business Intelligence & Analytics

An end-to-end BI project that turns raw pizza sales transactions into actionable business insights — using **SQL** for data extraction and analysis, and **Power BI** for interactive dashboarding.

## 📌 Overview

This project simulates a real-world analytics workflow for a pizza restaurant business: load raw transactional data, run SQL queries to surface revenue and performance metrics, then build an interactive Power BI dashboard for stakeholders to explore sales trends, top products, peak hours, and customer behavior.

## 🗂️ Project Structure

```
PIZZA_SALES_REPORT/
├── README.md                  # Project documentation
├── pizza_sales.csv            # Raw sales dataset (~7.9 MB)
├── PIZZA SALES SQL.docx       # SQL queries & analysis documentation
└── POWER-BI.pbix              # Interactive Power BI dashboard
```

## 🛠️ Tech Stack

| Component      | Technology              | Purpose                                   |
|----------------|--------------------------|--------------------------------------------|
| Database       | SQL (MySQL / SQL Server) | Data extraction, transformation, aggregation |
| Visualization  | Microsoft Power BI       | Interactive dashboards & reports          |
| Data Source    | CSV                      | Raw sales transaction data                |
| Documentation  | Word (.docx)             | SQL query documentation                   |

**Key techniques:** window functions, CTEs, joins, aggregations, date functions, DAX measures, slicers, conditional formatting.

## 📊 Dataset

| Column         | Type     | Example       |
|----------------|----------|---------------|
| order_id       | INT      | ORD-001234    |
| order_date     | DATE     | 2024-03-15    |
| order_time     | TIME     | 14:30:00      |
| customer_id    | VARCHAR  | CUST-5678     |
| pizza_name     | VARCHAR  | Margherita    |
| category       | VARCHAR  | Classic, Veggie, Chicken, Supreme |
| size           | VARCHAR  | S, M, L, XL   |
| quantity       | INT      | 1–5           |
| price          | DECIMAL  | 8.99 – 24.99  |
| total_amount   | DECIMAL  | Quantity × Price |

## ⚙️ Workflow

```
Raw CSV Data
   ↓
SQL Load & Transformation
   ↓
SQL Queries (Extract Insights)
   ↓
Aggregated Results
   ↓
Power BI Connection & DAX Calculations
   ↓
Interactive Dashboard
   ↓
Stakeholder Reports & Decision Making
```

## 🔍 SQL Analysis

Key queries used to derive metrics (see `PIZZA SALES SQL.docx` for full documentation):

- **Total Revenue** — sum of `quantity × price` across all orders
- **Best-Selling Pizzas** — total units sold, ranked
- **Sales by Category** — revenue grouped by pizza category
- **Peak Order Hours** — order count and revenue by hour of day
- **Monthly/Seasonal Trends** — revenue and order count by month/year
- **Pizza Size Analysis** — frequency, quantity, revenue, and average price by size

SQL features used: aggregate functions, inner/left joins, `GROUP BY`/`HAVING`, window functions (`ROW_NUMBER`, `RANK`), date functions (`EXTRACT`, `DATEPART`, `DATE_TRUNC`), CTEs, and subqueries.

## 📈 Power BI Dashboard

**KPI Cards:** Total Revenue · Total Orders · Average Order Value · Total Pizzas Sold

**Sales Analysis:** Revenue by category (bar), Top 10 best-sellers (table), Size distribution (pie)

**Temporal Analysis:** Daily sales trend (line), Monthly revenue (column), Hourly order distribution (bar), Day-of-week performance

**Interactivity:** Date range slicer, category filter, pizza size filter, cross-filtering across pages

## 💡 Key Insights & Business Applications

- **Revenue Recognition** — peak periods, seasonal fluctuations, YoY/MoM growth
- **Product Strategy** — menu mix optimization, underperformer identification, size pricing
- **Marketing** — targeting high-spending categories, timing promotions around peak hours
- **Operations** — staff scheduling and inventory planning based on hourly demand

## 🚀 Getting Started

1. Clone/download this repository
2. Open `pizza_sales.csv` in your SQL environment (MySQL / SQL Server) and load it into a database
3. Run the queries documented in `PIZZA SALES SQL.docx`
4. Open `POWER-BI.pbix` in Power BI Desktop to explore the dashboard
5. Refresh the data source if connecting to an updated dataset

## ✅ Skills Demonstrated

Database design · SQL analysis · Business intelligence · Data visualization · Trend/statistical analysis · KPI definition · Technical documentation
