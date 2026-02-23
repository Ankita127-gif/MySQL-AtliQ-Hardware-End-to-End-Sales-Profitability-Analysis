📊 Sales & Finance Analytics using SQL
End-to-End P&L & Performance Reporting System
📌 Project Overview

AtliQ Hardware is a growing company that wanted to implement data analytics to make data-driven business decisions.

This project was originally developed in Power BI.
I rebuilt the entire business logic using SQL, transforming raw transactional data into finance-ready reports and reusable reporting architecture.

The objective was to simulate a real-world Sales & Profitability reporting system completely in SQL.

🏗 Data Model

The database follows a Star Schema:

Fact Tables

fact_sales_monthly

fact_gross_price

fact_pre_invoice_deductions

fact_post_invoice_deductions

Dimension Tables

dim_product

dim_customer

⚙ What I Built Using SQL
🔹 1. Fiscal Year Logic

Converted calendar dates into Fiscal Year using User Defined Functions.

Ensured consistent financial reporting logic across queries.

🔹 2. Product-Level Sales Reporting

Generated monthly product sales report including:

Sold Quantity

Gross Sales

Net Invoice Sales

Net Sales

Enabled product performance tracking at SKU level.

🔹 3. Complete P&L Calculation Pipeline

Implemented full sales calculation logic:

Gross Sales
→ Net Invoice Sales (after pre-invoice discount)
→ Net Sales (after post-invoice discount)


To make logic reusable and scalable, I created:

Views (sales_preinv_discount, sales_postinv_discount, net_sales)

CTE-based structured queries

Avoided creating physical tables to reduce duplication and storage.

🔹 4. Dynamic Stored Procedures

Built parameterized stored procedures for:

Top N Markets by Net Sales

Top N Customers by Net Sales

Top N Products per Division

Market Badge Classification (Gold/Silver)

Enabled self-service reporting for stakeholders.

🔹 5. Advanced SQL Techniques Used

Complex JOINs

CTEs

Window Functions (OVER(), PARTITION BY)

DENSE_RANK()

Stored Procedures

User Defined Functions

Views

Conditional Logic

FIND_IN_SET for dynamic filtering

📈 Key Business Insights Derived
🔹 1. Revenue Concentration Risk

A small number of markets and customers contributed a large portion of total Net Sales.

👉 Indicates dependency on key accounts
👉 Helps in strategic risk planning

🔹 2. Discount Impact on Profitability

Significant gap observed between:

Gross Sales

Net Invoice Sales

Net Sales

Pre and post-invoice discounts had major impact on final revenue.

👉 Supports discount policy evaluation
👉 Helps finance team analyze margin leakage

🔹 3. Top Performing Markets

Using Top-N analysis, identified high revenue markets (Gold category).

👉 Enables focused marketing & resource allocation

🔹 4. Regional Performance Distribution

Customer contribution varied significantly across regions.

👉 Helps identify underperforming regions
👉 Supports regional sales strategy

🔹 5. Product Performance Insights

Top-selling products were identified per division using ranking functions.

👉 Helps in inventory planning
👉 Supports demand forecasting
👉 Identifies low-performing SKUs

🔹 6. Customer Contribution Analysis

Using window functions, calculated percentage contribution of each customer to total revenue.

👉 Enables prioritization of strategic accounts
👉 Supports account management decisions

💼 Business Impact

✔ Automated recurring business reports
✔ Reduced manual Excel-based calculations
✔ Built scalable and reusable SQL architecture
✔ Simulated real-world Finance P&L system
✔ Enabled stakeholder self-service reporting
✔ Improved reporting consistency and accuracy

🚀 What This Project Demonstrates

Strong SQL fundamentals + Advanced SQL

Understanding of Finance & Sales analytics

Ability to convert BI dashboard logic into backend SQL

Data modeling & structured thinking

Business-first approach to analytics
