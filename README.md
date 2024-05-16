# Coffee_Shop_sales-SQL-PRoject
The coffee shop sales data analysis project aims to provide insights into the sales performance of a coffee shop chain operating in three different locations. The project utilizes a combination of SQL, Excel, and Power BI to analyze sales data, identify trends, and make data-driven recommendations to improve business operations.

## Objective:
The primary objective of the project is to analyze sales data from the three coffee shop locations to:

Understand the total sales performance on a monthly basis.
Determine the month-on-month changes in sales.
Analyze the total number of orders and quantity sold each month.
Identify trends and patterns in sales data to make informed business decisions.
## Data Sources:
The project utilizes sales data collected from the three coffee shop locations. The data includes information such as order dates, total sales amount, number of orders, and quantity sold.

## Methodology:
The project follows a structured methodology to analyze the sales data:

### Data Gathering: 
Sales data is collected from each coffee shop location and stored in a central database.

### SQL Analysis: 
SQL queries are used to aggregate the sales data and calculate metrics such as total sales, total orders, and total quantity sold for each month. Month-on-month changes are also calculated using SQL.

### Excel Analysis: 
The SQL results are imported into Excel for further analysis. Excel formulas and functions are utilized to calculate month-on-month changes and differences in sales metrics. Visualizations such as charts and graphs are created in Excel to represent the sales data.

### Power BI Analysis: 
The data is imported into Power BI to create interactive visualizations and dashboards. Power BI is used to analyze trends, identify patterns, and present the analysis findings in a user-friendly format.

### Interpretation and Reporting: 
The analysis findings are interpreted to identify key insights and trends in the sales data. A comprehensive report is prepared summarizing the analysis results and providing recommendations for business improvement.

### Deliverables:
The deliverables of the project include:
SQL queries for aggregating and analyzing sales data.
Excel workbook containing analysis results and visualizations.
Power BI dashboard presenting interactive visualizations of sales data.
A comprehensive report summarizing analysis findings and recommendations.

## Conclusion:
The coffee shop sales data analysis project aims to provide actionable insights into sales performance, enabling the coffee shop chain to make informed decisions to improve business operations and increase profitability.




``` SELECT 
    MONTH(transaction_date) as month_number,
    MONTHNAME(transaction_date) as month_name,
    ROUND(SUM(unit_price * transaction_qty)) AS Total_Sales
FROM 
    COFFEE_SHOP_SALES.PUBLIC.COFFEE_SALES
GROUP BY 
    MONTH(transaction_date), MONTHNAME(transaction_date)
ORDER BY 
    month_number;
```

![Screenshot 2024-05-16 132835](https://github.com/AbhinayBogala/Coffee_Shop_sales-SQL-PRoject/assets/168276269/a7ffb4c6-3957-4542-a530-e8d10b7bd995)
