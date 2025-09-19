📌 Project: Retail Sales Analytics using Snowflake SQL

Description:
Designed and implemented a retail sales database in Snowflake Cloud Data Warehouse to analyze customer behavior, sales performance, and inventory management. Created a relational schema, ingested large datasets (>5,000 rows), and executed advanced SQL queries to generate business insights.

Key Contributions:

Created a retail sales schema with 6 tables (Customers, Orders, OrderDetails, Products, Categories, Suppliers).

Ingested structured datasets (>5,000 rows) into Snowflake using Web UI drag-and-drop and handled data quality issues (headers, nulls).

Wrote optimized SQL queries to extract KPIs such as:

Top-selling products and categories

Monthly revenue trends

Customer lifetime value (CLV) and top spenders

Low-stock inventory alerts

Applied joins, aggregations, and date functions to answer complex business questions.

Delivered insights useful for sales forecasting, customer segmentation, and inventory planning.

Tech Stack:
Snowflake, SQL, CSV Data

👉 This way, you can show it as a Cloud SQL Analytics Project.
When you fix your Snowflake → Power BI connection, you can extend it to “Retail Sales Dashboard using Power BI & Snowflake”.

Would you like me to also prepare a GitHub README template for this project (like you had for Flipkart/Blinkit), so you can upload it and showcase it properly?

You said:
yes
ChatGPT said:

Great 🚀 Dinesh! Here’s a GitHub README template you can directly use for your Snowflake SQL Retail Sales Project.

🛒 Retail Sales Analytics – Snowflake SQL Project
📌 Project Overview

This project demonstrates the use of Snowflake Cloud Data Warehouse for building and analyzing a Retail Sales Database.
The objective is to perform end-to-end data analytics on retail transactions, customer purchases, and inventory to derive meaningful business insights.

📂 Dataset

Size: 5,000+ rows

Tables Created:

Customers – Customer details

Orders – Order transactions

OrderDetails – Line items for each order

Products – Product catalog

Categories – Product categories

Suppliers – Supplier details

🛠️ Tech Stack

Snowflake – Cloud Data Warehouse

SQL – Data Querying & Analytics

CSV – Data ingestion

⚙️ Process

Database & Schema Setup

Created database: RetailSalesDB

Created schema: RetailSchema

Data Loading

Loaded CSV files using Snowflake Web UI (drag-and-drop)

Fixed header row issue by applying proper file format options

SQL Analytics & Insights

Wrote queries for:

Top-selling products & categories

Monthly revenue trends

Customer spending analysis (Top 5 customers)

Low-stock product alerts

Category-wise sales performance

📊 Sample Queries
🔹 Top 10 Best-Selling Products
SELECT p.ProductName, SUM(od.Quantity) AS TotalSold
FROM OrderDetails od
JOIN Products p ON od.ProductID = p.ProductID
GROUP BY p.ProductName
ORDER BY TotalSold DESC
LIMIT 10;

🔹 Monthly Sales Revenue
SELECT DATE_TRUNC('month', o.OrderDate) AS Month,
       SUM(od.TotalAmount) AS Revenue
FROM Orders o
JOIN OrderDetails od ON o.OrderID = od.OrderID
GROUP BY Month
ORDER BY Month;

🎯 Key Learnings

Data ingestion and management in Snowflake Cloud DW

Schema design and relational modeling

Writing advanced SQL queries for analytics

Generating business insights for sales, customers, and inventory
