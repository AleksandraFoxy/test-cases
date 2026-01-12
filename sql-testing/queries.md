# 🛢️ SQL Practical Tasks & Queries

This document contains my solutions to various SQL exercises.

---

### 🔹 Exercise 1: Basic Selection
*Request: Display all products from the table.*

```sql
SELECT * FROM products;


🔹 Exercise 2: Filtering
Request: Find all products from Apple in the 'Phones' category.

SQL

SELECT * FROM products 
WHERE manufacturer = 'Apple' AND category = 'Phones';


🔹 Exercise 3: Aggregation
Request: Calculate total price of Samsung products.

SQL

SELECT SUM(price) AS 'SAMSUNG TOTAL PRICE' 
FROM products 
WHERE manufacturer = 'Samsung';


🔹 Exercise 4: Conditional Logic
Request: Add a custom message based on manufacturer.

SQL

SELECT 
    manufacturer, 
    category, 
    price, 
    name,
    CASE
        WHEN manufacturer = 'Apple' THEN 'This is an Apple product.'
        WHEN manufacturer = 'Samsung' THEN 'This is a Samsung product.'
        ELSE 'Unknown company.'
    END AS brand_message
FROM products;


🔹 Exercise 5: Joins
Request: Connect products with their orders.

SQL

SELECT 
    products.name, 
    orders.order_date, 
    orders.quantity
FROM products
JOIN orders ON products.id = orders.product_id;'''