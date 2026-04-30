# Sales Person Performance Analysis - SQL Project

An advanced data analysis project focused on evaluating **salesperson performance** using the **AdventureWorks database**. The project leverages SQL and analytical techniques to uncover patterns in revenue generation, territory distribution, and demographic impact, enabling better **data-driven business decisions**.

# Table of Contents  

* [Brief](#Brief)
* [Project_Goals](#Project_Goals)
* [DataSet](#DataSet)
* [How_It_Works](#How_It_Works)
* [Tech_Stack](#Tech_Stack)
* [Tools](#Tools)  
* [Key_Findings](#Key_Findings)  
* [Key_Recommendations](#Key_Recommendations)
* [Future_Work](#Future_Work)  


# Brief
This project analyzes salespersons within the AdventureWorks dataset to understand key performance drivers such as territory allocation, experience, and demographics. Using SQL-based analysis, the project uncovers insights that help evaluate efficiency, identify top performers, and highlight improvement opportunities.


# Project_Goals
- Identify top-performing salespersons based on revenue
- Analyze revenue distribution across different territories
- Evaluate the impact of working in multiple territories
- Measure the effect of experience (Hire Date) on performance
- Compare performance across gender and marital status
- Analyze yearly sales trends and growth rates


# DataSet
- AdventureWorks Database
- Key tables used:
  - Sales.SalesPerson
  - Sales.SalesOrderHeader
  - Sales.SalesOrderDetail
  - Sales.SalesTerritory
  - Person.Person
  - HumanResources.Employee
  - Production.Product
  - Production.ProductCostHistory


# How_It_Works
1. **Data Extraction & Integration**  
   Multiple tables are joined using keys such as `BusinessEntityID`, `SalesPersonID`, and `TerritoryID` to form a unified dataset for analysis.

2. **Exploratory Data Analysis (EDA)**  
   - Identified total number of salespersons (17)  
   - Explored territory distribution  
   - Evaluated multi-territory assignments  

3. **Revenue Analysis**  
   - Calculated total revenue per salesperson and per territory  
   - Compared single vs multi-territory performance  
   - Identified top and low performers  

4. **Advanced Analytics using Window Functions**  
   - `RANK()` to identify top performers  
   - `SUM() OVER()` for cumulative calculations  
   - `LAG()` for year-over-year comparison  
   - `FIRST_VALUE()` for first-year performance analysis  

5. **Demographic Analysis**  
   - Performance comparison based on:
     - Gender  
     - Marital Status  
     - Age Segmentation  

6. **Time-Based Analysis**  
   - Yearly sales trends  
   - Growth rate calculation  
   - Performance comparison across years  

7. **Profit Calculation (Advanced)**  
   - Profit formula:
     SUM(OrderQty * UnitPrice) - SUM(OrderQty * StandardCost)  
   - Linked product-level data with salesperson performance  


# Tech_Stack
- **SQL Server**: Data querying and analysis  
- **T-SQL**: Window functions, aggregations, and CTEs  


# Tools
I. SQL Server Management Studio (SSMS)  

II. T-SQL  

III. AdventureWorks Dataset  


# Key_Findings
- There are **17 salespersons** in the dataset  
- Working in multiple territories does **not guarantee higher revenue**  
- SalesPersonID 276 is the top revenue generator  
- Only **2 salespersons** generated less than 1M revenue  
- Experience is **not a strong predictor** of performance  
- Male salespersons generated higher total revenue than females  
- Married employees generated higher revenue than single employees  
- Significant performance gap exists between top and low performers  


# Key_Recommendations
- Focus on individual performance rather than number of territories  
- Reallocate territories based on actual performance metrics  
- Implement targeted training programs for low-performing employees  
- Utilize demographic insights to improve hiring strategies  
- Continuously monitor yearly trends for better decision-making  


# Future_Work
- Fix and optimize Year-over-Year calculations  
- Build threshold-based performance classification (High / Medium / Low)  
- Develop an interactive dashboard using Power BI  
- Apply machine learning models for performance prediction  
- Improve profit calculation using consistent cost history  
