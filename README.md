# Customer Shopping Behavior Analysis
Data Analytics project showcasing customer shopping behavior analysis.
An End-to-End Data Pipeline: Python (ETL) ➔ MySQL (Business Logic) ➔ Power BI (Interactive Dashboard)

# Project Overview
This project addresses a critical business need: understanding consumer shopping patterns to optimize marketing and inventory strategies. I built a full data pipeline to analyze **3,900+ customer records**, focusing on how demographics, subscription status, and shipping methods impact a **$233k+ revenue stream.**

# Business Problem
The management team needed to identify high-value customer segments and determine if current loyalty programs (Subscriptions) and incentives (Discounts) were effectively driving revenue and customer satisfaction.

# Tools & Technologies
- **Python (Jupyter):** Performed data cleaning, handled missing review ratings via median imputation, and engineered new features like `age_group` and `purchase_frequency_days`.
- **MySQL:** Created a relational database to execute complex business queries, including window functions for product ranking and CTEs for customer segmentation.
- **Power BI:** Developed an interactive executive dashboard with dynamic slicers for Gender, Category, and Subscription Status.

# Key Data Engineering (Python)
I utilized Python to transform raw data into "Analysis-Ready" formats:
- **Missing Value Handling:** Imputed `Review Rating` gaps using category-based medians.
- **Feature Engineering:** Segmented `Age` into four quartiles (`Young Adult` to `Senior`) to identify generational spending habits.
- **Database Integration:** Automated the transfer of cleaned DataFrames into MySQL using `SQLAlchemy`.

# Strategic Business Insights (MYSQL)
- **The Loyalty Gap:** Only **27%** of customers are subscribed. However, repeat buyers (>5 purchases) show a significant volume in the non-subscriber pool, indicating a massive opportunity for conversion marketing.
- **Category Leadership:** **Clothing** is the primary revenue driver, contributing over **$104k** to total sales.
- **Discount Efficiency:** I identified the top 5 products (like Blouses and Sweaters) with the highest discount-to-purchase ratios to evaluate margin health.
- **Logistics:** Average purchase amounts are nearly identical between **Standard** and **Express** shipping, suggesting customers are not currently incentivized to spend more for faster delivery.

# Business Recommendations
1. **Targeted Conversion:** Launch a "Loyalty Upgrade" campaign specifically for the "Returning" and "Loyal" customer segments who are not yet subscribers.
2. **Age-Based Bundling:** Since **Young Adults** are the top spenders, create "Summer/Winter Bundles" for the Clothing category tailored to this demographic.
3. **Review-Driven Stocking:** Increase inventory for the top 5 highest-rated products to capitalize on high customer satisfaction.
