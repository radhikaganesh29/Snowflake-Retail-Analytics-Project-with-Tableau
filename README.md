# Snowflake-Retail-Analytics-Project-with-Tableau


This advanced analytics project demonstrates how to use **Snowflake** for scalable data warehousing and **Tableau** for insightful visualizations on a real-world global retail dataset.

## Dataset

- Source: https://www.kaggle.com/datasets/apoorvaappz/global-super-store-dataset
- Data: ~50,000 orders with fields like sales, profit, customer, product, discount, and region
- Format: CSV → Loaded into Snowflake via web UI

---

## Snowflake Workflow

### Steps:
1. Created and configured warehouses (COMPUTE_WH)
2. Loaded data into database: SALES_ANALYTICS.RAW_DATA.GLOBAL_SUPERSTORE
3. Performed SQL-based analysis:
   - Sales and profit trends (monthly)
   - Discount impact
   - RFM customer segmentation
   - Regional and product-level profitability

### RFM Logic:
Customers were scored on:
- **Recency** (days since last order)
- **Frequency** (number of orders)
- **Monetary** (total spending)

Segments generated:  
Champions, Loyal, Potential, At Risk, Churned

---

## Tableau Dashboards

Dashboards created using 6 Snowflake-exported CSVs.

### 1. **Sales Trends Dashboard**
- Line chart: Monthly Sales vs Profit (dual-axis)
- Stacked bar: Sales by Category over time
- Bar chart: Top 5 Products by Profit

<img width="752" alt="Screenshot 2025-05-01 at 4 21 53 PM" src="https://github.com/user-attachments/assets/26c710f0-225b-4240-80af-3bc7e62580e4" />


### 2. **Customer Segmentation Dashboard (RFM)**
- Segment Distribution: Customer count by RFM segment
- Heatmap: Recency vs Frequency
- Bar chart: Top 10 High-Value Customers

<img width="753" alt="Screenshot 2025-05-01 at 4 22 12 PM" src="https://github.com/user-attachments/assets/99fceff5-d018-4dde-b841-5971ad418ded" />


### 3. **Regional & Product Profitability Dashboard**
- Bar chart: Total Profit by Region
- Bar chart: Profit by Category and Sub-Category

<img width="807" alt="Screenshot 2025-05-01 at 4 23 25 PM" src="https://github.com/user-attachments/assets/aef08766-5ded-4a9d-b1b7-e20cd2aa0ae7" />

## Key Insights

### 1. Customer Behavior (RFM Analysis)
- **Champions** made up over 25% of total high-value orders.
- A significant cluster of customers with high recency scores (4–5) and low frequency scores (1–2) shows that several customers made large purchases long ago but haven’t returned, indicating high-value reactivation opportunities.
- Over **100 customers** were classified as **"Churned"**, suggesting possible revenue leakage.

### 2. Product Profitability
- Products in the **Furniture > Tables** category generated **significant losses** (over -$60K), despite decent sales volumes.
- **Technology products** (especially Copiers and Phones) accounted for the highest profits — over **$475K combined**.
- Some sub-categories like **Envelopes** and **Labels** had high volume but low profit, ideal candidates for price optimization.

### 3. Regional Insights
- The **Central** and **North** regions were the most profitable, contributing over **$500K in combined profit**.
- **Canada** and **Southeast Asia** performed the worst in terms of profit, with values below **$20K** — potentially overserved or misaligned in pricing.

### 4. Trend Analysis
- Despite consistent sales growth, **profit margins remained flat**, implying rising costs or over-discounting.


