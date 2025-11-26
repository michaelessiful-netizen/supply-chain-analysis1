# supply-chain-analysis1
# 📦 Sylar Supply Chain Data Analysis -- A make-believe comapny I created for the purpose of analysis

## 🎯 Project Overview
This project performs a comprehensive **Data Analysis** of a large-scale Supply Chain dataset (sourced from Kaggle) using **MySQL**. The goal was to transform raw order and logistics data into actionable business intelligence across three critical areas: **Demand & Sales**, **Logistics & Efficiency**, and **Financial Performance**.

### Key Deliverables
* **Data Preparation:** Initial schema creation, handling data type issues (especially `DATETIME` and `DECIMAL` precision), and robust ETL process using `LOAD DATA LOCAL INFILE` with temporary variables and character set conversion (`utf8mb4`).
* **Feature Engineering:** Created key metrics like `Delivery_Lead_Time_Days`, `Delivery_Time_Variance`, `Order_Item_Profit_Actual`, and temporal columns (`Order_Month`, `Order_Hour`).
* **Deep Dive Analysis:** Executed over 14 analytical queries to uncover trends, identify bottlenecks, and measure profitability.

## 🛠️ Technology Stack
* **Database:** MySQL (Primary tool for cleaning, transformation, and analysis)
* **Data Source:** Supply Chain Dataset (Kaggle)

## 📊 Core Analysis & Insights
The analysis focused on answering key business questions, resulting in the following insights:

| Focus Area | Key Metrics Analyzed | Sample Insight |
| :--- | :--- | :--- |
| **Demand & Sales** | Total Units Sold by Time, Top Product Categories, Order Status Volume, AOV by Customer Segment. | Identified peak ordering times (seasonality/hour) and the **Top 10 Revenue-Generating Product Categories** for inventory optimization. |
| **Logistics & Efficiency** | On-Time Delivery Rate (OTD), Delivery Lead Time by Region, Delivery Time Variance. | Measured **OTD by Shipping Mode** (a core KPI) and pinpointed **Departments/Cities struggling with delivery schedule variance** to address bottlenecks. |
| **Financial Performance** | Total Net Profit by Category, Gross Margin by Customer Segment, Discount Cost Analysis, CLV. | Quantified the **financial impact of negative order statuses** (Canceled/Fraud) and calculated the **Repeat Purchase Rate** to approximate Customer Lifetime Value (CLV). |

## 💡 Technical Highlights (MySQL)
* **Complex ETL:** Utilized `LOAD DATA LOCAL INFILE` with variable assignment and the `STR_TO_DATE` function to correctly import and transform date columns from string format.
* **Error Handling:** Implemented fixes for `Error 1300` (character set issues) and `Error 1054` (column count mismatch during import).
* **Window Functions & CTEs:** Used a `WITH` clause for advanced Customer Lifetime Value (CLV) approximation and `CASE` statements for performance bucketing (e.g., Delivery Performance).

---
