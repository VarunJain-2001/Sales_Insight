# India based Hardware company Sales Insight Dashboard using PowerBI and TableaU

## Problem statement

AtliQ hardware is a company which delivers computer hardware & peripheral 
Manufacturers to his clients, which has several branches throughout India. The sales director of the company is facing a lot of
issues in terms of understanding how the business is performing and what are all the problem company is
facing currently as the sales are not as expected and declining gradually. And whenever he calls the regional managers
to get the current status of the sales and market, as a human behaviour, these people 
Humans are not comfortable in consuming numbers from excel files, which is obvious reason for the frustration.

## Solution

Sales director of the AltiQ hardware, decided to build a PowerBI Dashboard for converting the data into 
visual representation to make data driven decisions. So, he hired a team of data people to complete this task.

### AIMS Grid

----
By using the AIMS grid project management tool, we made sure what are the purpose, stakeholder, end result 
and success criteria  of our project.

<img src ="https://github.com/VarunJain-2001/Sales_Insight/blob/main/Images/aims_grid.png">

### Data Analysis - Approach
<p  align="center"><a href="https://github.com/VarunJain-2001"><img width="80%" src="https://github.com/VarunJain-2001/Sales_Insight/blob/main/Images/flowChart.jpg" /></a></p>

### Data Analysis - Model Schema
<p  align="center"><a href="https://github.com/VarunJain-2001"><img width="80%" src="https://github.com/VarunJain-2001/Sales_Insight/blob/main/Images/model_schema.png" /></a></p>

## Technologies used ⚙️

* <a href="https://coursera.org/share/064db4645159df788ad0b31abebf1556">Advance Excel</a><a href="https://coursera.org/share/064db4645159df788ad0b31abebf1556" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/mrankitgupta/66DaysOfData/60139fb461ef56a19afd68ea4094f6069f27ce49/icons8-microsoft-excel%20(1).svg" alt="excel" width="25" height="25"/> </a>

* <a href="https://www.mysql.com/">MySQL</a><a href="https://www.mysql.com/" target="_blank"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/mysql/mysql-original-wordmark.svg" alt="mysql" width="35" height="20"/> </a>   |  <a href="https://www.microsoft.com/en-us/sql-server">SQL Server</a><a href="https://www.microsoft.com/en-us/sql-server" target="_blank" rel="noreferrer"> <a href="https://www.microsoft.com/en-us/sql-server" target="_blank"> <img src="https://www.svgrepo.com/show/303229/microsoft-sql-server-logo.svg" alt="sql-server" width="28" height="22"/> </a> 

* <a href="https://public.tableau.com/app/profile/mrankitgupta">Tableau</a><a href="https://public.tableau.com/app/profile/mrankitgupta" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/mrankitgupta/mrankitgupta/a768d6bf0a001f03327578ae12f8867e4056cbaf/tableau-software.svg" alt="tableau" width="20" height="20"/> </a>  |
<a href="https://powerbi.microsoft.com/en-us/">Power BI</a><a href="https://powerbi.microsoft.com/en-us/" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/mrankitgupta/mrankitgupta/a768d6bf0a001f03327578ae12f8867e4056cbaf/power-bi.svg" alt="powerbi" width="20" height="20"/> </a>

* <a href="https://github.com/mrankitgupta/Statistics-for-Data-Science-using-Python">Statistics</a><a href="https://github.com/mrankitgupta/Statistics-for-Data-Science-using-Python" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/mrankitgupta/66DaysOfData/c8c040f1c85d921db317152567f331354446286a/statistics-21.svg" alt="Statistics" width="25" height="25"/> </a>


## Steps Followed in this project

<!-- 1. Learned about AIMS grid for project planning.
2. Used MySQL for retrieving the data from the database into Power BI.
3. Data Cleaning in power query.
4. Performed ETL process (Extract Transform and Load)
5. Created measure for needs and used them for creating visuals in PowerBi.
6. In the currency there were two types of currencies in transactions, performed currency conversion to make all the currency type same
7. Data Validation
8. Data Modelling and Visualization.
 -->

