# Task 7: Basic Sales Summary using SQLite and Python

## Objective
Analyze sales data using SQL queries inside Python and visualize it using Matplotlib.

## Dataset
A simple SQLite database `sales_data.db` was created with a single table `sales` containing the following columns:
- `product`: Name of the product
- `quantity`: Number of units sold
- `price`: Price per unit

## Steps Performed
1. **Created a SQLite database** with sample sales data using `sqlite3`.
2. **Ran SQL queries** to calculate:
   - Total quantity sold per product
   - Total revenue per product (`quantity * price`)
3. **Loaded SQL results into pandas** for processing and visualization.
4. **Plotted a bar chart** using Matplotlib to show revenue per product.

## Tools Used
- Python
- SQLite (sqlite3)
- pandas
- matplotlib

## Output
The bar chart showing revenue per product is saved as `sales_chart.png`.

## How to Run
1. Open `sales_summary.ipynb` in Jupyter Notebook or VS Code.
2. Run each cell to recreate the database, run the queries, and generate the chart.
3. The chart will be saved and displayed in the notebook.

---

### Sample SQL Query Used:
```sql
SELECT 
    product, 
    SUM(quantity) AS total_qty, 
    SUM(quantity * price) AS revenue 
FROM sales 
GROUP BY product;
