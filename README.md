# Online Retail Data Analysis 
# 🎯 Objectives
The objectives of this assignment are to:
- Load raw retail transaction data into a PostgreSQL database
- Clean and transform the data using defined business rules
- Store a cleaned, analytics-ready dataset in SQL
- Perform Python-based analysis to answer key business questions
- Generate supporting CSV files and visual proof of work

  # 📦 Dataset Overview

**Dataset:** Online Retail Dataset

**Type:** Transaction-level sales data

**Key Fields:**
- InvoiceNo
- StockCode
- Description
- Quantity
- InvoiceDate
- UnitPrice
- CustomerID
- Country

# 🧱 Phase 2 — Data Storage (SQL Layer)
- Create a PostgreSQL table for raw data
- Load the dataset using SQLAlchemy
- Confirm table creation, data types, and row counts

# 🛠 Actions Taken
Raw data loaded into PostgreSQL using Python and SQLAlchemy
Table created: o_retail_raw
Schema and row counts verified using SQL queries
# Raw Table Created
<img width="1150" height="264" alt="image" src="https://github.com/user-attachments/assets/f9122194-da60-435c-ad75-243b99421b17" />

# Row Count Verification
<img width="623" height="479" alt="image" src="https://github.com/user-attachments/assets/68319b77-2545-4511-ab9c-e3e4aa8984e6" />

# 🧹 Phase 3 — Data Preparation (Cleaning & Transformation)
- Validate quantities and prices
- Remove canceled invoices
- Handle missing customer data
- Remove duplicates
- Create new calculated and date fields
- Store cleaned data in SQL

# 🧼 Cleaning Rules Applied
- Removed transactions with Quantity ≤ 0
- Removed records with UnitPrice < 0
- Removed canceled invoices (InvoiceNo starting with “C”)
- Dropped rows with missing CustomerID
- Removed duplicate records

# ✨ Feature Engineering
- Revenue = Quantity × UnitPrice
- Extracted from InvoiceDate:

  - Year
  - Month
  - Day

# 📤 Output
- Cleaned SQL table: online_retail_clean
- Supporting CSV: online_retail_clean.csv
<img width="1140" height="626" alt="image" src="https://github.com/user-attachments/assets/e0a36429-a437-4193-9e87-1a0674d288cc" />
<img width="1160" height="82" alt="image" src="https://github.com/user-attachments/assets/93281caf-cda9-479c-bfe4-66d361b8941f" />

# 📊 Phase 4 — Data Analysis (Python Only)
# 📈 1. Time Series Analysis — 2011 Revenue by Month

- What are the monthly revenue trends in 2011?
- Are there seasonal patterns or monthly changes?

# Actions Taken
Filtered data for Year = 2011
Grouped revenue by month
Calculated total monthly revenue
# Output
- monthly_revenue_2011.csv
- <img width="993" height="349" alt="image" src="https://github.com/user-attachments/assets/a5f3472a-17ef-406e-98d8-6fc6eec5a997" />

# 🌍 2. Country Performance (Excluding United Kingdom)
Which countries generate the most revenue outside the UK?
How much quantity is sold by each country?

# Actions Taken
Excluded United Kingdom
Ranked countries by total revenue
Calculated revenue and quantity sold
Identified top 10 countries
# Output
- top_10_countries.csv
<img width="860" height="369" alt="image" src="https://github.com/user-attachments/assets/8cfe6736-7c20-4978-a720-64a3f8b2c158" />

# 👥 3. Top Customers by Revenue
- Who are the highest-spending customers?
# Actions Taken
Grouped transactions by CustomerID
Ranked customers by total revenue
Selected top 10 customers
# Output
- top_customers.csv
<img width="817" height="268" alt="image" src="https://github.com/user-attachments/assets/1cbfdda1-a785-4121-9766-61e27b0c7c6c" />

# 📦 4. Global Product Demand (Excluding United Kingdom)
Which countries show the highest product demand outside the UK?

# Actions Taken
Grouped data by country
Calculated total quantity sold
Excluded United Kingdom
Ranked countries by demand

# Output
- global_demand.csv
 <img width="833" height="299" alt="image" src="https://github.com/user-attachments/assets/8668f0a2-6bff-420b-9687-13fe4937c966" />

# 📁 Final Deliverables
- ✅ Raw data stored in PostgreSQL (o_retail_raw)
- ✅ Cleaned data stored in PostgreSQL (online_retail_clean)
- ✅ Python scripts for cleaning and analysis
- ✅ Supporting CSV files
- ✅ Screenshot evidence of all actions taken

# 🧠 Key Findings Summary
- Revenue in 2011 shows strong seasonal patterns, with higher sales toward the end of the year
- Several countries outside the UK generate significant revenue and demand
- A small group of customers contributes a large portion of total revenue
- High-demand non-UK markets represent potential growth opportunities

# 📌 Notes
- All data processing and analysis were completed using Python and PostgreSQL
- Screenshots were captured from VS Code and DBeaver to document each step




