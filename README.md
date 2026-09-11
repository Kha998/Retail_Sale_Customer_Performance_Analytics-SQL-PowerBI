# Retail_Business_Performance_Analysis-SQL-PowerBI-
# 🛒 Retail Sales & Customer Performance Analytics

## Project Overview

This project presents an end-to-end **Retail Sales & Customer Performance Analytics solution** developed using **MySQL and Microsoft Power BI**.

The project transforms multi-table retail transactional data into an integrated analytical model and interactive Business Intelligence dashboard to evaluate:

- Overall sales and estimated profitability
- Customer contribution and purchasing performance
- Product and brand performance
- Store and geographic performance
- Product return activity

The solution demonstrates the complete analytics workflow from raw data preparation and SQL analysis to data modeling, DAX KPI development, dashboard visualization, business insights, and actionable recommendations.

---

## Business Problem

The multi-store retail business lacks a consolidated analytical view of sales, customer, product, store, geographic, profitability, and return performance.

This limits management's ability to understand how business performance changes over time, identify the customers, products, stores, and markets driving results, detect underperforming areas, and recognize opportunities for performance improvement.

An integrated analytics solution is therefore required to transform transactional and operational retail data into measurable KPIs and actionable insights that support evidence-based commercial and operational decision-making.

---

## Project Objective

The main objective of this project is to develop an end-to-end retail analytics and Business Intelligence solution that provides management with a consolidated view of business performance, identifies key performance drivers and underperforming areas, and generates actionable insights to support data-driven commercial and operational decisions.

---

##  Business Questions

The project addresses five primary business questions:

1. **Overall Performance**  
   How is the retail business performing overall, and how has performance changed over time?

2. **Customer Performance**  
   Which customer groups contribute most to business performance, and how does purchasing performance differ across customer segments?

3. **Product & Brand Performance**  
   Which products and brands drive sales and estimated profitability, and which areas are underperforming?

4. **Store & Geographic Performance**  
   How does business performance vary across stores, store formats, and geographic markets?

5. **Return Performance**  
   Where are product returns concentrated, and which products, stores, locations, and time periods contribute most to return activity?

---

## Dataset Overview

The project uses a multi-table retail dataset covering sales transactions, customers, products, stores, geographic regions, calendar dates, and product returns.

### Main Data Tables

| Dataset | Description |
|---|---|
| Transactions 1997 | Retail sales transactions for 1997 |
| Transactions 1998 | Retail sales transactions for 1998 |
| Customers | Customer demographic and membership information |
| Products | Product, brand, retail price, and cost information |
| Stores | Store format, location, and operational attributes |
| Regions | Sales district and regional information |
| Returns | Product return transactions |
| Calendar | Date dimension source |

The combined sales data contains approximately **269K transaction records** covering 1997–1998.

---

## Tools & Technologies

| Tool | Purpose |
|---|---|
| **MySQL** | Database creation, data preparation, transformation, EDA, and business analysis |
| **SQL** | Data quality checks, cleaning, transformation, aggregation, and analytical queries |
| **Power BI** | Data modeling, DAX measures, dashboard development, and visualization |
| **DAX** | KPI calculations and time-intelligence measures |
| **Power Query** | Data connection and final validation |
| **Git & GitHub** | Version control and project documentation |

---

## Project Workflow

The project follows an end-to-end analytics workflow:

Raw Retail Data  
→ Database Setup & Import  
→ Database Exploration  
→ Data Quality Assessment  
→ Data Cleaning  
→ Data Transformation & Modeling  
→ Exploratory Data Analysis  
→ SQL Business Analysis  
→ Power BI Data Model  
→ DAX KPI Development  
→ Dashboard Development  
→ Key Insights  
→ Business Recommendations  
→ Portfolio Delivery

---

## SQL Data Preparation & Analysis

The SQL stage was structured into seven scripts:

1. `01_database_setup.sql`
2. `02_database_exploration.sql`
3. `03_data_quality_assessment.sql`
4. `04_data_cleaning.sql`
5. `05_data_transformation_modeling.sql`
6. `06_EDA.sql`
7. `07_business_analysis.sql`

### Key SQL Activities

- Imported multi-table retail data into MySQL
- Assessed missing values and duplicate records
- Validated primary and foreign-key relationships
- Standardized categorical and text fields
- Created analysis-ready tables
- Combined 1997 and 1998 sales transactions
- Built fact and dimension tables
- Performed exploratory data analysis
- Answered business questions using SQL aggregations and analytical queries

---

## Data Model

A **star-schema analytical model** was developed to support efficient reporting and filtering in Power BI.

### Dimension Tables

- `dim_customer`
- `dim_product`
- `dim_store`
- `dim_date`

### Fact Tables

- `fact_sales`
- `fact_returns`

### Relationship Structure

`dim_customer` → `fact_sales`

`dim_product` → `fact_sales`  
`dim_product` → `fact_returns`

`dim_store` → `fact_sales`  
`dim_store` → `fact_returns`

`dim_date` → `fact_sales`  
`dim_date` → `fact_returns`

Customer-level return analysis is intentionally excluded because the returns dataset does not contain a `customer_id`.

---

## KPI Framework

The Power BI measure layer was organized into seven KPI groups:

### 01 — Sales KPIs
- Estimated Sales
- Total Units Sold

