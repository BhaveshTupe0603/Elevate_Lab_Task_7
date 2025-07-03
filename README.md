# 🛒 Task 7: Basic Sales Summary using SQLite and Python

## 📌 Objective

The goal of this task is to analyze simple sales data using **SQLite** and **Python**, extract meaningful summaries such as total quantity sold and revenue per product, and visualize the results using **Matplotlib**. This project demonstrates how to integrate SQL with Python for quick data analytics and reporting.

---

## 🧰 Tools & Technologies

- **Python 3**
- **SQLite3** (built-in with Python)
- **Pandas** for data handling
- **Matplotlib** for data visualization
- **Jupyter Notebook** or `.py` script

---

## 📂 Dataset

We use a custom SQLite database `sales_data.db` containing a single table:

### Table: `sales`
| Column   | Type    | Description              |
|----------|---------|--------------------------|
| id       | INTEGER | Auto-increment primary key |
| product  | TEXT    | Product name             |
| quantity | INTEGER | Quantity sold            |
| price    | REAL    | Unit price of the product |

Sample data is inserted manually for demonstration.

---

## 🚀 How to Run

1. **Create the database and insert sample data**
    - Run the setup script to create `sales_data.db` and populate the `sales` table.

2. **Execute the analysis script**
    - Use Python to connect to the database, run SQL queries, and load results into a Pandas DataFrame.

3. **Visualize results**
    - Generate a bar chart showing revenue by product using Matplotlib.
    - Optionally save the chart as `sales_chart.png`.

---

## 📊 Output

- **Printed sales summary table**: Showing product, total quantity sold, and total revenue.
- **Bar chart**: A visual representation of revenue by product.

---

## 🧠 Insights

- Efficiently combined **SQL + Python** to perform sales aggregation.
- Visualized revenue distribution across products using a simple bar chart.
- Learned to work with **SQLite databases in Python projects**.
![sales_chart](https://github.com/user-attachments/assets/042861d7-636a-41aa-8628-6afcacc1d57b)

---

## 📝 Sample SQL Query Used

```sql
SELECT product, 
       SUM(quantity) AS total_qty, 
       ROUND(SUM(quantity * price), 2) AS revenue
FROM sales
GROUP BY product;
