# power-bi-module-end-assignment
# 📊 Power BI – Sales Data Analysis

## 📌 Project Overview

This project focuses on cleaning, transforming, and analyzing sales data using **Microsoft Power BI**. The objective is to identify regional order distribution, trending products, and profit trends through interactive visualizations and DAX calculations.

## 🎯 Objectives

- Clean and transform raw sales data.
- Handle missing values and duplicate records.
- Standardize date formats.
- Analyze order distribution across regions.
- Identify the top 5 trending products.
- Analyze profit trends over time.
- Create calculated tables, columns, and measures using DAX.

## 🛠️ Tools & Technologies

- Microsoft Power BI Desktop
- Power Query Editor
- DAX (Data Analysis Expressions)
- CSV Dataset

## 📂 Dataset Information

**Dataset:** SalesData_1000Rows_WithIssues_copy.csv

The original dataset contains 1,020 records and 11 columns.

**Columns included:**
- OrderID
- OrderDate
- CustomerName
- Region
- Product
- Category
- Quantity
- UnitPrice
- Sales
- Cost
- Profit

## 🧹 Data Cleaning & Transformation

The following data cleaning operations were performed using Power Query:

- Handled missing values in text columns.
- Replaced missing text values with "Unknown".
- Handled missing numerical values using available related columns.
- Removed duplicate rows.
- Removed records with missing OrderDate values.
- Standardized OrderDate into a consistent Date format.
- Changed numerical columns to appropriate data types.
- Verified data quality before loading.

## 📈 Data Visualizations

Three visualizations were created to analyze the sales data.

### 1. Order Distribution Across Regions
- Visualization: Pie Chart
- Shows the distribution of orders across different regions.
- Helps identify the region with the highest number of orders.

### 2. Top 5 Trending Products
- Visualization: Clustered Column Chart
- Displays the five most frequently ordered products.
- Uses the count of OrderID to identify trending products.

### 3. Profit Trend Over Time
- Visualization: Line Chart
- Displays profit trends over different years.
- Helps understand changes in profitability over time.

## 🧮 DAX Calculations

### 1. Calculated Table – EastRegionOrders

```dax
EastRegionOrders =
FILTER(
    SalesData,
    SalesData[Region] = "East"
)
```

Creates a separate table containing only orders from the East region.

### 2. Calculated Column – ProfitCostDifference

```dax
ProfitCostDifference =
SalesData[Profit] - SalesData[Cost]
```

Calculates the difference between Profit and Cost for each order.

### 3. Measure – TotalProfit

```dax
TotalProfit =
SUM(SalesData[profit])
```

Calculates the total profit earned from sales.

## 📊 Key Insights

- East region recorded the highest order count among the regions.
- Monitor was the most frequently ordered product.
- The Top 5 Products chart highlights the most popular products.
- The profit trend chart helps identify yearly profit fluctuations.
- Total profit is approximately 5.14 million in the Power BI report.

## 📁 Project Files

| File | Description |
|---|---|
| SalesData_Module_End_Evaluation.pbix | Power BI project file |
| SalesData_1000Rows_WithIssues_copy.csv | Original dataset |
| README.md | Project documentation |

## 🚀 Conclusion

This project provided practical experience in data cleaning, data transformation, data visualization, and DAX calculations using Microsoft Power BI.

It demonstrates how raw sales data can be transformed into meaningful insights to support better business decision-making.

---

**Project Type:** Module End Evaluation  
**Domain:** Data Analytics  
**Tool:** Microsoft Power BI
