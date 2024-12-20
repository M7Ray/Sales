# Sales Analysis
- PROJECT OVERVIEW

  Using SQL Server and Power BI for data processing, storage, and visualization, the project offers a comprehensive study of sales performance.
  The dashboards created are: Sales Overview, Customer Details, and Product Details.

  DB used can be accessed [here](https://learn.microsoft.com/en-us/sql/samples/adventureworks-install-configure?view=sql-server-ver15&tabs=ssms)

  Outcomes:
    * Sold Quantity of each product, to which clients and how it has been over time.
    * Identify each sales person work on different products and customers.
    * Measure the numbers against budget and compare the values against performance.
  
  The main tables are:
    
    * DIM_Calendar: This dimension table contains attributes for date-based analysis. Key fields include:
    * DIM_Customers: Stores customer information, essential for customer segmentation and analysis. 
    * DIM_Products: Contains product-related data for sales and inventory analysis.
    * FACT_InternetSales: A fact table that records all internet sales transactions, enabling analysis of sales performance over time. 
    * SalesBudget: Contains budgetary data for financial comparison, helping analyze performance against targets.

  Created Measures:
    * under FACT_InternetSales:
        * Sales = SUM(FACT_InternetSales[SalesAmount])
    * under FACT_Budget:
        * Budget Amount = SUM(FACT_Budget[Budget])
        * Sales / Budget Amount = DIVIDE ([Sales], [Budget Amount])
        * Sales - Budget = [Sales] - [Budget Amount]
  
- Data Cleaning & Transformation (SQL)
  The extracted csv tables were extracted using SQL.

- Data Model
  The following is a screenshot of the data model and prepared tables were read into Power BI.
  It also shows how FACT_Budget has been connected to FACT_InternetSales and other necessary DIM tables.

  <img width="402" alt="Data Model" src="https://github.com/user-attachments/assets/b1d89cbe-1ffb-4cca-ae99-d84697f2f4ed">

  
- POWER BI DASHBOARDS
   * Sales Overview:
    Key visuals include:
      Sales by Top 10 Customers
      Top 10 Product Sales
      Sales and Budget by Month: Tracks sales trends per month compared to budget.
      Customer City Distribution: A map visual illustrating where top customers are located.
   * Customer Details:
    Key visuals include:
      Sales by Customer City
      Sales by Top 10 Customers
      Monthly Sales Table by Customer
   * Product Details:
    Key visuals include:
      Sales by Top 10 Products
      Sales by Customer City
      Monthly Sales Table by Product

     <img width="689" alt="Sales Overview" src="https://github.com/user-attachments/assets/e6a81d4e-92b9-406b-92cb-99fa250ce0cd">
     <img width="686" alt="Customer Details" src="https://github.com/user-attachments/assets/eda3c33f-d822-4ef6-b361-9ea52d3078e7">
     <img width="687" alt="Product Details" src="https://github.com/user-attachments/assets/ade0ec07-e348-4fcb-bf6b-921cb1951669">




- INSIGHTS

  The project enables comprehensive sales analysis, supporting business decisions related to customer engagement, product performance, and geographic sales distribution. By   comparing actual sales with budgeted targets, this dashboard setup provides a robust tool for identifying growth opportunities and optimizing product and customer       
  strategies.

- CONCLUSION

  The project is a strong tool for examining and comprehending several facets of sales performance, consumer behavior, and product popularity. It gives stakeholders the   
  ability to track important indicators, spot trends, and make data-driven decisions by combining data from many sources into interactive Power BI dashboards.
