# E-Commerce Sales Analysis - Python (Google Colab)

This project analyzes global sales data for a company operating both online and offline.

The goal is to clean, transform, and explore transactional data from multiple sources to uncover insights about company performance across countries, regions, product categories, and sales channels.

The entire analysis is performed in Google Colab using Python, with an emphasis on data quality, visualization, and business interpretation.

## 🔎 Project Overview

Given a dataset that describes product sales for a company operating globally through brick-and-mortar stores and an online shop. The dataset has three CSV files:

- events.csv - transactional events (orders/sales) spanning multiple years.

- products.csv - product catalog (categories, product codes, attributes).

- countries.csv - country and region reference with codes.

### High-level goals:

1. Clean and validate data (missing values, types, duplicates, anomalies).

2. Join tables into a single analysis-ready DataFrame.

3. Compute business metrics and produce visualizations (category / geography / channel / time analyses).

4. Analyze shipping lead times and their relationship with profit.

## 🎯 Objectives & Questions to Answer

- What are the key metrics: total orders, total revenue, total profit, number of unique countries/regions served, average order value, etc.?

- How do sales and profit distribute by product category, country, region, and channel (online vs offline)?

- What are trends over time (daily/weekly/monthly) and by category/country?

- What is the distribution of shipping delay (time between order and shipment)? How does shipping delay affect profit?

- Are there seasonal or weekday patterns in sales for categories or specific products?

- Identify anomalies or unexpected patterns.
  
## 📂 Dataset Description

The dataset consists of three CSV files that describe transactions, products, and geographical information:

1. events.csv

Contains detailed sales records over multiple years.

|Column|Description|
|----|----|
|Order ID|Unique identifier of a sale|
|Order Date|Date when the order was placed|
|Ship Date|Date when the order was shipped|
|Order Priority|Priority of the order|
|Country Code|ISO code linking to country details|
|Product ID|Code linking to product details|
|Sales Channel|Online or Offline sales channel|
|Units Sold|Number of units sold|
|Unit Price|Selling price per unit|
|Unit Cost|Cost per unit|
2. products.csv

Contains product information and categories.

|Column|Description|
|----|----|
|id|Unique product identifier|
|item_type|Product category (Cereal, Beverages, Clothes, etc.)|
3. countries.csv

Contains country and regional metadata.

|Column|Description|
|----|----|
|name|Country name|
|alpha-2, alpha-3|ISO country codes|
|region|Continent or macro-region|
|sub-region|Subdivision within the region|

## 🧹 Data Preparation & Cleaning

Before analysis, all datasets are cleaned and prepared for merging:

- Handle missing values (e.g., missing Country Code in events).

- Detect and remove duplicates and anomalies (e.g., invalid prices or dates).

- Correct data types (convert numeric and date fields properly).

- Standardize country codes and product identifiers for consistent joins.

- Compute derived metrics
  
## 📈 Analysis & Visualization

After cleaning and merging, exploratory data analysis (EDA) is performed to identify key trends:

### Core KPIs

- Total number of orders

- Total revenue, total cost, and total profit

- Average order value (AOV)

- Number of countries and regions with sales

### Analytical Dimensions

- **By Product Category**: Which product types generate the most revenue and profit.

- **By Geography**: Sales performance by country and region.

- **By Channel**: Comparison of online vs offline sales performance.

- **By Time**:

  - Trends in sales, revenue, and profit over time

  - Seasonality and weekday effects on sales volume

- **By Shipping Delay**: Relationship between delivery time and profitability.
  
## ⚙️ Technologies Used

- Python (Google Colab)

- pandas, numpy - data manipulation and cleaning

- matplotlib, seaborn - visualization

- Google Drive integration - dataset management in Colab

## 📊 Project Output

- Cleaned and merged dataset ready for business analysis

- Interactive visualizations showing sales performance by multiple dimensions

- Documented Google Colab notebook containing:

   - Code for cleaning and analysis

   - All visual outputs

   - Explanations and business interpretations
