# Sizwe Coffee- SQL Sales and Profitability Analysis
## Project Overview
This project analsyse the sales and financial performance of Sizwe Cofee (Pty) Ltd using SQL in Databricks

Sizwe Coffee is a coffee roasting and wholesale supply company based in Isando , Johannesburg, with a second distribution centre, in Epping, Capetown. The company serves approximately 1400 business customers, including grocery chains, restaurants,independent cafes, hotels and offices.

The company operates through towo sales channels: Wholesale, contributing approximately 70% of revenue, and Subcriotion, contributing approximately 30%.

The analysis covers two financial years:
FY2024:1 July 2023-30 June 2024
FY2025:1 July 2024-30 June 2025

The Objectives is to use SQL to answer eight business questions and provide insights to nomsa and Bongani.

## Business Questions
The project addresses eight questions:

1. Channel performance: How did revenue change between FY2024 and FY2025 across sales channels?
2. Product Line profitability: Which product lines generated the highest gross profit and gross margin?
3. Collections Perfomance: Which sales channels have outsatnding invoices and longer payment settlement periods?
4. Top Customers: Who were the ten Highest-Revenue customers in FY2025?
5. Trade Promotions: Which fifteen high- revenue wholesale customers have never recived trade promotions?
6. Sales Represntative: Performance : How did sales representative perform against their monthly sale target?
7. Revenue Seasonality: What monthly revenue patterns occured across the two financial years?
8. Gross Margin Analysis : Why did the company's overall gross margin decline despite revenue growth?

## Dataset
The analysis uses the Sizwe Coffee dataset provided for the Witle plus SQL assignment.The data was uploaded into Databricks under the bootcamp.Default schema.

| Table Name | Purpose |
|---|---|
| sizwe_sales_orders_1 | Contains order dates and sales channels |
| sizwe_sales_lines_1 | Contains revenue and cost of goods sold |
| sizwe_customers | Contains customer information |
| sizwe_products_1 | Contains product lines |
| sizwe_reps_1 | Contains sales representatives and targets |
| sizwe_trade_promotions_1 | Contains customer promotion records |

Additional invoice and payment data was used for the collections analysis in Task 3.

## How the tables connect

Sales Orders and Sales Lines are connected using order_id.
Sales Orders and Customers are connected using customer_id.
Sales Lines and Products are connected using sku.
Customers and Sales Representatives are connected using rep_id.
Customers and Trade Promotions are connected using customer_id.
These relationships allow sales, profitability, customer performance and promotional activity to be analysed together.

## SQL Skills Demonstrated

| SQL Technique | Tasks Used | Application |
|---|---|---|
| INNER JOIN | 1, 2, 4, 5, 6, 7, 8 | Combining related tables |
| LEFT JOIN | 4, 6 | Including customers or representatives without matching records |
| SUM and GROUP BY | 1–8 | Calculating totals and summarising data |
| CASE WHEN | 1, 3, 8 | Applying business conditions and financial-year classifications |
| Common Table Expressions (WITH) | 1, 4, 5, 6, 7, 8 | Organising complex queries |
| NULLIF | 1, 2, 6, 7, 8 | Preventing division-by-zero errors |
| NOT EXISTS | 5 | Finding customers without promotions |
| Window Functions | 7, 8 | Calculating month-on-month changes, rolling averages and revenue shares |
| ORDER BY | Multiple tasks | Ranking and sorting results |

## How to Run the SQL Queries

The project was developed using Databricks SQL, To reproduce the analysis:

1.	Open a Databricks workspace.
2.	Create or access a catalog named bootcamp and its default schema.
3.	Import the Sizwe Coffee dataset into the relevant tables.
4.	Open the SQL Editor.
5.	Copy the SQL queries from queries.sql.
6.	Execute each query in task order.
7.	Review the results and compare them with the findings documented below.


## Key Business Insights

### Channel Performance
Sizwe Coffee's overall revenue increased from approximately R441 million in FY2024 to R480 million in FY2025, representing growth of nearly 9%.
Both Wholesale and Subscription contributed to revenue growth, with Wholesale remaining the larger sales channel.

### Product Line Profitability
House blend generated the hightest gross profit of R107.15 million , with a gross margin of 38.33%, making it sizwe coffee's largest contributor to gross profit.
However, Single Origin recorded the highest gross margin of 44.27%,  generating R75.31 million in gross profit. this shows that the product lib=ne earning the most total profit is not necessarily the one with the highest profit margin of 44.27%, generating R75.31 million in gross profit. this shows that the productline earning the most total profit is not necessarily the one with the highest proft margin.

### Collections Performance
Wholesale presents the greatest collection risk, with 3454 unpaid invoices worth R 87.85 million and an average settlement period of 68.68 days, in contrast , subcription has only 44 outstanding invocies worth R 751 178.89, with payments settled within 3.85 days on average. Sizwe Coffee should prioritise investing wholeslae payment delays to improve cash flow and reduce outstanding debts.

### Top Customers
Halvane retail Group dominates FY2025 revenue, genrating R 38.40million, significantly exceeding the second-largest customer, highveld deli 85, at R3. 38 million. the remaining top customers contribute between R1.93 million and R 3.33 million each.  this highlights susbtantial reveneu concentrateion in one major grocery chain, making customer retention, relationship maangement and revenu diversification important priorities for Sizwe coffes's future growth and stability.

### Trade Promotions
The analysis identified high-revenue Wholesale customers who had not received trade promotions.
A recommended approach is to prioritise the top three customers for  volume-based discounts.

### Sales Representative Performance
Sales perfomance was strong, with 16 of 18 representative exceeding their monthly targets. Karabo van wyk achieved the highest performance at 250.32%, generating  R2.25 million in average monthly revenue revenue against a R900 000 target. However, john Naidoo(77.63%) and Sipho Steb (97.99%) fell below target. Sizwe coffee should inestogate their challeneges and provide targeted coaching to improve perfomance.

### Monthly Revenue and Seasonality
Sizwe Coffee showed a consistent seasonal pattern across both financial years, with monthly revenue generally declining from July to December and recovering from January to June.
December was the quietest calendar month in both years. The lowest monthly revenue was R29,872,699.78 in December 2023, compared with R32,609,167.66 in December 2024.

### Gross Margin Decline
Sizwe Coffee's overall gross margin declined from 34.7% in FY2024 to 33.0% in FY2025, despite revenue growth of nearly 9%.
The main driver was a shift in revenue towards Bulk Commercial, the lowest-margin product line. Its revenue share increased from 25.02% to 33.65%, while its gross margin remained approximately 19.9%.
At the same time, higher-margin products lost revenue share. House Blend's share declined from 32.14% to 28.71%, while Single Origin declined from 19.45% to 17.57%.
This indicates that the decline was mainly driven by changes in the sales mix rather than a significant reduction in individual product-line margins.

## Conclusion

This project demonstrates how SQL can be used to transform business transaction data into meaningful insights.
The analysis highlights the importance of monitoring revenue growth alongside profitability, customer payment behaviour, sales performance and product mix.
It also demonstrates that increasing revenue does not always lead to improved profit margins.

## Project Files

•	queries.sql — All eight SQL queries, with written answers included as comments.
•	README.md — Project overview, dataset explanation, SQL skills, execution instructions and business findings.
