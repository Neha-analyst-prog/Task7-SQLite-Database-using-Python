# Basic Sales Summary using SQLite in Python

## Objective
To connect Python to a SQLite database, query sales data, and visualize the result.

## Steps
1. Created `sales_data.db` with a `sales` table.
2. Inserted sample sales records.
3. Ran an SQL query to find:
   - Total quantity sold
   - Total revenue (quantity × price)
4. Displayed results in a printed table and a bar chart.

## SQL Query
```sql
SELECT 
    product, 
    SUM(quantity) AS total_qty, 
    SUM(quantity * price) AS revenue
FROM sales
GROUP BY product;
