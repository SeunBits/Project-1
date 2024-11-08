
# Project-1
Documentation of my 1st Project in Data Analysis

### PROJECT TITLE: Sales Performance Analysis for a Retail Store

### OUTLINE
[PROJECT OVERVIEW](#project-overview)

[DATA SOURCES](#data-sources)

[TOOLS USED](#tools-used)

[DATA CLEANING AND PREPARATIONS](#data-cleaning-and-preparations)

[EXPLORATORY DATA ANALYSIS](#exploratory-data-analysis)

[DATA ANALYSIS](#data-analysis)

[DATA VISUALIZATION](#data-visualization)

### PROJECT OVERVIEW
This project focuses on analyzing the sales performance of a retail store using data analysis tools like Excel, SQL, and Power BI. The objective is to derive key insights such as top-selling products, regional sales performance, and monthly trends. The final deliverable is an interactive Power BI dashboard that presents these insights in a visually appealing and informative manner.
     -  This project demonstrates proficiency in data analysis, SQL querying, and data visualization, culminating in a comprehensive sales performance dashboard.

### KEY STEPS:

#### Data Exploration in Excel:
  -  Used pivot tables to summarize:
        -  Top 3 Regions by Sales
        -  Bottom 3 Products by Quantity Sold
        -  Product by Average Total Sales
        -  Percentage of Total Sales by Product
        -  Sales by Month, detailed for the years 2023 and 2024
        -  Calculated metrics such as average sales per product and total revenue by region.
        -  Created additional reports highlighting key sales metrics and trends.

#### SQL Analysis:
  -  Loaded the dataset into SQL Server and wrote queries to extract insights on sales performance.
  -  Key queries include total sales by product category, regional transaction counts, highest-selling products, and monthly sales trends.

#### Power BI Visualization:
  -  Built an interactive dashboard that showcases the findings from Excel and SQL.
  -  Visualized key metrics, top-performing products, and regional sales breakdowns.

 ### DATA SOURCES
   -  Sales Data excel file
   -  Sales Data csv file

 ### TOOLS USED
   -   Microsoft Excel [Download Here](https://www.microsoft.com)
          - For Data Cleaning
          - For Analysis
          - For data Visualization
   -   SQL - Structured Query Language for Data Quering
   -   Github for Portfolio building
   -   Microsoft Power BI
          - Data Cleaning
          - Analysis
          - Visualization

### DATA CLEANING AND PREPARATIONS
In the initial phase of Data Cleaning and preparations, i performed the following action;
  -   Data loading and Inspection
  -   Handling missing variables
  -   Data Cleaning and formatting

### EXPLORATORY DATA ANALYSIS
This involved exploring of the Data to answer some questions about the Data such as;
  -   Top 3 Regions by Sales
  -   Bottom 3 Products by Quantity Sold
  -   Average Total Sales per product
  -   Percentage of Total Sales by Product
  -   Sales by Month, detailed for the years 2023 and 2024
  -   Calculated metrics such as average sales per product and total revenue by region.
  -   Total sales by product category
  -   Regional transaction counts
  -   Highest-selling products
  -   Monthly sales trends.

### DATA ANALYSIS
This is where I included some basic lines of code or queries and some of the DAX expressions used during the analysis;

#### Data Analysis with Excel
---
     1.     Summary of total sales by Product

![Screenshot 2024-11-04 115627](https://github.com/user-attachments/assets/ec82c443-0dcb-4e10-9c6b-3725571859cc)

     2.     Summary of total sales by Region

![Screenshot 2024-11-04 120743](https://github.com/user-attachments/assets/576e662f-69a7-4cde-974b-edf0f8a9eb6c)

     3.     Summary of total sales by Month

![Screenshot 2024-11-04 121101](https://github.com/user-attachments/assets/b56ea00f-77c7-45e2-ab69-e19799a0a72f)

     4.     Summary of Top 3 Regions by Sales

![Screenshot 2024-11-04 121320](https://github.com/user-attachments/assets/7adde82e-24e9-4e87-9c8f-0b88013b6959)

     5.     Summary of Bottom 3 Products by Quantity Sold

![Screenshot 2024-11-04 121456](https://github.com/user-attachments/assets/1725b1e2-7848-49a6-93c0-05273b0763d3)

     6.     Summary of Average Total Sales By Product

![Screenshot 2024-11-04 121629](https://github.com/user-attachments/assets/8a67006a-f71a-476d-a593-0b60f37d6167)

     7.      Summary of Average Total Sales By Product
     
![Screenshot 2024-11-04 121746](https://github.com/user-attachments/assets/1b9ebda2-2022-4f5e-a035-6c2f4d70f7bd)

     8.     Summary of Sales by Month, detailed for the years 2023 and 2024

![Screenshot 2024-11-04 121906](https://github.com/user-attachments/assets/4543e799-c1dd-44c2-9a0b-0c7da552aca5)

     9.     Average sales per product
This is done by using the excel function AVERAGEIF 

## =AVERAGEIF(range,criteria,[average_range])

WHERE;

    - Range: the range of cells to evaluate. The column that has the condition, in this sense product
    - Criteria: the condition that must be met. This can be any of the 6 products in this analysis. This was done for each of the region.
    - Average_range: the actual cell to average. The column that has the number to be summed, in this case was the Total sales.

    SHIRT	=AVERAGEIF(C2:C50001,C2,H2:H50001)
    SHOES	=AVERAGEIF(C2:C50001,C15,H2:H50001)
    HAT	=AVERAGEIF(C2:C50001,C49981,H2:H50001)
    SOCKS	=AVERAGEIF(C2:C50001,C49977,H2:H50001)
    JACKET=AVERAGEIF(C2:C50001,C49978,H2:H50001)
    SHOES	=AVERAGEIF(C2:C50001,C7,H2:H50001)

![Screenshot 2024-11-04 131902](https://github.com/user-attachments/assets/0bfbc20f-b596-429a-9fcd-6866bee4e289)

     10.     Total revenue by region.
This is done by using the excel function SUMIF 

## =SUMIF(range,criteria,[sum_range])

WHERE;

     •	Range: the range of cells to evaluate. The column that has the condition, in this sense region
     •	Criteria: the condition that must be met. This can be any of the 4 regions in this analysis. This was done for each of the region.
     •	Sum_range: the actual cell to sum. The column that has the number to be summed, in this case was the Total sales.
     
     NORTH     =SUMIF(D2:D50001,D2,H2:H50001) 
     SOUTH     =SUMIF(D2:D50001,D3,H2:H50001)
     EAST     =SUMIF(D2:D50001,D4,H2:H50001)
     WEST     =SUMIF(D2:D50001,D5,H2:H50001)

![Screenshot 2024-11-04 131440](https://github.com/user-attachments/assets/cf9aab3f-8120-4698-b0a6-c8ad61190d90)


#### Data Analysis with SQL

     1.     Total sales for each product category.
```
SELECT Product, SUM("Total_Sales") AS Total_Sales
     FROM CapstoneSales
     GROUP BY Product;
```
![Screenshot 2024-11-04 202241](https://github.com/user-attachments/assets/e521d5d6-2b7c-48e6-b1f0-795d63d07cb9)

     2.    Number of sales transactions in each region.
```
SELECT Region, COUNT(OrderID) AS Transaction_Count
FROM CapstoneSales
GROUP BY Region;
```
![Screenshot 2024-11-04 202351](https://github.com/user-attachments/assets/faefda03-a82e-4ba6-9bfe-34f52e4a763c)

     3.     Highest-selling product by total sales value.
```
SELECT TOP 1 Product, SUM("Total_Sales") AS Total_Sales
FROM CapstoneSales
GROUP BY Product
ORDER BY Total_Sales DESC;
```
![Screenshot 2024-11-04 203340](https://github.com/user-attachments/assets/220cbac7-15c2-4367-804e-7720ba8b15b5)

     4.    Total revenue per product.
```
SELECT Product, SUM("Total_Sales") AS Total_Revenue
FROM CapstoneSales
GROUP BY Product;
```
![Screenshot 2024-11-04 202440](https://github.com/user-attachments/assets/1a0a02c3-bb0c-4aa4-a4cb-4a7e8a840d6f)

     5.     Monthly sales totals for the current year.
```
SELECT FORMAT(OrderDate, 'yyyy-MM') AS Month, 
       SUM("Total_Sales") AS Monthly_Sales
FROM CapstoneSales
WHERE YEAR(OrderDate) = YEAR(GETDATE())
GROUP BY FORMAT(OrderDate, 'yyyy-MM')
ORDER BY Month;
```
![Screenshot 2024-11-04 203138](https://github.com/user-attachments/assets/30c0e645-064f-4a19-85df-7651577efadb)

     6.     Top 5 customers by total purchase amount.
```
SELECT TOP 5  "Customer_Id", SUM("Total_Sales") AS Total_Purchase
FROM CapstoneSales
GROUP BY "Customer_Id"
ORDER BY Total_Purchase DESC
```
![Screenshot 2024-11-04 202709](https://github.com/user-attachments/assets/72d9c2e5-90a1-42f6-809a-9776eaa7b981)

     7.     The percentage of total sales contributed by each region.
```
SELECT Region,
       SUM("Total_Sales") AS Regional_Sales,
       (CAST(SUM("Total_Sales") AS FLOAT) / 
        CAST((SELECT SUM("Total_Sales") FROM CapstoneSales) AS FLOAT) * 100) AS Sales_Percentage
FROM CapstoneSales
GROUP BY Region;
```
![Screenshot 2024-11-04 202918](https://github.com/user-attachments/assets/704a06d2-3d21-400d-9f34-513824598589)

     8.     Products with no sales in the last quarter.
```
SELECT Product
FROM CapstoneSales
WHERE Product NOT IN (
    SELECT Product
    FROM CapstoneSales
    WHERE OrderDate >= DATEADD(MONTH, -3, GETDATE())
)
GROUP BY Product;
```
![Screenshot 2024-11-04 203018](https://github.com/user-attachments/assets/db84e19a-78e2-407a-958e-2354fae8fa39)


### DATA VISUALIZATION

#### From Excel

---
![Screenshot 2024-11-04 122549](https://github.com/user-attachments/assets/a69f6da7-8955-4f3c-b3c4-91a52db3db58)


![Screenshot 2024-11-04 122659](https://github.com/user-attachments/assets/d08deddb-0bd5-4fd5-a70e-f6d91670751d)


![Screenshot 2024-11-04 122841](https://github.com/user-attachments/assets/2d7df052-74dc-485c-b435-0e75523ba941)




