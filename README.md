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
## EXPLORATORY DATA AnNALYSIS
---
This involves exploring the the Data to answer some questions which are needful for effective analysis. Questions such as
### Sales Data

 *What is the total sales for each product category
 *Number of sales in each region
 *Total revenue per product Monthly Sales totals for the current year
 *Top 5 customers by purchase amount
 *Percentage of total sales contributed by each region
 *Products with no sales in the last quarter

### Customer Data
 *The total number of customers for each region
 *The most popular subscription type by number of customers
 *Customers who cancelled their subscription within 6 months
 *Customers with subscription longer than 12 months
 *Total revenue by subscription type
 *Top 3 regions by subscription cancellations
 *Total number of active and cancelled subscription

## DATA ANALYSIS WITH EXCEL
---
### Sales Data
[LITA Capstone Dataset (1).xlsx](https://github.com/user-attachments/files/17638634/LITA.Capstone.Dataset.1.xlsx)
[LITA CAPSTONE Cleaned EXCEL PIVOT TABLE.xlsx](https://github.com/user-attachments/files/17638672/LITA.CAPSTONE.Cleaned.EXCEL.PIVOT.TABLE.xlsx)
### Sales Data
 Sales Data
Screenshot 

Screenshot (14)

Customer Data
Screenshot (16)

Screenshot (17)

## DATA VISUALIZATION WITH POWER BI.
---
### Sales data
Screenshot (18)

Customer data

Screenshot (19)

Attrition count 2

## INSIGHT ON ANALYSIS.
---

### Sales Data

 *Shoes is the best selling product with over 600,000 sales
 
 *Socks is the least selling product with about 180,000 sales
 
 *The busiest month was February
 
 *There was strong and high sales in the first and second quarter
 
 *Sales was down by about 50% in the last quarter
 
 *In all the regions, South had 44% of sales, East had 23%, North had 18% and lastly West with 14%
 
 *Average sales for the year was 211.78% showing strong customer interest throughout the year
 
 *Customer data
 
 *Basic Subsciption emerged as the most popular type of subscription accounting for over 50% of all the subscriptions
 
 *Average Subscription was 365vdays
 
 *East showed a remarkable commitment to their subscription with zero cancellation while others occasionaly cancel their subscription
 
 *Total revenue generated was 68 million which is quite impressive and also shows the loyalty cusomers place on theie subscription thereby building a strong foundation 
 for the service
 
## DATA ANALYSIS WITH SQL.

### Sales Data

SELECT * FROM [dbo].[Sales Data];

- Total sales from each product category 
select PRODUCT, SUM(Total_Sales) as Totalsales from [dbo].[Sales Data]
group by Product;

- Number of sales transaction in each region 
select Region, COUNT(Total_Sales) as  No_of_sales_by_region
from [dbo].[Sales Data]
Group by Region

- Highest selling product by total sales value 
select PRODUCT, SUM(Total_Sales) as highest_selling_product from [dbo].[Sales Data]
group by Product
order by PRODUCT desc

- Total revenue per product 
select PRODUCT, SUM(Total_Sales) as Totalsales from [dbo].[Sales Data]
group by Product;

- Monthly sales totals for the current year 
select month(orderdate) as month,
SUM(quantity*unitprice) as monthly_sales
from[dbo].[Sales Data]
where YEAR(OrderDate)=YEAR(GETDATE())
group by MONTH(OrderDate);

- Top 5 customers by total purchase amount 
select top 5 customer_Id,
sum(total_sales) AS Total_purchase_Amount
From [Sales Data]
group by customer_ID
order by
Total_purchase_Amount DESC;

- Percentage of total sales contributed by each region 

SELECT REGION, sum(quantity*unitprice) as Totalsales,
sum(quantity*unitprice)* 1.0/ (select sum(Quantity * Unitprice) 
from [dbo] .[Sales Data]) * 100
as PercentageOfTotalSales
from [dbo] .[Sales Data]
group by Region;

- Products with no sale in the last quater 
select distinct product, orderid, quantity
from [dbo].[Sales Data]
where product NOT IN
(select distinct product
from [dbo].[Sales Data]
where OrderDate between '2024-07-01' and '2024-09-30'
)

Customer Data

SELECT * FROM [dbo].[Customer Data];

- Total number of customers from each region------
Select region, COUNT(distinct customerid)
as total_customer from [dbo].[Customer data]
group by Region;

- Most popular subscription type by the number of customers----
Select top 1 subscriptiontype, 
COUNT(distinct customerid)
as total_customers from [dbo].[Customer data]
group by SubscriptionType
order by total_customers desc;

- Customers who cancelled their subscription within 6 months 
select customerid, customername, canceled
from [dbo].[Customer data]
where canceled = 'true' and month (subscriptionStart) between 1 and 6

- Average subscription duration for all customers 
select AVG(datediff(day, subscriptionstart, subscriptionend))
as avg_subscription_duration from [dbo].[Customer data]

- Customers with subscription longer than 12 months 
select customerid from [dbo].[Customer data]
where DATEDIFF(month, subscriptionstart, subscriptionend) >12;

- Total Revenue by subscription type 
select subscriptiontype, 
SUM(revenue) as total_revenue from [dbo].[Customer data]
group by SubscriptionType;

- Top 3 regions by subscription cancellation 
select Region, COUNT(customerid) as Totalccancellations
from [dbo].[Customer data]
where canceled = 'True'
group by Region
order by Totalccancellations DESC;

- Total number of active and cancelled subscription 
Select canceled, COUNT(customerid) as SubscriptionCount
from[dbo].[Customer data]
Group by Canceled;



