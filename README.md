# Customer Shopping Behavior & Loyalty Analysis
**A Data Analytics Pipeline: Python (ETL) ➔ MySQL (Analysis) ➔ Power BI (Visualization)**

## Overview
This project focuses on identifying trends in retail consumer behavior. By analyzing **3,900+ customer records**, I built a data pipeline to investigate how demographics, loyalty programs (subscriptions), and shipping preferences impact revenue. The final output is an interactive dashboard that provides actionable insights for marketing and inventory optimization.

## Business Problem
A retail company aims to improve customer engagement and marketing strategies. The analysis solves four key questions:
1. Which demographic segments (Age/Gender) drive the most revenue?
2. Does the Subscription program lead to significantly higher spending or satisfaction?
3. How do discounts and shipping types influence the final purchase amount?
4. What are the top-performing products within each category?

## Tools & Technologies
- **Python (Jupyter):** Used for Data Cleaning (imputation), Feature Engineering (`age_group`, `frequency_mapping`), and Database Ingestion.
- **MySQL:** Used for complex data aggregation, Customer Segmentation (CTEs), and Product Ranking (Window Functions).
- **Power BI:** Developed an interactive dashboard with dynamic slicers for executive decision-making.
- **Libraries:** Pandas, SQLAlchemy, PyMySQL.

## Data Pipeline (Python ETL)
- **Data Cleaning:** Imputed missing `Review Rating` values using the **Category Median** to ensure analysis accuracy.
- **Feature Engineering:** - Created `age_group` using quartiles (Young Adult, Adult, Middle-aged, Senior).
    - Mapped qualitative frequency strings (e.g., "Fortnightly") to numerical `purchase_frequency_days`.
    - Removed redundant features (Dropped `promo_code_used` as it mirrored `discount_applied`).
- **Database Integration:** Exported the cleaned dataset directly into MySQL for a persistent relational storage layer.

## Key Findings (SQL Analysis)
- **Loyalty Segmentation:** Divided customers into 'New', 'Returning', and 'Loyal'. Found that many 'Loyal' customers (>10 purchases) remain unsubscribed.
- **Shipping Trends:** Average spending is consistent across **Standard** and **Express** shipping, suggesting customers don't increase order size for faster delivery.
- **Product Ranking:** Used `ROW_NUMBER()` to identify the top 3 items per category (e.g., Blouses lead in Clothing).

## Power BI Dashboard
The dashboard provides a high-level view of retail health and granular control via button slicers:
* **Core KPIs:** Real-time tracking of **Total Customers (3.9K)**, **Avg. Purchase ($59.76)**, and **Avg. Rating (3.75)**.
* **Subscription Insight:** Donut chart revealing **73% of customers are non-subscribers**, highlighting a major conversion opportunity.
* **Category Performance:** Comparison of **Revenue vs. Sales Volume** identifying Clothing as the primary revenue engine.
* **Demographic Trends:** Visualized revenue distribution across age groups, identifying **Young Adults** as the highest contributors.
* **Interactive Control:** Filterable by **Gender, Subscription Status, Category,** and **Shipping Type**.

<img width="889" height="490" alt="Screenshot 2026-04-29 102816" src="https://github.com/user-attachments/assets/8aacd2c2-19c9-4069-b459-060230204c5f" />

  
## Final Recommendations
1. **Targeted Loyalty Conversion:** Launch a campaign for the 73% non-subscribers who are in the 'Loyal' segment.
2. **Age-Based Bundling:** Create specific marketing bundles for **Young Adults**, the top spending demographic.
3. **Inventory Focus:** Increase stock for high-rated items like **Blouses** and **Jewelry** which show the highest customer satisfaction.

## How to Run
1. Run `Customer_Shopping_Behavior_Analysis.ipynb` to clean the data and load it to MySQL.
2. Execute the queries in `customer.sql` to generate insights.
3. Open `Customer_Behavior_Analysis.pbix` to view the visualizations.
