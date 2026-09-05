# 🛒 E-Commerce SQL Data Analysis

## 📊 Project Overview

This project analyzes an **e-commerce dataset using MySQL** to answer practical business questions related to customers, orders, products, revenue, and purchasing behavior.

The goal is to demonstrate practical SQL skills by transforming business questions into queries and extracting meaningful insights from relational data.

---

## 🗂️ Dataset

The dataset is **synthetic** and contains no real customer information.

| File              | Records | Description                      |
| ----------------- | ------: | -------------------------------- |
| `customers.csv`   |   3,000 | Customer information             |
| `products.csv`    |     300 | Product information              |
| `orders.csv`      |  15,000 | Customer orders                  |
| `order_items.csv` |  26,251 | Products purchased in each order |
| `payments.csv`    |  15,000 | Payment information              |

### Database Relationships

```text
customers
    │
    │ customer_id
    ▼
orders
    │
    ├───────────────┐
    │ order_id      │
    ▼               ▼
order_items      payments
    │
    │ product_id
    ▼
products
```

---

## 🎯 Business Questions

### Customer Analysis

* How many customers are there?
* Which cities have the most customers?
* How many orders has each customer placed?
* Which customer has placed the highest number of orders?
* Which customers have never placed an order?
* What percentage of customers have placed at least one order?
* Which customers have placed more than 5 orders?
* Who are the top 10 customers by total spending?
* Which customers have spent more than the average customer?
* Who are the top 10 customers by number of items purchased?

### Product Analysis

* What are the different product categories?
* How many products are there in each category?
* What is the average product price for each category?
* Which category has the highest number of products?
* Which products have never been ordered?
* What are the top 10 best-selling products by quantity?
* What are the top 10 products by revenue?
* Which product category generates the highest revenue?

### Order & Revenue Analysis

* How many orders are completed, cancelled, or pending?
* What is the total revenue?
* What is the average order value?
* Which month generated the highest revenue?
* Which month had the highest number of orders?
* What is the average order value for each customer?
* What is the average number of items purchased per order?
* Which cities generate the highest revenue?
* What percentage of total revenue comes from the top 10 customers?
* Which customers have purchased orders but never purchased from Electronics?

---

## 🧠 SQL Concepts Used

This project demonstrates:

* `SELECT`
* `WHERE`
* `DISTINCT`
* `ORDER BY`
* `LIMIT`
* `COUNT()`
* `SUM()`
* `AVG()`
* `ROUND()`
* `GROUP BY`
* `HAVING`
* `INNER JOIN`
* `LEFT JOIN`
* `RIGHT JOIN`
* Subqueries
* Aggregations
* Date functions
* Top-N analysis
* Revenue calculations
* Customer segmentation

---

## 💰 Key Metrics

The analysis calculates important e-commerce KPIs including:

* Total Customers
* Total Orders
* Total Revenue
* Average Order Value
* Average Items per Order
* Revenue by Customer
* Revenue by Product
* Revenue by Category
* Revenue by City
* Customer Order Frequency
* Top 10 Customer Revenue Contribution

---

## 🛠️ Tools Used

* **MySQL**
* **SQL**
* **MySQL Workbench**
* **GitHub**

---

## 📁 Project Structure

```text
sql-ecommerce-data-analysis/
│
├── README.md
├── ecommerce_analysis.sql
├── schema.md
│
└── data/
    ├── customers.csv
    ├── products.csv
    ├── orders.csv
    ├── order_items.csv
    └── payments.csv
```

---

## 🚀 How to Run the Project

### 1. Clone the repository

```bash
git clone https://github.com/YOUR-USERNAME/sql-ecommerce-data-analysis.git
```

### 2. Create a MySQL database

```sql
CREATE DATABASE ecommerce_analytics;
USE ecommerce_analytics;
```

### 3. Import the CSV files

Import the files from the `data/` directory into their corresponding MySQL tables.

### 4. Run the SQL analysis

Open:

```text
ecommerce_analysis.sql
```

Run the queries in MySQL Workbench or another MySQL client.

---

## 📌 Project Purpose

This project demonstrates how SQL can be used to move from:

```text
Raw Data
    ↓
Data Exploration
    ↓
SQL Analysis
    ↓
Business Metrics
    ↓
Business Insights
```

The project is intended as part of my **Data Analyst portfolio**.

---

## 🔮 Future Improvements

Planned improvements include:

* Building an interactive **Power BI dashboard**
* Adding visualizations for revenue and customer performance
* Performing deeper customer segmentation
* Adding advanced SQL analysis using CTEs and window functions
* Adding month-over-month revenue growth analysis

---

## 👤 Author

**Rushil Ande**

SQL Data Analysis Portfolio Project
