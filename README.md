# retail-sales-analysis
A complete SQL-based data analysis project focused on analyzing retail sales data using MySQL. This project demonstrates SQL skills including data cleaning, data exploration, business problem solving, Common Table Expressions (CTEs), Window Functions, Aggregate Functions, and Business Insights.

---

## Project Overview

This project analyzes retail sales transactions to uncover valuable business insights using SQL.

The objective is to practice real-world SQL concepts while answering business-related questions such as:

- Sales trends
- Customer behavior
- Category performance
- Best-selling months
- Revenue analysis
- Customer segmentation
- Shift-wise order analysis

This project is ideal for beginners preparing for Data Analyst, Business Analyst, or SQL interviews.

---

## Tech Stack

- MySQL
- SQL
- MySQL Workbench

---

## Dataset

The dataset contains retail transaction details including:

| Column | Description |
|----------|-------------|
| transactions_id | Unique Transaction ID |
| sale_date | Date of Sale |
| sale_time | Time of Sale |
| customer_id | Customer ID |
| gender | Customer Gender |
| age | Customer Age |
| category | Product Category |
| quantiy | Quantity Purchased |
| price_per_unit | Price of One Unit |
| cogs | Cost of Goods Sold |
| total_sale | Total Sale Amount |

---

## Project Structure

```
spotify-data-analysis-python/
│
├── README.md
├── sales_analysis.sql
├── images/
│   ├── output/
│
└── dataset/
    └── retail_sales.csv
```

---

# Database Creation

```sql
CREATE DATABASE retail;
USE retail;
```

---

# Table Creation

```sql
CREATE TABLE sales_info(
transactions_id INT PRIMARY KEY,
sale_date DATE,
sale_time TIME,
customer_id INT,
gender VARCHAR(15),
age INT,
category VARCHAR(50),
quantiy INT,
price_per_unit FLOAT,
cogs FLOAT,
total_sale FLOAT
);
```

---

# Data Cleaning

The dataset was checked for missing values across every column.

```sql
SELECT *
FROM sales_info
WHERE
transactions_id IS NULL
OR sale_date IS NULL
OR sale_time IS NULL
OR customer_id IS NULL
OR gender IS NULL
OR age IS NULL
OR category IS NULL
OR quantiy IS NULL
OR price_per_unit IS NULL
OR cogs IS NULL
OR total_sale IS NULL;
```

Rows containing missing values were removed before analysis.

---

# Data Exploration

Performed exploratory SQL queries such as:

- Total number of sales
- Total unique customers
- Product categories
- Distinct category analysis

---

# Business Questions Solved

## 1. Sales made on a specific date

Retrieve all transactions made on **2022-11-05**.

---

## 2. Clothing sales in November 2022

Find clothing purchases with quantity greater than or equal to the specified value.

---

## 3. Total sales by category

Calculate total revenue generated from each product category.

---

## 4. Average customer age

Find the average age of customers purchasing Beauty products.

---

## 5. High-value transactions

Retrieve all transactions where total sales exceeded ₹1000.

---

## 6. Transactions by gender and category

Analyze purchasing behavior across genders and product categories.

---

## 7. Best-selling month of each year

Using:

- CTE
- Window Function (RANK())

Identify the month with the highest average sales for every year.

---

## 8. Top 5 customers

Find customers generating the highest revenue.

---

## 9. Unique customers by category

Calculate customer diversity across product categories.

---

## 10. Shift-wise Order Analysis

Categorize orders into:

- Morning
- Afternoon
- Evening

and calculate total orders in each shift.

---

# SQL Concepts Used

DDL
- CREATE DATABASE
- CREATE TABLE

DML
- DELETE

Filtering
- WHERE
- AND
- OR

Aggregate Functions
- COUNT()
- SUM()
- AVG()
- ROUND()

Date Functions
- YEAR()
- MONTH()
- MONTHNAME()
- DATE_FORMAT()

Conditional Logic
- CASE WHEN

Grouping
- GROUP BY
- ORDER BY

Window Functions
- RANK()

Common Table Expressions (CTEs)
- WITH

DISTINCT

LIMIT

---

# Key Business Insights

- Identified highest revenue-generating product categories.
- Determined the best-performing sales month each year.
- Discovered top spending customers.
- Analyzed customer demographics.
- Compared purchasing behavior across genders.
- Measured customer engagement across product categories.
- Evaluated shift-wise order distribution.

---

# Learning Outcomes

Through this project, I strengthened my understanding of:

- SQL Query Writing
- Data Cleaning
- Data Exploration
- Business Analysis
- Aggregate Functions
- Window Functions
- Common Table Expressions (CTEs)
- Real-world SQL Interview Questions
- Retail Sales Analysis

---

# Future Improvements

- Create interactive Power BI Dashboard
- Perform Python Data Analysis using Pandas
- Build visualizations using Matplotlib & Seaborn
- Predict future sales using Machine Learning

---

⭐ If you found this project helpful, don't forget to give it a Star!
