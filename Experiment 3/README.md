# Importing and Connecting Business Data Sources in Power BI

##  Project Overview

This project focuses on integrating business data from multiple sources into **Microsoft Power BI** for retail sales analysis.

The project uses **MySQL and CSV data sources** to collect business data related to products, customers, stores, and sales transactions. The data was imported into Power BI, cleaned and transformed using Power Query, modeled using relationships, and presented through an interactive 3-page dashboard.

##  Objectives

* Connect Power BI with multiple business data sources.
* Import data from MySQL and CSV files.
* Create and manage a MySQL database using SQL queries.
* Clean and transform business data using Power Query.
* Create relationships between Sales, Customer, and Product tables.
* Develop an interactive Power BI dashboard.
* Analyze sales, customers, products, stores, and regional performance.
* Generate meaningful business insights for decision-making.

##  Data Sources

The project uses two main data sources:

### 1. MySQL Database

A custom MySQL database was created using SQL queries.

It contains business data related to:

* Products
* Customers
* Stores
* Sales Transactions

### 2. CSV File

Additional retail business data was stored in CSV format and imported into Power BI using **Get Data**.

## Tools & Technologies

* **Microsoft Power BI**
* **Power Query**
* **MySQL**
* **SQL**
* **CSV**
* **DAX / Power BI Data Modeling**

##  Data Import & Connection

The following steps were followed:

1. Opened Power BI Desktop.
2. Imported CSV data using **Get Data**.
3. Connected Power BI to the MySQL database.
4. Imported the required MySQL tables.
5. Verified that all required data was loaded successfully.

## Data Cleaning & Transformation

The data was prepared using **Power Query Editor**.

The following operations were performed:

* Checked data types.
* Removed unnecessary data.
* Checked and removed duplicate data.
* Cleaned the imported data.
* Applied the required transformations.

##  Data Modeling

Relationships were created between the main business tables:

```text
Sales
  │
  ├── Customer
  │
  └── Product
```

The relationships were verified as **one-to-many relationships** to support accurate analysis.

##  Dashboard Features

The final Power BI dashboard contains **3 pages**:

### 1. Sales Analysis

* Total Sales
* Total Quantity
* Total Orders
* Product-wise Sales
* Category-wise Sales
* City-wise Sales
* Monthly Sales Trends

### 2. Customer Analysis

* Customer Analysis
* Gender Analysis
* Payment Method Analysis
* Age Group Analysis
* Customer Segment Analysis

### 3. Store & Regional Analysis

* Store-wise Sales
* Mall vs Standalone Store Analysis
* Sales by City
* Orders by City
* Regional Performance

### Interactive Filters

The dashboard includes interactive slicers for:

* Month-Year
* Category

These filters allow users to explore the dashboard dynamically.

##  Dashboard Output

The final dashboard provides:

* **Total Sales Performance**
* **Customer Analysis**
* **Product-wise Sales Analysis**
* **Store-wise Sales Performance**
* **Monthly Sales Trends**
* **Interactive Filters and Slicers**

The dashboard provides management with a centralized view of business performance and supports data-driven decision-making.

##  Business Insights

The project helped identify the following business insights:

1. **Product Performance** – Identified top-selling and low-selling products.
2. **Store Performance** – Compared sales performance across different stores.
3. **Customer Analysis** – Identified high-value customers and their contribution to sales.
4. **Sales Trends** – Analyzed sales patterns across different time periods.
5. **Business Growth** – Identified opportunities to improve sales, inventory, and customer targeting.


## Conclusion

This project successfully integrated business data from **MySQL and CSV sources** into Power BI. The data was cleaned, transformed, and modeled to create meaningful retail business insights.

The final interactive dashboard provides a centralized view of **sales, customers, products, stores, and regional performance**, helping management monitor business performance and make better data-driven decisions.

tps://github.com/Bhumikaravi/Business-Analysis-Projects)
