# Superstore Business Performance Analysis Using Power BI

##  Project Overview

This project focuses on analyzing the **sales and profitability performance of a retail organization** using Microsoft Power BI.

The **Sample Superstore dataset** was imported, cleaned, transformed, and analyzed using Power Query and DAX. An interactive Power BI dashboard was developed to understand sales, profit, customers, products, regions, segments, and discount-related performance.

## Objectives

* Analyze retail sales and profit performance.
* Import and prepare the Sample Superstore dataset.
* Clean and transform data using Power Query.
* Create a Date Table using DAX.
* Develop important DAX measures and KPIs.
* Analyze products, categories, sub-categories, regions, and customer segments.
* Identify sales and profitability trends.
* Build an interactive Power BI dashboard.
* Generate useful business insights for decision-making.

## Dataset

The **Sample Superstore** dataset was obtained from Kaggle.

* **File:** `SampleSuperstore.csv`
* **Records:** 9,994
* **Fields:** 13

### Important Fields

* Ship Mode
* Segment
* Region
* Category
* Sub-Category
* Sales
* Quantity
* Discount
* Profit
* Order Date
* Order ID
* Customer ID

## 🛠️ Tools & Technologies

* **Microsoft Power BI**
* **Power Query**
* **DAX**
* **CSV**
* **Kaggle Dataset**

## 🔄 Data Preparation

The dataset was prepared using **Power Query**.

The following steps were performed:

* Verified and corrected data types.
* Set Sales, Profit, and Discount as Decimal Number.
* Set Quantity and Postal Code as Whole Number.
* Checked and removed duplicate records.
* Checked important fields for missing values.
* Organized query and column names for easier analysis.

##  Data Modeling

A separate **Date Table** was created using the DAX `CALENDAR()` function.

The Date Table contains:

* Year
* Month
* Month Name
* Quarter

The Date Table was marked as an official Date Table and connected with the `Order Date` field of the Superstore table.

##  DAX Measures

The following measures were created:

```DAX
Total Sales = SUM('Superstore'[Sales])
```

```DAX
Total Profit = SUM('Superstore'[Profit])
```

```DAX
Total Orders = DISTINCTCOUNT('Superstore'[Order ID])
```

```DAX
Total Customers = DISTINCTCOUNT('Superstore'[Customer ID])
```

```DAX
Total Quantity = SUM('Superstore'[Quantity])
```

```DAX
Profit Margin % = DIVIDE([Total Profit], [Total Sales], 0)
```

```DAX
Average Order Value = DIVIDE([Total Sales], [Total Orders], 0)
```

```DAX
Average Discount = AVERAGE('Superstore'[Discount])
```

These measures were used to create KPI cards, charts, tables, and other dashboard visualizations.

## 📈 Dashboard Features

The Power BI dashboard includes:

### KPI Analysis

* Total Sales
* Total Profit
* Total Orders
* Total Customers
* Total Quantity
* Profit Margin

### Sales Analysis

* Sales by Category
* Sales by Sub-Category
* Sales by Region
* Monthly/Yearly Sales Trend

### Product Analysis

* Top 10 Products
* Highest-selling products

### Profit Analysis

* Profit by Category
* Profit by Region
* Sales vs Profit
* Discount vs Profit

### Customer Analysis

* Sales by Customer Segment
* Consumer
* Corporate
* Home Office

### Interactive Filters

The dashboard includes slicers for:

* Year
* Region
* Category
* Segment
* Order Date

## Key Business Insights

The analysis provides the following insights:

1. **Technology** is one of the major contributors to overall sales.
2. Sales performance varies across the four regions, helping identify strong and weak markets.
3. The **Top 10 Products** visualization identifies products contributing significantly to revenue.
4. High sales do not always result in high profit.
5. Monthly and yearly trends help identify periods of increasing or decreasing sales.
6. Customer segments contribute differently to overall sales.
7. Discount vs Profit analysis helps identify the effect of discounts on profitability.
8. Category and sub-category analysis can help identify areas requiring better pricing or business strategies.



## 🎓 Learning Outcomes

Through this project, I learned how to:

* Create DAX measures for business analysis.
* Calculate important business KPIs.
* Use `SUM()`, `DISTINCTCOUNT()`, `AVERAGE()`, and `DIVIDE()`.
* Calculate Profit Margin, Average Order Value, and Average Discount.
* Analyze sales and profitability using DAX measures.
* Create interactive charts and KPI cards.
* Use slicers for interactive analysis.
* Identify business trends and performance indicators.
* Build an interactive Power BI dashboard.
* Convert raw sales data into meaningful business insights.

##Conclusion

The Power BI dashboard provides a clear overview of **Superstore sales and profitability performance**. The combination of KPI cards, charts, scatter plots, filters, and product analysis makes it easier to identify strong categories, profitable regions, top-performing products, sales trends, and the effect of discounts on profit.

The project demonstrates how **Power BI, Power Query, and DAX** can be used to transform raw retail data into meaningful insights and support data-driven business decisions.




[Business Analysis Projects](https://github.com/Bhumikaravi/Business-Analysis-Projects)