### 02 — Profitability KPIs
- Estimated COGS
- Estimated Gross Profit
- Estimated Gross Margin %

### 03 — Customer KPIs
- Total Customers
- Active Customers
- Average Sales per Customer
- Average Units per Customer

### 04 — Product KPIs
- Products Sold
- Average Sales per Product

### 05 — Store KPIs
- Active Stores
- Average Sales per Store
- Average Profit per Store

### 06 — Return KPIs
- Return Records
- Returned Units
- Estimated Return Value
- Aggregate Return Rate %

### 07 — Time Intelligence KPIs
- Previous-Year Estimated Sales
- Year-over-Year Sales Growth %

---

# Power BI Dashboard

The final Power BI report consists of five interactive analytical pages.

## 1️⃣ Executive Overview

**Purpose:** Provide management with a consolidated view of overall business performance.

### Key Analysis
- Estimated Sales
- Estimated Gross Profit
- Estimated Gross Margin %
- Active Customers
- Aggregate Return Rate %
- Monthly sales trends
- Geographic performance
- Store-format performance
- Top products

> Add Executive Overview screenshot here.

---

## 2️⃣ Customer Performance Analytics

**Purpose:** Identify which customer groups contribute most and compare purchasing performance across customer segments.

### Key Analysis
- Total and active customers
- Average sales per customer
- Average units per customer
- Membership contribution
- Income-level performance
- Occupation performance
- Top customers

> Add Customer Performance dashboard screenshot here.

---

## 3️⃣ Product & Brand Analytics

**Purpose:** Identify products and brands driving estimated sales and profitability and detect weaker areas.

### Key Analysis
- Products sold
- Estimated sales
- Estimated gross profit
- Estimated gross margin
- Brand contribution
- Brand ranking changes over time
- Top-performing products

> Add Product & Brand dashboard screenshot here.

---

## 4️⃣ Store & Geographic Performance

**Purpose:** Compare business performance across stores, store formats, and geographic markets.

### Key Analysis
- Active stores
- Average sales per store
- Average profit per store
- Store ranking
- Store-format performance
- Sales vs. profit performance
- Country-level performance

> Add Store & Geographic dashboard screenshot here.

---

## 5️⃣ Return & Refund Analytics

**Purpose:** Identify where product return activity is concentrated.

### Key Analysis
- Return records
- Returned units
- Estimated return value
- Aggregate return rate
- Product return concentration
- Monthly return patterns
- Geographic return performance

> Add Returns dashboard screenshot here.

---

# Key Insights

### Overall Performance

- The business generated approximately **$1.76M in Estimated Sales**.
- Estimated Gross Profit was approximately **$1.05M**.
- Estimated Gross Margin was approximately **59.67%**.
- Performance is concentrated across particular markets and store formats.

### Customer

- Approximately **8.84K customers** made purchases.
- Bronze members generate the largest overall estimated sales contribution.
- Golden members demonstrate stronger average sales per customer.

### Product & Brand

- Approximately **1,559 products** were sold.
- Product and brand contribution varies substantially.
- Brand rankings change over time, indicating dynamic competitive performance within the product portfolio.

### Store & Geography

- The retail network contains **24 stores**.
- The USA contributes the largest estimated sales value.
- Store productivity varies considerably across locations and formats.

### Returns

- The dataset contains **7,087 return records** representing **8,289 returned units**.
- Aggregate Return Rate is approximately **0.99%**.
- Return activity varies across products, markets, stores, and time periods.

---

# Business Recommendations

### Customer Strategy
Develop differentiated strategies for high-contribution and high-value customer segments.

### Product Optimization
Protect high-performing products and brands while investigating persistent underperformers.

### Store Performance
Benchmark weaker stores against stronger locations to identify opportunities for operational improvement.

### Geographic Strategy
Protect strong markets while investigating opportunities to improve weaker geographic performance.

### Return Management
Monitor products, stores, countries, and periods with elevated return quantities and return rates.

---

## Data Limitations

The following limitations should be considered when interpreting the results:

- Product retail price is available instead of actual transaction-level selling price.
- Financial metrics are therefore reported as **Estimated Sales, Estimated COGS, and Estimated Gross Profit**.
- The returns dataset does not contain actual refund amounts.
- Return monetary value is therefore reported as **Estimated Return Value**.
- Return reasons are unavailable.
- Returns do not contain `customer_id` or original transaction identifiers.
- Customer-level return analysis cannot therefore be performed reliably.

---

## 📁 Repository Structure

```text
Retail-Sales-Customer-Performance-Analytics/
│
├── data/
│   └── raw_data
│
├── sql/
│   ├── 01_database_setup.sql
│   ├── 02_database_exploration.sql
│   ├── 03_data_quality_assessment.sql
│   ├── 04_data_cleaning.sql
│   ├── 05_data_transformation_modeling.sql
│   ├── 06_EDA.sql
│   └── 07_business_analysis.sql
│
├── powerbi/
│   └── Retail_Sales_Customer_Performance_Analytics_Dashboard.pbix
│
├── images/
│   ├── 01_executive_overview.png
│   ├── 02_customer_performance.png
│   ├── 03_product_brand_analytics.png
│   ├── 04_store_geographic_performance.png
│   └── 05_return_analytics.png
│
├── docs/
│   └── Retail_Analytics_Project_Documentation.pdf
│
└── README.md