**Step 1: Data Acquisition**
- Download the data file from the provided links: [db_dump.sql](https://github.com/VarunJain-2001/Sales_Insight/blob/main/db_dump.sql)

**Step 2: Data Preparation**
- If using MySQL, import the downloaded file (`db_dump.sql`) into your MySQL database.
- Perform necessary ETL (Extract, Transform, Load) operations to clean and structure the data as needed. This may include removing duplicates, handling missing values, and transforming data types.

**Step 3: Data Analysis Tools Setup**
- Download and install [Tableau Public](https://www.tableau.com/products/public/download)
- Download and install [Power BI Desktop](https://powerbi.microsoft.com/en-us/downloads/)

**Step 4: Data Connection**
- Connect Tableau and PowerBI to your MySQL database or Excel file where you've loaded the data.

**Step 5: Data Analysis in Tableau**
- Perform data analysis in Tableau and PowerBI. Create visualizations, measures, and dashboards to explore and analyze the data.
- Utilize the AIMS grid principles for project planning as needed during the analysis.

**Step 6: Currency Conversion (if applicable)**
- If the data includes multiple currencies in transactions, perform currency conversion to standardize them to a common currency.

**Step 7: Data Validation**
- Ensure the data is accurate and validated. Double-check calculations, aggregations, and visualizations for correctness.

**Step 8: Data Modeling and Visualization**
- Continue building data models and visualizations in Tableau and PowerBI to address the analysis goals.
- Use MySQL or Excel data as a source to create calculated fields and further refine the visualizations.

**Step 9: Save**
- Save Tableau project file (.twb or .twbx) and PowerBI project file (.pbix) to preserve your analysis and visualization work.

By following these steps, you can effectively plan, prepare, and perform data analysis using Tableau, MySQL, and Power BI, combining the elements of data cleaning, ETL, visualization, and validation into a structured workflow.


## Data Analysis Using SQL
  
1. Show all customer records

    `SELECT * FROM customers;`

1. Show total number of customers

    `SELECT count(*) FROM customers;`

1. Show transactions for Chennai market (market code for chennai is Mark001)

    `SELECT * FROM transactions where market_code='Mark001';`

1. Show distrinct product codes that were sold in chennai.

    `SELECT distinct product_code FROM transactions where market_code='Mark001';`

1. Show transactions where currency is US dollars.

    `SELECT * from transactions where currency="USD"`

1. Show transactions in 2020 join by date table.

    `SELECT transactions.*, date.* FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020;`

1. Show total revenue in year 2020.

    `SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and transactions.currency="INR\r" or transactions.currency="USD\r";`
	
1. Show total revenue in year 2020, January Month.

    `SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and and date.month_name="January" and (transactions.currency="INR\r" or transactions.currency="USD\r");`

1. Show total revenue in year 2020 in Chennai.

    `SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020and transactions.market_code="Mark001";`


## Major Changes/ Customizations Made

1.Solved the ‘(blank)’ problem for the products section by deleting the original products table and adding the self-modified products table where I have added the Products ranging from Prod280 to Prod339 with their product type (random type- b/w ‘Own Brand’ and ‘Distribution’).
2.Merged the original modified ‘sales_transaction’ table with the new ‘sales_transaction’ table having profit margin, cost price, etc.

###  Insights
  
1. In this dashboard, we can see company has generated total revenue in 4 years ₹ 985M, total profit margin ₹24.7M, Profit margin% 2.5%, Sales Qty ₹2M.
   in 2020 company has generated total revenue of ₹ 142M by selling a total of 350K and earned a profit of ₹ 2.1M.
2. In 4 years Delhi NCR is our largest market in terms of revenue with ₹ 520M and total contribution of 52.8% with total revenue but if you look at the profit            margin Delhi NCR is generating only 2.3% profit margin.
3. If we check the profit margin then here In 2020 Bhubaneshwar comes into the picture which is generating the highest profit margin of 10.48%. Similarly, if we can      check the Profit Contribution % by Market then here Mumbai is the largest player with 23.89% of total contribution in total profit.
4. In 4 years Bengaluru generating the lowest profit margin of -20.8%.if we can check the Profit Contribution % by Market then here also Bengaluru is the Lower with      -0.3% of total contribution in total profit.
5. In our top 5 customers, the Electricalsara Stores is our biggest customer who has generated total ₹ 413 M revenue generated in 4 years.
6. In our top 5 products,the Prod318 is our highest product has generated total  ₹ 69M revenue generated in 4 years.
7. In product type Distribution has generated the revenue of ₹494M and ownbrand revenue is ₹494M generated in entire 4 years.
7. Revenue Trend is showing that in June 2020 revenue has been decreased drastically compared to the revenue last year and the profit margin was the least in              April 2020.
  
### Key Learnings

1. Learned about what real business data sets look like.
2. Learned about how to write some major analysis queries in MySQL.
3. how to connect the database’s tables to Power Bi and how to clean & modify the unwanted data in Power Query.
4. Learned about some major practical DAX functions and measures.
5. Learned about some major analytical visuals and reports.


## Final result 

#### Dashboard KPI Page

-------
 <img src="https://github.com/NotRamm/Sales-Insight-Dashboard-using-Power-BI/blob/master/Screenshots/Sales%20Insight%20-%20Page%20KPI.png" class="center">
 
 #### Dashboard Performance Insights

-------
 <img src="https://github.com/NotRamm/Sales-Insight-Dashboard-using-Power-BI/blob/master/Screenshots/Sales%20Insight%20-%20Page%20Performance%20Insights.png" class="center">
 

 #### Dashboard Profit Analysis
 
 -----------
 
  <img src="https://github.com/NotRamm/Sales-Insight-Dashboard-using-Power-BI/blob/master/Screenshots/Sales%20Insight%20-%20Page%20Profit%20Analysis.png" class="center">

 #### Sales Dashboard
 
 -----------
 
  <img src="https://github.com/VarunJain-2001/Sales_Insight/blob/main/Data%20Visualization/Tableau/Sales/salesDashboard.png" class="center">

 #### Profit Dashboard
 
 -----------
 
  <img src="https://github.com/VarunJain-2001/Sales_Insight/blob/main/Data%20Visualization/Tableau/Profit/profitDashboard.png" class="center">






