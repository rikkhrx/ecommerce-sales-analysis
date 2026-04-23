# ecommerce-sales-analysis
SQL-based analysis of e-commerce data to extract business insights
## Top 5 Most Ordered Products


---

## 💻 Example (copy paste kar)

### 🔹 Top 5 Products section ke niche:
```md
### SQL Query
```sql
SELECT 
    p.product_name,
    COUNT(od.quantity) AS total_orders
FROM products p
JOIN order_details od 
    ON p.product_id = od.product_id
GROUP BY p.product_name
ORDER BY total_orders DESC
LIMIT 5;

![Top 5 Products](top_5_products.png)

## Total Revenue from Delivered Orders

![Total Revenue](delivered_orders_revenue.png)

## Order Status Analysis

This analysis shows the distribution of order statuses.  
We can observe that most orders are successfully delivered, while a portion gets cancelled, indicating potential areas for improvement in order fulfillment.

![Order Status](order_status_analysis.png)

## Revenue by Product Category

This analysis shows which product categories generate the most revenue.  
Electronics contributes the highest revenue, indicating strong demand in this category.

![Category Revenue](category_revenue_analysis.png)

## Order Cancellation Rate

This analysis calculates the percentage of cancelled orders.  
A high cancellation rate (45%) indicates potential issues in order processing, delivery, or customer satisfaction.

![Cancellation Rate](cancel_rate_analysis.png)
