# 📊 SuperStore Time Series Analysis — Power BI Dashboard

> **DEPI Internship Project** | Power BI | Time Series Analysis | DAX

---

## 🗂️ Project Overview

This Power BI report analyzes **SuperStore sales data** with a deep focus on **Time Series Analysis**, enabling stakeholders to track performance trends across years, quarters, and months — and compare current results against prior periods.

The project was developed as part of the **Digital Egypt Pioneers Initiative (DEPI) Internship**, where the primary focus was applying time intelligence functions in DAX and building interactive, drill-enabled reports.

---

## 📁 File

| File | Description |
|------|-------------|
| `SuperStore_step_1.pbix` | Main Power BI report with all pages, visuals, and DAX measures |

---

## 📄 Report Pages

### 1. 🕐 Time Based on Sales (Yearly)
Focuses on **year-over-year** sales performance.

- **Line Chart** — Total Sales vs Last Year Sales by Year
- **Clustered Column Chart** — Side-by-side comparison of current vs prior year sales

---

### 2. 📅 Time Based on Sales 2 (Monthly)
Focuses on **month-over-month** trends and cumulative performance.

- **Area Chart** — Monthly Total Sales trend
- **Combo Chart (Line + Column)** — Total Sales vs Last Month Sales by Month
- **Pivot Table** — Year × Month breakdown with YTD column
- **Year Slicer** — Interactive filter to isolate specific years

---

### 3. 📆 Time Based on Sales 3 (Quarterly)
Focuses on **quarter-over-quarter** analysis.

- **Area Chart** — Quarterly Total Sales vs Last Quarter Sales
- **Clustered Column Chart** — Current vs prior quarter by Q
- **Pivot Table** — Year × Quarter breakdown

---

### 4. 🔖 Bookmarks Page (Category & Sub-Category)
Interactive navigation page with bookmarked views for product analysis.

- **Clustered Bar Charts** — Sales by Category and Sub-Category
- **Donut Charts** — Sales share by Category and Sub-Category
- **Line Charts** — Sales trend by Year and by Month
- **Pivot Tables** — Category Table and Sub-Category Table
- **Action Buttons (×3)** — Bookmark navigation to switch between Category and Sub-Category views

---

### 5. 🗺️ Tooltip — Category
Custom tooltip page providing city-level detail on hover.

- **Clustered Bar Chart** — Sales by City (used as a custom tooltip)

---

### 6. 🗺️ Tooltip — Sub-Category
Custom tooltip page providing segment and shipping detail on hover.

- **Clustered Bar Chart** — Sales by Customer Segment
- **Donut Chart** — Sales distribution by Ship Mode

---

### 7. 🔍 Drill Through — Months
Dedicated drill-through page accessible from monthly visuals.

- **Pivot Table** — Month-level detail with Total Sales, Last Month Sales, and MoM comparison
- **Back Button** — Returns user to the originating page

---

## 🧮 DAX Measures

All custom measures are organized in a dedicated `CALCULATIONS` table.

| Measure | Description |
|---------|-------------|
| `Total_Sales` | Sum of all sales from the FACT TABLE |
| `Last_Sales_Year` | Total sales for the same period in the prior year (using `SAMEPERIODLASTYEAR`) |
| `Last_Sales_Month` | Total sales for the previous month (using `PREVIOUSMONTH`) |
| `Last_sales_Quarter` | Total sales for the previous quarter (using `PREVIOUSQUARTER`) |
| `YTD` | Year-to-date cumulative sales (using `TOTALYTD`) |
| `Comparing_Last_Month` | Variance between current and previous month sales |
| `ComparingByQuarter` | Variance between current and previous quarter sales |

---

## 🗃️ Data Model

| Table | Role |
|-------|------|
| `FACT TABLE` | Core transactions — Sales, Orders |
| `CalenderDate` | Date dimension with Year / Month / Quarter hierarchy |
| `product category` | Product Category dimension |
| `sub category` | Product Sub-Category dimension |
| `poduct name` | Product name/Sub-Category lookup |
| `city` | City dimension |
| `customer segment dim` | Customer Segment dimension |
| `ship mode dim` | Ship Mode dimension |

---

## ✨ Key Features

- ✅ **Time Intelligence DAX** — YoY, MoM, QoQ, and YTD calculations
- ✅ **Drill-Through** — Click through monthly summaries to a detailed breakdown page
- ✅ **Custom Tooltips** — Hover on visuals to see city-level and segment-level context
- ✅ **Bookmarks & Action Buttons** — Toggle between Category and Sub-Category views without leaving the page
- ✅ **Interactive Slicers** — Filter the entire report by year
- ✅ **Combo Charts** — Overlay current vs prior period on the same axis for clear comparison

---

## 🛠️ Tools & Technologies

![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
![DAX](https://img.shields.io/badge/DAX-0078D4?style=for-the-badge&logo=microsoft&logoColor=white)
![Microsoft](https://img.shields.io/badge/Microsoft-5E5E5E?style=for-the-badge&logo=microsoft&logoColor=white)

- **Power BI Desktop** (version 2025.06)
- **DAX** for all time intelligence and comparative measures
- **SuperStore Dataset** (classic retail analytics dataset)

---

## 🎓 Context

This project was built as part of the **DEPI (Digital Egypt Pioneers Initiative) Internship Program**, with a focus on:

- Applying **Time Series Analysis** techniques in business intelligence
- Building production-grade Power BI reports using **best practices**
- Creating reusable DAX measures for period-over-period comparisons
- Designing user-friendly reports with drill-through, tooltips, and bookmarks









---

*Built with ❤️ during the DEPI Internship Program*
