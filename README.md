# 📊 Retail Analytics – Exploratory Data Analysis (EDA)

## 📌 Project Overview
This project focuses on performing Exploratory Data Analysis (EDA) on a retail data warehouse built using **SQL Server**. The goal is to extract meaningful insights from structured data using analytical SQL queries.

The dataset is organized using a **Star Schema**:
* **Fact Table:** `fact_sales`
* **Dimension Tables:** `dim_customers`, `dim_products`

This EDA layer builds on top of the data warehouse to analyze trends, performance, and business metrics.

## 🏗️ Database Setup
The project begins with initializing the database:
1.  Creates `DataWarehouseAnalytics` database.
2.  Defines `gold` schema.
3.  Creates dimension and fact tables.
4.  Loads data using `BULK INSERT`.

> [!WARNING]
> Running the initialization script will drop and recreate the database, deleting all existing data.

## 📂 Project Structure
```text
/scripts/
│
├── 00_init_database.sql
├── 01_database_exploration.sql
├── 02_dimensions_exploration.sql
├── 03_date_range_exploration.sql
├── 04_measures_exploration.sql
├── 05_magnitude_analysis.sql
├── 06_ranking_analysis.sql
├── 07_change_over_time_analysis.sql
├── 08_cumulative_analysis.sql
├── 09_performance_analysis.sql
├── 10_data_segmentation.sql
├── 11_part_to_whole_analysis.sql
├── 12_report_customers.sql
└── 13_report_products.sql

##🔍 Analysis Breakdown
1. Database Exploration
Explore tables and schema structure
Inspect metadata using INFORMATION_SCHEMA

2. Dimensions Exploration
Analyze unique values in dimension tables
Understand categorical distributions

3. Date Range Analysis
Identify time span of data
Functions used: MIN(), MAX(), DATEDIFF()

4. Measures Exploration
Compute key metrics:
Total sales
Average values
Record counts

5. Magnitude Analysis
Group data by categories (e.g., product, region)
Understand distribution using aggregations

6. Ranking Analysis
Identify:
Top-performing products
High-value customers
Functions: RANK(), DENSE_RANK(), ROW_NUMBER()

7. Change Over Time Analysis
Track trends and seasonality
Time-based grouping using:DATEPART(), DATETRUNC()

8. Cumulative Analysis
Running totals and growth tracking
Window functions:SUM() OVER(), AVG() OVER()

9. Performance Analysis
Year-over-Year (YoY) and Month-over-Month (MoM) comparisons
Functions:LAG(), CASE, window aggregates

10. Data Segmentation
Segment customers/products into groups
Example:
VIP vs Regular customers
Uses CASE and grouping logic

11. Part-to-Whole Analysis
Contribution analysis (e.g., category share of total sales)
Uses window functions for percentage calculations

12. Customer Report
Comprehensive customer-level insights:
Total orders, sales, quantity
Customer lifespan

Segmentation:
VIP / Regular / New

KPIs:
Recency
Average Order Value (AOV)
Monthly spend

13. Product Report
Detailed product performance analysis:
Total sales, orders, quantity
Unique customers
Product lifespan

Segmentation:
High / Mid / Low performers

KPIs:
Recency
Average Order Revenue (AOR)
Monthly revenue

##🛠️ Tools & Technologies
SQL Server
T-SQL
Data Warehouse (Star Schema)
Window Functions
Aggregate Functions

##📈 Key Insights Enabled
This project helps answer:
Which products generate the most revenue?
Who are the most valuable customers?
How does sales performance change over time?
What percentage does each category contribute to total sales?
Which segments drive business growth?

##🚀 How to Run

Run 00_init_database.sql to create and load data

Execute scripts sequentially (01 → 13)

Analyze outputs in SQL Server

##🎯 Learning Outcomes

Hands-on experience with data warehouse analytics

Strong understanding of SQL for data analysis

Practical use of:
Window functions

Ranking techniques

Time-series analysis

Building business-oriented insights from raw data
