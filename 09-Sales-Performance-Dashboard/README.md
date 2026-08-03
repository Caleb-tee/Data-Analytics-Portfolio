#  Sales Performance Dashboard | Power BI

## Project Overview

This project analyses a retail sales dataset consisting of **four related tables**. The tables were imported into Microsoft Power BI, cleaned using Power Query, and connected through appropriate relationships to create a robust data model.

The objective was to analyse sales performance, product profitability, customer activity, and revenue trends while creating an interactive dashboard that supports business decision-making.

---

# Project Requirements

The project involved the following tasks:

- Import four related tables into Power BI.
- Clean and prepare the data.
- Create relationships between the tables.
- Build DAX measures to calculate business KPIs.
- Develop an interactive dashboard to analyse sales performance.

---

# Data Preparation

The dataset was cleaned using **Power Query** by:

- Correcting data types
- Removing duplicate records
- Handling missing values
- Standardising column formats
- Validating numerical fields
- Creating relationships between the four tables

The resulting data model ensured accurate calculations and efficient report performance.

---

# DAX Measures

The following DAX measures were created to calculate key business metrics.

## Total Orders

```DAX
Total Orders =
COUNTROWS(Sales)
```

---

## Total Revenue

```DAX
Total Revenue =
SUMX(
    Sales,
    Sales[Quantity] * RELATED(Products[Unit Price])
)
```

---

## Total Quantity Sold

```DAX
Total Quantity Sold =
SUM(Sales[Quantity])
```

---

## Total Customers

```DAX
Total Customers =
DISTINCTCOUNT(Sales[Customer ID])
```

---

## Profit Per Unit

```DAX
Profit Per Unit =
Products[Unit Price] - Products[Cost Price]
```

---

## Total Profit

```DAX
Total Profit =
SUMX(
    Sales,
    Sales[Quantity] *
    (
        RELATED(Products[Unit Price])
        -
        RELATED(Products[Cost Price])
    )
)
```

---

# Dashboard Pages

## 🏠 Home Dashboard

The Home page provides an executive overview of business performance through interactive KPI cards and summary visualisations.

### KPIs

- Total Orders
- Total Quantity Sold
- Total Revenue
- Total Profit
- Total Customers

### Visualisations

- Top Products by Revenue
- Product Categories by Revenue
- Monthly Revenue Trend
- Top Locations by Quantity Sold
- Revenue Distribution by Location

Interactive slicers were added for:

- Month
- Category
- Location

---

## 📦 Product Performance

This page focuses on product-level analysis.

### Visualisations

- Products by Revenue
- Products by Quantity Sold
- Products by Profit
- Revenue by Product Category

The analysis identifies the products contributing most to sales, revenue, and profitability.

---

## 💰 Sales Performance

This page analyses sales performance over time.

### Visualisations

- Monthly Revenue Trend
- Monthly Quantity Sold
- Monthly Profit Trend
- Profit by Category

The dashboard highlights seasonal trends and changes in business performance throughout the year.

---

# Key Insights

- The business processed approximately **2,000 customer orders**.
- More than **11,000 products** were sold.
- Total revenue exceeded **₦4 million**.
- Total profit was approximately **₦2 million**.
- Electronics generated the highest category revenue.
- Notebook Pro generated the highest revenue.
- Keyboard recorded both the highest quantity sold and the highest overall profit.
- July was the strongest-performing month for revenue and profit.
- Sales performance varied across locations, highlighting regional differences in demand.

---

# Business Recommendations

- Increase inventory for top-performing products to minimise stock shortages.
- Prioritise high-performing product categories in marketing campaigns.
- Introduce promotional activities during weaker sales months to improve demand.
- Focus on both profitability and revenue when evaluating product performance.
- Strengthen sales strategies in high-performing regions while implementing targeted campaigns in lower-performing locations.
- Use monthly sales trends to improve forecasting and inventory planning.

---

# Tools & Technologies

- Microsoft Power BI
- Power Query
- DAX
- Data Modelling
- Data Cleaning
- Interactive Dashboard Design
- Business Intelligence
- Data Visualisation

---

# Skills Demonstrated

- Data Cleaning
- Data Transformation
- Relationship Modelling
- DAX Measure Development
- KPI Design
- Interactive Reporting
- Sales Analytics
- Business Intelligence
- Data Storytelling

---

# Dashboard Preview

## 🏠 Home Dashboard

<img width="1159" height="676" alt="Home Dashboard" src="https://github.com/user-attachments/assets/9a0e0a6b-55a7-48f5-b0bb-40e6a902f18d" />


---

## 📦 Product Performance

<img width="1204" height="675" alt="Product Performance" src="https://github.com/user-attachments/assets/0fcfd48b-4dce-49da-8b38-b1434fc137ff" />


---

## 💰 Sales Performance

<img width="1201" height="675" alt="Sales Performance" src="https://github.com/user-attachments/assets/6a1c74d1-0320-438c-879f-c1d25d758685" />

