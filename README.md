# CAPSTONE_PROJECT

## PROJECT OVERVIEW
 ---
This work presents two in-depth data analysis projects that explore retail sales performance and customer segmentation for a subscription service. Using a combination of Excel, SQL, and Power BI, these projects demonstrate how to analyze, interpret, and visualize data to uncover actionable business insight
## DATA CLEANING
---
In both the Sales Performance Analysis and Customer Segmentation projects, data cleaning was essential to ensure accuracy and reliability. This process involved multiple steps to transform raw data into a usable format, identifying and addressing issues such as missing values, inconsistent formats, duplicate records, and outliers. Here’s an outline of the data cleaning process used:

1. Handling Missing Values
Assessment: Checked for missing values across key columns, such as sales figures, product names, customer IDs, and subscription dates.
Action Taken:
For missing sales values:I  verified if missing values could be attributed to returns, cancellations, or data entry errors. Where possible, filled with zeroes or interpolated based on historical data trends.
For customer or product information: I ensured that missing identifiers did not lead to duplicate or inaccurate results. Rows with critical missing values were flagged or removed if data could not be reliably filled.
2. Removing Duplicates
Assessment: Searched for duplicate rows that could misrepresent the data, such as repeat sales transactions or duplicate customer records.
Action Taken: Used filters in Excel to highlight duplicates in key columns (e.g., transaction IDs, customer IDs) and removed all redundant records, keeping only unique entries for accurate analysis.
3. Standardizing Data Formats
Date Formats: Ensured that all date entries followed a consistent format (e.g., YYYY-MM-DD) to facilitate time-based analysis, especially for monthly and quarterly trends.
Text Formatting: Standardized text data to maintain uniformity across categories, such as product names, regions, or subscription types (e.g., consistent use of uppercase or lowercase).
Numeric Formatting: Removed special characters from numerical values (e.g., dollar signs or commas) to simplify calculations and avoid formula errors in Excel.
4. Outlier Detection and Treatment
Assessment: Reviewed data distributions for numerical columns (e.g., sales amounts, subscription duration) to identify potential outliers that could skew the analysis.
Action Taken:
For outliers caused by data entry errors: Corrected or removed values that were unrealistic (e.g., extremely high sales values).
For legitimate high or low values: Left valid data points intact if they provided meaningful insights, such as unusually high sales for popular products or regions.
5. Creating New Columns for Analysis
Added new calculated columns as needed:
In the Sales Performance project: Created month and year columns derived from date data for easy aggregation and trend analysis.
In the Customer Segmentation project: Created a subscription duration column by calculating the difference between start and end dates for each subscription.
6. Data Validation and Quality Check
Conducted a final review to ensure data consistency and quality:
Verified that all key metrics (e.g., total sales, customer counts) aligned with expected values.
Checked that data was ready for SQL queries and Power BI dashboard creation.
## DATA SOURCES
---
The main spurces for this data analysis are the "Sales Data.csv" and "Customer Data.csv" which are the open source datasets that are readily available for free download from online repositories like Kaggle, FRED or other similar platforms.
## TOOLS USED
---
This portfolio uses a combination of Excel, SQL, and Power BI to conduct a thorough analysis of sales and customer data, transforming raw information into actionable insights through data cleaning, exploration, and visualization.
1. MICROSOFT EXCEL;
Purpose: Initial data exploration, summary reporting, and preliminary calculations.
Key Uses:
Pivot Tables: Generated summaries of sales by product, region, and month for a high-level overview.
Formulas and Calculations: Calculated metrics such as average sales per product, total revenue per region, and subscription durations.
Data Cleaning: Identified and handled missing values, removed duplicates, and standardized formats in preparation for SQL analysis and Power BI visualization.
[Download here](https//www.microsoft.com).
2. STRUCTURED QUERY LANGUAGE (SQL);
Purpose: Perform more complex data queries, aggregations, and transformations to answer specific business questions.
Key Uses:
Data Extraction: Queried key insights such as top-selling products, regional sales trends, monthly revenue, popular subscription types, and customer segmentation.
Data Transformation: Used SQL functions to filter data, calculate metrics, and identify trends (e.g., revenue by product category, cancellations within six months).
Data Quality Checks: Ensured consistency and accuracy in data by cross-validating findings with Excel calculations.
3. POWER BUSINESS INTELEGENCE (Power BI)
Purpose: Create interactive dashboards for data visualization, enabling users to explore insights in a visually engaging and user-friendly format.
Key Uses:
Dashboard Creation: Developed dashboards that display sales trends, customer segments, and other key performance indicators (KPIs) found through Excel and SQL analysis.
Data Slicers and Filters: Incorporated slicers for dynamic filtering, allowing stakeholders to interact with the data (e.g., view sales by region, subscription types, or specific time periods).
Data Visualization: Presented complex insights through charts, graphs, and other visuals, making trends and patterns easily understandable. [Download here]
(https//www.microsoft.com)
## Exploratory Data Analysis
---
This involves exploring the the Data to answer some questions which are needful for effective analysis. Questions such as
Sales Data

What is the total sales for each product category
Number of sales in each region
Total revenue per product Monthly Sales totals for the current year
Top 5 customers by purchase amount
Percentage of total sales contributed by each region
Products with no sales in the last quarter

Customer Data
The total number of customers for each region
The most popular subscription type by number of customers
Customers who cancelled their subscription within 6 months
Customers with subscription longer than 12 months
Total revenue by subscription type
Top 3 regions by subscription cancellations
Total number of active and cancelled subscription

## Data Analysis with Excel
---
Sales Data

