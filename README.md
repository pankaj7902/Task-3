SQL Basics – Task 3 (Data Analyst Internship)

Objective

The goal of this task is to practice basic SQL operations such as:

Data filtering
Sorting
Aggregations
Grouping
Creating summary reports

Tools Used

MySQL
MySQL Workbench
Dataset: Superstore(CSV)

Files Included

queries_task3.sql – Contains all SQL queries written for the task
sales_summary.csv – Exported result of summary queries
README.md – Explanation of the task and queries
[sales_summary.csv](https://github.com/user-attachments/files/24716268/sales_summary.csv)
[queries_task3.sql](https://github.com/user-attachments/files/24716261/queries_task3.sql)

SQL Queries Explained

1. View Dataset

sql
SELECT * FROM sales;
Used to inspect the data after importing the CSV file.

2. Count Records

sql
SELECT COUNT(*) FROM sales;
Used to verify that the number of records matches the CSV file.

3. Filtering Data (WHERE)

sql
SELECT * FROM sales WHERE category = 'Technology';
Filters rows where the category is Technology.

4. Sorting Data (ORDER BY)

sql
SELECT * FROM sales ORDER BY sales DESC;
Displays products with highest sales first.

5. Aggregation with GROUP BY

sql
SELECT category, SUM(sales) FROM sales GROUP BY category;
Calculates total sales for each category.

6. Using HAVING

sql
SELECT category, SUM(sales)
FROM sales
GROUP BY category
HAVING SUM(sales) > 100000;
Filters grouped results to show only high-performing categories.

7. BETWEEN and LIKE

sql
SELECT * FROM sales WHERE order_date BETWEEN '2023-01-01' AND '2023-01-31';
SELECT * FROM sales WHERE customer_name LIKE '%John%';0
Used for date-based and pattern-based filtering.

8. Top Customers

sql
SELECT customer_name, SUM(sales)
FROM sales
GROUP BY customer_name
ORDER BY SUM(sales) DESC
LIMIT 5;
Finds top 5 customers by total spending.

Outcome

Learned how to write clean SQL queries
Understood filtering, sorting, grouping, and aggregation
Gained confidence for SQL interview questions

Author
Pankaj Parmar
