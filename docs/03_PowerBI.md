# Power BI Dashboard Specification — Olist

## Page 1 — Executive Overview

KPI cards:
- Orders
- Item Sales Value
- Average Order Value
- Unique Customers
- Sellers
- Average Delivery Days
- Late Delivery Rate
- Repeat Customer Share

Visuals:
- Monthly Orders
- Monthly Item Sales Value
- Order Status Distribution

## Page 2 — Commercial & Marketplace

- Top Product Categories by Item Sales Value
- Orders by Customer State
- Top Sellers by Item Sales Value
- Payment Method by Order
- Items per Order

## Page 3 — Customer Experience

- One-Time vs Repeat Customers
- Review Score Distribution
- Average Delivery Days by Review Score

## Page 4 — Logistics

- Monthly Late Delivery Rate
- Average Delivery Days
- Late Delivery by State
- Late Delivery by Category

## KPI Definitions

Orders = distinct order IDs.

Item Sales Value = sum of `price` from Order Items. This is a transaction-value proxy, not Olist revenue.

Average Order Value = item sales value divided by distinct orders.

Average Delivery Days = average days from purchase to customer delivery for delivered orders.

Late Delivery Rate = delivered orders delivered after estimated delivery date divided by delivered orders.

Repeat Customer Share = unique customers with more than one order divided by all unique customers.

## Design Rules

Keep each page focused. Use consistent number formats, date filters, state/category/status slicers, clear titles, and short insight boxes. Avoid overcrowding.
