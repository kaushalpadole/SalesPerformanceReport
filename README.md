# Sales Performance Report — CYKLES

This repository contains a comprehensive Power BI project analyzing sales, products, and customer data for **Cykles**, a fictional global cycling brand (built on the AdventureWorks dataset). The project transforms raw data into actionable insights through a multi-stage ETL and visualization process, with a fully custom brand identity and dashboard design.

---

# Business Problem

Cykles, a cycling products retail company, wants to:

1. Monitor overall business performance (Revenue, Profit, Orders, Return Rate)
2. Identify top customers and high-value segments
3. Track product-level performance vs targets
4. Analyze return trends and category performance
5. Support management with data-driven decisions

The objective was to build an interactive dashboard solution to provide real-time business insights across executive, customer, and product levels.

---

# Methodology

## Step 1: Data Preparation (Power Query Editor)

- Cleaned missing and inconsistent values
- Removed duplicates
- Standardized column formats (date, currency, categories)
- Created calculated columns where necessary
- Transformed raw tables into structured fact & dimension tables

## Step 2: Data Modeling

### Key Components of the Model:
1. **Fact Tables:** Centered around Sales Data and Returns Data, containing quantitative measures like OrderQuantity and ReturnQuantity.
2. **Dimension Tables (Lookups):** Provide descriptive context for the facts, including Customer, Product, Territory, and a dedicated Calendar table for time-intelligence analysis.
3. **Snowflake Elements:** The model includes a sub-hierarchy for products (Product Subcategories and Categories) to allow for granular drill-down analysis.

<p align="center">
  <img src="https://github.com/kaushalpadole/AdventureWorks-Report/blob/main/assets/Data%20Model.png?raw=true" width="900">
</p>

### Technical Implementation Details:
1. **Cardinality:** Mostly One-to-Many (1:*) relationships, ensuring data integrity and preventing many-to-many ambiguity.
2. **Filter Direction:** Primarily one-way filtering (from Lookups to Facts) to maintain high performance and predictable DAX results.
3. **Date Intelligence:** A central Calendar Lookup table is linked to both Sales and Returns, enabling year-over-year comparisons and trend analysis.

<p align="center">
  <img src="https://github.com/kaushalpadole/AdventureWorks-Report/blob/main/assets/Relationships.png?raw=true" width="900">
</p>

## Step 3: DAX Calculations

Created a dedicated measure table consisting of:

1. Total Revenue
2. Total Profit
3. Total Orders
4. Return Rate
5. Revenue per Customer
6. Monthly Revenue & Profit Trends
7. Target vs Actual KPIs
8. Adjusted Profit (Price Adjustment Simulation)
9. Top N Customers & Products

Key DAX functions used: `CALCULATE`, `SUMX`, `DIVIDE`, `FILTER`, `ALL`, `DATESYTD`

## Step 4: Visualization (Power BI Report)

Built **3 interactive dashboards** and **2 AI-powered analytics pages**, all themed around the Cykles brand identity (charcoal dark background, gold + crimson accent palette, custom hexagonal logo).

### Executive Overview Dashboard
<p align="center">
  <img src="https://github.com/kaushalpadole/AdventureWorks-Report/blob/main/assets/Executive%20Overview.png?raw=true" width="900">
</p>

### Customer Insights Dashboard
<p align="center">
  <img src="https://github.com/kaushalpadole/AdventureWorks-Report/blob/main/assets/Customer%20Insights.png?raw=true" width="900">
</p>

### Product Insights Dashboard
<p align="center">
  <img src="https://github.com/kaushalpadole/AdventureWorks-Report/blob/main/assets/Product%20Insights.png?raw=true" width="900">
</p>

### Orders Decomposition Tree
<p align="center">
  <img src="https://github.com/kaushalpadole/AdventureWorks-Report/blob/main/assets/Orders%20Decompostion.png?raw=true" width="900">
</p>

### Key Influencers
<p align="center">
  <img src="https://github.com/kaushalpadole/AdventureWorks-Report/blob/main/assets/Key%20Influencers.png?raw=true" width="900">
</p>

---

# Skills Used

- Power BI Desktop
- Power Query (ETL)
- Data Cleaning & Transformation
- Data Modeling (Star Schema / Snowflake)
- DAX (Data Analysis Expressions)
- KPI Design & Dashboard Layout
- Brand Identity Application in BI Tools
- Data Visualization Best Practices

---

# Results

- Built an executive-level interactive reporting solution for a fictional cycling brand
- Identified top revenue-generating categories — Accessories leading with 7.4K orders
- Flagged high-return products (Sport-100 Helmets, Bike Stands) for quality investigation
- Tracked revenue growth trend from 2020–2022, reaching $9.3M total
- Enabled product-level performance tracking vs monthly targets
- Simulated price adjustments to quantify impact on adjusted profit

### Business Impact:
1. Improved visibility into sales & profitability across categories
2. Identified product and segment optimization opportunities
3. Enabled data-driven strategic decisions at the executive level

---

# Business Recommendations

1. **Focus on High-Performing Categories:**
   Accessories generate the highest order volume — consider expanding the product line or increasing marketing investment.

2. **Reduce Product Return Rates:**
   Sport-100 Helmets and Bike Stands show elevated return percentages. Investigate potential causes: product quality, inaccurate descriptions, or shipping damage.

3. **Optimize Pricing Strategy:**
   Use the Price Adjustment Simulation on the Product Detail page to model price increases and their effect on adjusted profit before implementing changes.

4. **Strengthen Customer Retention:**
   Focus on high-value customers (top segment averages $12K+ revenue). Launch loyalty programs and personalized campaigns targeting Professional and Skilled Manual segments.

5. **Improve Underperforming Products:**
   Products tracking below monthly targets should be evaluated for promotional campaigns, bundling strategies, or inventory adjustments.

---

> **Dataset note:** This project uses the publicly available AdventureWorks dataset, reimagined under the fictional Cykles brand for portfolio purposes.











