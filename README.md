📌 Project Overview

Designed and implemented a retail sales database in Snowflake Cloud Data Warehouse to analyze customer behavior, sales performance, and inventory management. Created a relational schema, ingested large datasets (>5,000 rows), and executed advanced SQL queries to generate business insights.

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
