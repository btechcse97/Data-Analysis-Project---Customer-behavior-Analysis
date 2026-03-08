# Customer Behavior Analysis

## Project Overview

This project focuses on analyzing customer purchasing behavior using data analysis techniques. The dataset includes information about customers, products, and orders to understand buying patterns and trends.

The goal of this project is to identify useful insights such as popular products, high-value customers, and overall purchase behavior that can help businesses make data-driven decisions.

## Tools & Technologies Used

* SQL
* Data Analysis Techniques
* CSV Dataset
* GitHub for project hosting

## Dataset Information

The dataset used in this project contains information about:

* Customers
* Products
* Orders
* Quantity purchased

These datasets help analyze how customers interact with products and how frequently purchases are made.

## Analysis Performed

Some important analysis performed in this project includes:

* Average quantity of products purchased
* Customer-wise total purchases
* Product performance analysis
* Identifying high-value customers

## Example SQL Queries

Average quantity of products purchased:
SELECT p.product,
AVG(o.quantity) AS avg_quantity
FROM orders o
JOIN products p
ON o.product_id = p.product_id
GROUP BY p.product;

Customer total purchases greater than a threshold:
SELECT c.name,
SUM(o.quantity) AS total_quantity
FROM orders o
JOIN customers c
ON c.customer_id = o.customer_id
GROUP BY c.name
HAVING SUM(o.quantity) > 600;

## Key Insights

* Some customers purchase significantly more products than others.
* Certain products are ordered more frequently.
* Customer behavior patterns can help businesses improve marketing strategies.


## Power BI Dashboard

![Customer Behavior Dashboard](screenshots/Dashboard.png)

## Acknowledgment

This project was developed by following tutorials from the YouTube channel - Amlan Mohanty. The tutorial provided guidance on data analysis concepts, SQL queries, and customer behavior analysis.
