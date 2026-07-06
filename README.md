# Retail Customer and Revenue Analysis

## Overview

This project uses SQL to analyze retail customer and transaction data. The goal is to understand customer demographics, revenue performance, brand-level sales, monthly trends, and customer segment behavior.

The analysis focuses on turning raw retail data into business insights that can support customer targeting, brand strategy, and sales planning.

## Business Questions

This analysis answers the following questions:

* Who are the main customers by age group, gender, and income level?
* Which brands generate the most revenue?
* Do higher-revenue brands also have higher customer ratings?
* How does revenue change from month to month?
* Do revenue drops align with changes in customer count?
* Which customer segments contribute the most to total revenue?

## Key Analysis Performed

* Summary statistics for total customers, total revenue, average transaction amount, and transaction range
* Customer demographic analysis by age group, gender, and income level
* Brand revenue ranking using aggregation and window functions
* Average product rating comparison by brand
* Monthly revenue trend analysis
* Customer segment revenue share and revenue per customer

## Key Insights

* The customer base is concentrated in younger age groups, especially customers between 18 and 34.
* Male customers represent a larger share of customers across age groups.
* Pepsi, Zara, and Nike are among the top revenue-generating brands.
* Some lower-revenue brands have higher average ratings than the highest-revenue brands.
* Revenue fluctuates across months, with noticeable dips in May, August, September, November, and December.
* Revenue declines align with decreases in customer count, suggesting that lower customer traffic may be a major driver of weaker sales performance in those months.
* New customers contribute the largest share of total revenue at about $12M, or 40% of all sales.
* Revenue per customer remains consistent across all segments, so differences in total revenue are mainly driven by customer count rather than higher spending per person.

## Recommendations

* Strengthen marketing and inventory strategies for the strongest customer groups while also creating campaigns to attract underrepresented customer segments.
* Investigate why highly rated brands are generating lower revenue, as this may indicate issues with brand visibility, pricing, promotion, or inventory availability.
* Run targeted promotions or customer acquisition campaigns during months with revenue and customer count declines.
* Focus on retaining regular customers while encouraging more customers to move into the higher-level segment.

## Tools Used

* SQL
* Databricks Notebook
* Data visualization in Databricks
* Tableau

## Dataset

The analysis uses two retail tables:

* `retail_customers`: customer demographic information, including age, gender, income level, and customer segment
* `retail_transactions`: transaction-level data, including revenue, product brand, ratings, transaction date, and customer ID

The two tables are inner-joined using `CUSTOMER_ID`.

Source: [Retail Analysis on Large Dataset](https://www.kaggle.com/datasets/sahilprajapati143/retail-analysis-large-dataset/data)

## Skills Demonstrated

* SQL joins
* Aggregation with `COUNT`, `SUM`, `AVG`, `MIN`, and `MAX`
* Conditional logic using `CASE WHEN`
* Grouped customer segmentation
* Window functions including `RANK()` and `LAG()`
* Month-over-month trend analysis
* Business insight generation
* Data storytelling with SQL outputs and visualizations via Tableau

## Dashboard (Tableau)
Built two linked, interactive Tableau dashboards (Sales Performance & Customer Insights) to make the SQL-driven insights explorable for non-technical stakeholders:
- Cross-dashboard filter actions (e.g., filtering by brand updates customer demographics view)
- Parameter-driven "Top N Brands" control
- Calculated fields for age segmentation, dynamic KPI titles, and highest/lowest month highlighting
- Stacked bar charts breaking down revenue by age, gender, and income; brand-level revenue and rating comparisons

🔗 [View live dashboard on Tableau Public](https://public.tableau.com/views/CustomerSalesPerformanceAnalysis/SalesDashboard?:language=en-US&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link)

![(Sales Dashboard)](https://github.com/namvien94/retail_analysis_sql_databricks/blob/96a1640745a1c562aed75bcd44e843aa10afada2/Sales%20Dashboard.png)

![Customer Dashboard](https://github.com/namvien94/retail_analysis_sql_databricks/blob/96a1640745a1c562aed75bcd44e843aa10afada2/Customer%20Dashboard.png)
