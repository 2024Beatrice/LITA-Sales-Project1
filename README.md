[Initial dataset LITA.xlsx](https://github.com/user-attachments/files/17625072/Initial.dataset.LITA.xlsx)### LITA-CAPSTONE-SALES-PERFORMANCE ANALYSIS

# Project Overview
This project analyzes the sales performance of a retail store using Excel, SQL and Power BI. The aim was to identify Top-selling products, regional sales trends, and monthly sales performance of the CAPSTONE dataset project for the period of two years. This analysis will help guide business decisions and imporove revenue strategies.

# Data Sources
The primary source of data used used here is an Excel data file.

# Tools and Technology Used
Microsoft Excel: Download here

Data Cleaning
Data Visualisation
Metrics calculation and analysis
SQL server Data extraction and transformation for insight.

Power BI Visualization and interactive dashboard creation

Github for portfolio building

Project Steps
Data Cleaning and Preparation I performed the following on the initial phase which includes data loading and inspection, handling missing variables, data cleaning and formatting.

Data Exploration with Excel

Calculated Total revenue by region and Average sales per product.
Summarized sales data by product, region, and month using pivot tables.



![IMG_1773](https://github.com/user-attachments/assets/c2d75274-0f21-4d18-af78-d42dab12d46d)

![IMG_1774](https://github.com/user-attachments/assets/08798b6d-cfc5-464c-8bb6-672dbb71ab92)


SQL Analysis
Extracted key insight with SQL such as:

~~~sql 
Create database Salesdata_Project_1

Select * from [dbo].[Salesdata Project1

......Retrieve total sales for each product category

Select Product,
SUM (Revenue) As TotalSales from [dbo].[Salesdata Project1]
Group by Product

.........Number of sales transaction in each region

 Select Region,  
 Count (*) As NumberOfSalesTransaction from [dbo]. [Salesdata Project1]
 Group by Region

......Highest-selling product by total sales value

   Select top 1 product, 
   SUM (Revenue) as HighestSellingProduct from [dbo]. [Salesdata Project1]
   Group by Product

.....Total revenue per product

   Select Product, 
   SUM (Revenue) As TotalRevenue from [dbo]. [Salesdata Project1]
   Group by Product

.....Monthly sales total for the current year

Select
    Format(Orderdate, 'yyyy-MM') AS Sales_Month SUM(Revenue) AS Monthly_Sales_Total From [dbo].[Salesdata Project1]
Where
      Year(Orderdate, 'yyyy-MM')
Order by
Format (Orderdate, 'yyyy-MM)

...............Top 5 customers by total purchase amount

Select Top 5 Customer_ID,
Sum(Revenue) As Totalpurchase from [dbo].[Salesdata Project1]
Group by Customer_ID
Order by Totalpurchase desc

........Percentage of total sales contributed by each region

Select Region, SUM(Revenue) As Region_Sales_Total,
 (SUM(Revenue) * 100.0) / (Select SUM(Revenue) FROM [dbo].[Salesdata Project1] As Sales_percentage FROM [dbo].[Salesdata Project1]
Group By Region

..........Products with no sales in the last quarter

Select Product From [dbo].[Salesdata Project1]
 Group by Product
 Having SUM( CASE WHEN Orderdate >='2024-01-01' AND Orderdate < '2024-04-01' THEN 1 ELSE O END )



# PowerBi

![image](https://github.com/user-attachments/assets/4761d71e-ca7b-4a8f-bca8-6a6bf48554f4)


# Project Summary

    In this project, I used sales data to conduct a comprehensive analysis and identify key performance indicators, including:

Top-Selling Products: Determining which products generated the highest revenue and which products contributed the most to overall sales volume.

Regional Performance: Assessing sales performance across different regions to identify high-performing and underperforming areas.

Monthly Sales Trends: Analyzing sales by month to understand seasonal trends and identify any fluctuations in demand over the year.

