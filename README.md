# Sales Performance Report - CYKLES
This repository contains a comprehensive Power BI project focused on analyzing sales, products, and customer data for Cykles, a global manufacturing company. The project transforms raw data into actionable insights through a multi-stage ETL and visualization process.

# Business Problem 
Cykles, a retail company, wants to:

1. Monitor overall business performance (Revenue, Profit, Orders, Return Rate)
2. Identify top customers and high-value segments
3. Track product-level performance vs targets
4. Analyze return trends and category performance
5. Support management with data-driven decisions

The objective was to build an interactive dashboard solution to provide real-time business insights across executive, customer, and product levels.

# Methodology

## Step 1: Data Preparation (Power Query Editor)

- Cleaned missing and inconsistent values
- Removed duplicates
- Standardized column formats (date, currency, categories)
- Created calculated columns where necessary
- Transformed raw tables into structured fact & dimension tables

## Step 2: Data Modeling

### Key Components of the Model:
1. Fact Tables: Centered around Sales Data and Returns Data, containing quantitative measures like OrderQuantity and ReturnQuantity.
2. Dimension Tables (Lookups): Provide descriptive context for the facts, including Customer, Product, Territory, and a dedicated Calendar table for time-intelligence analysis.
3. Snowflake Elements: The model includes a sub-hierarchy for products (Product Subcategories and Categories) to allow for granular "drill-down" analysis.
  <p align="center"> <img src="https://github.com/kaushalpadole/AdventureWorks-Report/blob/main/assets/Data%20Model.png?raw=true" width="900"> </p>

### Technical Implementation Details:
1. Cardinality: Mostly One-to-Many (1:*) relationships, ensuring data integrity and preventing many-to-many ambiguity.
2. Filter Direction: Primarily One-way filtering (from Lookups to Facts) to maintain high performance and predictable results in DAX calculations.
3. Date Intelligence: A central Calendar Lookup table is linked to both Sales and Returns, enabling year-over-year comparisons and trend analysis.
  <p align="center"> <img src="https://github.com/kaushalpadole/AdventureWorks-Report/blob/main/assets/Relationships.png?raw=true" width="900"> </p>

## Step 3: DAX Calculations

Created a measure table consisting of key measures such as:

1. Total Revenue
2. Total Profit
3. Total Orders
4. Return Rate
5. Revenue per Customer
6. Monthly Revenue & Profit Trends
7. Target vs Actual KPIs
8. Adjusted Profit (Price Adjustment Simulation)
9. Top N Customers & Products

Used advanced DAX functions like,

CALCULATE, SUMX, DIVIDE, FILTER, ALL, DATESYTD

## Step 4: Visualization (Power BI Report)

Built 3 interactive dashboards and 3 AI powered advanced analytics:

### Executive Dashboard
<p align="center"> <img src="https://github.com/kaushalpadole/AdventureWorks-Report/blob/main/assets/Executive%20Dashboard.png?raw=true" width="900"> </p>

### Customer Detail Dashboard
<p align="center"> <img src="https://github.com/kaushalpadole/AdventureWorks-Report/blob/main/assets/Customer%20Detail.png?raw=true" width="900"> </p>

### Product Detail Dashboard
<p align="center"> <img src="https://github.com/kaushalpadole/AdventureWorks-Report/blob/main/assets/Product%20Detail.png?raw=true" width="900"> </p>

### Decomposition Tree
<p align="center"> <img src="https://github.com/kaushalpadole/AdventureWorks-Report/blob/main/assets/Decompostion%20Trees.png?raw=true" width="900"> </p>

### Key Influencers
<p align="center"> <img src="https://github.com/kaushalpadole/AdventureWorks-Report/blob/main/assets/Key%20Influencers.png?raw=true" width="900"> </p>


# Skills Used

- Power BI
- Power Query (ETL)
- Data Cleaning
- Data Transformation
- Data Modeling (Star Schema)
- DAX (Data Analysis Expressions)
- KPI Design
- Dashboard Design Principles
- Data Visualization

# Results

- Built an interactive executive-level reporting solution
- Identified top revenue-generating categories (Accessories leading)
- Analyzed high-return products for quality investigation
- Tracked revenue growth trend from 2020–2022
- Enabled product-level performance tracking vs target
- Simulated price adjustments to analyze impact on profit

### Business impact:

1. Improved visibility into sales & profitability
2. Identified optimization opportunities
3. Enabled data-driven strategic decisions

# Business Recommendations

1. Focus on High-Performing Categories:
   Accessories generate the highest orders — consider expanding product line or marketing efforts.

2. Reduce Product Return Rates:
   Some products show higher return percentages
   Product quality issues
   Incorrect product descriptions, shipping damage

3. Optimize Pricing Strategy:
   Use the Price Adjustment Simulation to test price increases
   Maximize profit without significantly impacting demand

4. Strengthen Customer Retention:
   Focus on high-value customers
   Launch loyalty programs
   Personalized marketing campaigns

5. Improve Underperforming Products

Products below target require:

- Promotional campaigns
- Bundling strategies
- Inventory adjustments

































