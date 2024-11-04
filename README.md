# Project-1
Documentation of my 1st Project in Data Analysis

### PROJECT TITLE: Sales Performance Analysis for a Retail Store

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


```
SELECT Region, COUNT(OrderID) AS Transaction_Count
FROM CapstoneSales
GROUP BY Region;
```

