# SQL Analytics Portfolio (MySQL)

This repository contains SQL queries for analytics use-cases such as KPI reporting, trend analysis, profitability, and top-N insights.

## Skills Demonstrated
- SQL fundamentals: SELECT, WHERE, ORDER BY
- Aggregations: GROUP BY, HAVING
- Joins: INNER JOIN, LEFT JOIN
- Date analysis: monthly trends using DATE_FORMAT
- KPI reporting: Revenue, COGS, Gross Profit, Profit Margin %
- Advanced SQL (MySQL 8+): CTEs (WITH), Window functions (LAG, SUM OVER, DENSE_RANK)

## Expected Tables (generic)
These queries assume business tables like:
- `sales` (sale_date, product_id, customer_id, units_sold, unit_price, unit_cost, discount_pct)
- `products` (product_id, product_name, category)
- `customers` (customer_id, customer_name, region)
- `purchases` (purchase_date, supplier_id, material_name, quantity, unit_cost)
- `suppliers` (supplier_id, supplier_name)
- `production` (production_date, product_id, units_produced, unit_production_cost)
- `expenses` (expense_date, expense_type, amount)

> If your real database has different column names, rename them in `queries.sql`.

## KPIs Used
- Revenue = SUM(units_sold * unit_price * (1 - discount_pct/100))
- COGS = SUM(units_sold * unit_cost)
- Gross Profit = Revenue - COGS
- Profit Margin % = (Gross Profit / Revenue) * 100

## How to Use
1. Open `queries.sql`
2. Run queries in MySQL Workbench / CLI
3. Use outputs for reporting/dashboard datasets

## Notes
- Queries are written for MySQL (Window functions require MySQL 8+).
- Real client data should be anonymized before sharing publicly.
