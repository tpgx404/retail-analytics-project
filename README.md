# sql-data-analytics-project
A comprehensive collection of SQL scripts for data exploration, analytics, and reporting. These scripts cover various analyses such as database exploration, measures and metrics, time-based trends, cumulative analytics, segmentation, and more.
This repository contains SQL queries designed to help data analysts and BI professionals quickly explore, segment, and analyze data within a relational database. Each script focuses on a specific analytical theme and demonstrates best practices for SQL queries.

---
# SQL Data Analytics Project

A comprehensive collection of SQL scripts for data exploration, analytics, and reporting. These scripts cover various analyses such as database exploration, measures and metrics, time-based trends, cumulative analytics, segmentation, and more.

This repository contains SQL queries designed to help data analysts and BI professionals quickly explore, segment, and analyze data within a relational database. Each script focuses on a specific analytical theme and demonstrates best practices for SQL queries.

---

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
