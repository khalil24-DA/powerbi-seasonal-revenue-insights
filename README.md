# powerbi-seasonal-revenue-insights
This project presents a Power BI dashboard analyzing seasonal sales trends, product performance, and regional revenue insights. It helps businesses understand revenue fluctuations, identify growth opportunities, and make data-driven decisions.

# 📊 Seasonal Sales Analytics Dashboard

## 📌 Overview
The **Seasonal Sales Analytics Dashboard** is a Power BI project designed to analyze sales performance across time, products, categories, and locations.  

It provides actionable insights into **seasonal trends, revenue growth, and business performance**, helping stakeholders make data-driven decisions.

---

## 🎯 Business Problem
Retail businesses often face challenges in understanding how **seasonality, product demand, and regional performance** impact overall revenue.

Without clear insights, organizations may struggle with:
- Inefficient inventory planning  
- Missed revenue opportunities  
- Poor strategic decision-making  
- Lack of visibility into growth trends  

---

## ✅ Solution
This dashboard provides an **interactive and dynamic analysis** of sales data, enabling users to:

- Track revenue performance over time  
- Identify seasonal patterns  
- Analyze product and category performance  
- Evaluate regional sales contributions  
- Generate automated business insights  

---

## ❓ Key Business Questions

### 📈 Revenue Performance
- What is the total revenue?
- How does revenue compare to previous month and previous year?
- What are the **YoY%** and **MoM%** growth trends?

### 📅 Seasonality Analysis
- How does revenue fluctuate over time?
- Are there seasonal peaks and dips?
- When are the highest and lowest sales periods?

### 📦 Product Performance
- Which products generate the most revenue?
- Which products are underperforming?

### 🌍 Regional Insights
- Which locations contribute the most revenue?
- Are there geographical sales patterns?

### 🛍 Category Analysis
- Which category dominates revenue?
- What is the distribution of revenue across categories?

### 🧠 Business Insights
- What overall trends can be observed?
- Is the business growing consistently?
- What insights can be automatically generated?

---

## 📊 Dashboard Features

- 📌 **KPIs**
  - Total Revenue
  - Revenue YoY%
  - Revenue MoM%
  - Revenue YTD
  - Revenue MTD

- 📉 **Visualizations**
  - Seasonal revenue trend (line chart)
  - Revenue by category (bar chart)
  - Revenue by product (bar chart)
  - Revenue by location (bar chart)

- 🧾 **Dynamic Narrative**
  - Automated summary of performance trends

- 🎛 **Filters / Slicers**
  - Day
  - Weekday
  - Month
  - Quarter
  - Year-Month

---

## 🖼 Dashboard Preview

[Dataset & Dashboard Screenshot & pbix files](https://drive.google.com/drive/u/0/folders/1ERnKrtUAi5apTJkIlLSla_ztrpz3L__z)

## 🧰 Tools & Technologies

- **Power BI Desktop**
- **DAX (Data Analysis Expressions)**
- **Data Modeling (Star Schema)**
- **Excel / CSV (Data Source)**

---

## 📂 Dataset Description

The dataset includes the following fields:

| Column Name     | Description |
|----------------|------------|
| OrderID        | Unique order identifier |
| OrderDate      | Date of purchase |
| CustomerName   | Customer name |
| ProductName    | Product purchased |
| Category       | Product category |
| SalesLocation  | City/location of sale |
| Quantity       | Number of items sold |
| UnitPrice      | Price per unit |
| TotalRevenue   | Total sales value |

---

## 📐 Key Metrics (DAX)

```DAX
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
