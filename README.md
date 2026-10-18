<div align="center">

# 📊 Seasonal Sales Analytics Dashboard

**A Power BI dashboard analyzing seasonal sales trends, product performance, and regional revenue insights.**

![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
![DAX](https://img.shields.io/badge/DAX-0078D4?style=for-the-badge)
![Star Schema](https://img.shields.io/badge/Data%20Model-Star%20Schema-2E7D32?style=for-the-badge)
![Excel/CSV](https://img.shields.io/badge/Data-Excel%20%2F%20CSV-217346?style=for-the-badge&logo=microsoftexcel&logoColor=white)

</div>

---

## 📑 Table of Contents

- [Overview](#-overview)
- [Dashboard Preview](#-dashboard-preview)
- [Business Problem](#-business-problem)
- [Solution](#-solution)
- [Key Business Questions](#-key-business-questions)
- [Dashboard Features](#-dashboard-features)
- [Tools & Technologies](#-tools--technologies)
- [Dataset Description](#-dataset-description)
- [Key Metrics (DAX)](#-key-metrics-dax)
- [Repository Structure](#-repository-structure)
- [How to Use](#-how-to-use)
- [Author](#-author)

---

## 📌 Overview

The **Seasonal Sales Analytics Dashboard** is a Power BI project that analyzes sales performance across **time, products, categories, and locations**.

It delivers actionable insights into **seasonal trends, revenue growth, and overall business performance**, helping businesses understand revenue fluctuations, identify growth opportunities, and make data-driven decisions.

---

## 🖼 Dashboard Preview

![Seasonal Sales Dashboard](Seasonal%20Sales%20Dashboard.png)

> 📁 Full dataset, screenshots, and `.pbix` file: [Google Drive folder](https://drive.google.com/drive/u/0/folders/1ERnKrtUAi5apTJkIlLSla_ztrpz3L__z)

---

## 🎯 Business Problem

Retail businesses often struggle to understand how **seasonality, product demand, and regional performance** affect overall revenue. Without clear insights, organizations risk:

- ❌ Inefficient inventory planning
- ❌ Missed revenue opportunities
- ❌ Poor strategic decision-making
- ❌ Lack of visibility into growth trends

---

## ✅ Solution

This dashboard provides an **interactive, dynamic analysis** of sales data that lets users:

- ✔️ Track revenue performance over time
- ✔️ Identify seasonal patterns
- ✔️ Analyze product and category performance
- ✔️ Evaluate regional sales contributions
- ✔️ Generate automated business insights

---

## ❓ Key Business Questions

| Area | Questions Answered |
|------|--------------------|
| 📈 **Revenue Performance** | What is the total revenue? How does it compare to the previous month and previous year? What are the YoY% and MoM% growth trends? |
| 📅 **Seasonality** | How does revenue fluctuate over time? Are there seasonal peaks and dips? When are the highest and lowest sales periods? |
| 📦 **Product Performance** | Which products generate the most revenue? Which ones are underperforming? |
| 🌍 **Regional Insights** | Which locations contribute the most revenue? Are there geographical sales patterns? |
| 🛍 **Category Analysis** | Which category dominates revenue? How is revenue distributed across categories? |
| 🧠 **Business Insights** | What overall trends can be observed? Is the business growing consistently? What insights can be generated automatically? |

---

## 📊 Dashboard Features

### 📌 KPIs
- Total Revenue
- Revenue YoY%
- Revenue MoM%
- Revenue YTD
- Revenue MTD

### 📉 Visualizations
- Seasonal revenue trend (line chart)
- Revenue by category (bar chart)
- Revenue by product (bar chart)
- Revenue by location (bar chart)

### 🧾 Dynamic Narrative
- Automated summary of performance trends

### 🎛 Filters / Slicers
- Day
- Weekday
- Month
- Quarter
- Year-Month

---

## 🧰 Tools & Technologies

| Tool | Purpose |
|------|---------|
| **Power BI Desktop** | Dashboard design and visualization |
| **DAX** | Measures and time-intelligence calculations |
| **Star Schema** | Data modeling |
| **Excel / CSV** | Data source |

---

## 📂 Dataset Description

| Column Name | Description |
|-------------|-------------|
| `OrderID` | Unique order identifier |
| `OrderDate` | Date of purchase |
| `CustomerName` | Customer name |
| `ProductName` | Product purchased |
| `Category` | Product category |
| `SalesLocation` | City/location of sale |
| `Quantity` | Number of items sold |
| `UnitPrice` | Price per unit |
| `TotalRevenue` | Total sales value |

---

## 📐 Key Metrics (DAX)

```dax
Total Revenue = SUM(Sales[TotalRevenue])

Total Orders = DISTINCTCOUNT(Sales[OrderID])

Average Order Value = DIVIDE([Total Revenue], [Total Orders])

Revenue YoY% =
DIVIDE(
    [Total Revenue] - CALCULATE([Total Revenue], SAMEPERIODLASTYEAR(Date[Date])),
    CALCULATE([Total Revenue], SAMEPERIODLASTYEAR(Date[Date]))
)

Revenue MoM% =
DIVIDE(
    [Total Revenue] - CALCULATE([Total Revenue], DATEADD(Date[Date], -1, MONTH)),
    CALCULATE([Total Revenue], DATEADD(Date[Date], -1, MONTH))
)
```

---

## 🗂 Repository Structure

```
powerbi-seasonal-revenue-insights/
├── README.md                        # Project documentation
├── Seasonal Sales Dashboard.pbit    # Power BI template file
└── Seasonal Sales Dashboard.png     # Dashboard screenshot
```

---

## 🚀 How to Use

1. Download or clone this repository:
   ```bash
   git clone https://github.com/khalil24-DA/powerbi-seasonal-revenue-insights.git
   ```
2. Open **Power BI Desktop**.
3. Open `Seasonal Sales Dashboard.pbit` (File → Open).
4. When prompted, point the template to your sales data (Excel/CSV) with the columns listed in [Dataset Description](#-dataset-description).
5. Refresh the report and explore the KPIs, charts, and slicers.

---

## 👤 Author

**Khalil**
GitHub: [@khalil24-DA](https://github.com/khalil24-DA)

⭐ If you found this project useful, please consider giving it a star!
