# Sales_Analysis-Project-with-SQL-Tableau

ATLIQ-Sales-Insight : Data-Analysis-using-SQL-and-TABLEAU

SALES INSIGHTS PROJECT-
* PROBLEM STATEMENT
* PROJECT PLANNING AND APPROACH
* MY APPROACH FOR THIS PROJECT
* DASHBOARD
* Conclusion

  ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  
* PROBLEM STATEMENT-
AtliQ Hardware is a hardware company which supplies hardware peripherals to different clients such as Normad stores, Excel stores, and Surge stores.
The sales director of this company is facing a lot of challenges because the market is growing dynamically and sales director is facing issues in terms of tracking the sales in this dynamic growth market and he is having issues with the growth of this business as overall sales was declining. He is the regional manager for North India, South and Central India. Whenever he wanted to get insights into these regions, he would call these people and on the phone, the regional manager gave some insights to him that this was the sales last quarter and we are going to grow by this much in the next quarter.
As the overall sales were declining, he wanted a simple data visualization tool that he can access daily. By using such tools and technology one can make data-driven decisions which helps to increase the sales of the company. So, In this project, we will help a company make its own sales-related dashboard using Tableau.

* PROJECT PLANNING AND APPROACH
    •	Performed Data Cleaning, Analysis and Visualization on India-based hardware company sales insights.
    •	Developed ETL mappings using SQL to extract the data from unstructured data and transformed it to the staging area to conduct data cleaning and design a star schema data model on Tableau.
    •	Developed a Tableau dashboard to perform analysis, creating visualizations in Tableau to draw valuable insights based on different parameters affecting the company's performance year on year and further provide business solutions.

* MY APPROACH FOR THIS PROJECT
  
Setup Process:

•	Step 1: Download file: db_dump.sql or db_dump.xlsx.

•	Step 2: Import it in MySql do ETL(Extract, Transform, Load) if required.

•	Step 3: Download Tableau Public (Free) or Tableau Desktop (14 days trial) to perform Data Analysis.

•	Step 4: Connect Tableau with MySql database or Excel database.

•	Step 5: Save the file as (.twb or .twbx).

DATA ANALYSIS USING SQL:
• Show all customer records
           
           SELECT * FROM customers;

• Show total number of customers
           
           SELECT count(*) FROM customers;

• Show transactions for Chennai market (market code for chennai is Mark001)
           
           SELECT * FROM transactions where market_code='Mark001';

• Show distrinct product codes that were sold in chennai.
           
           SELECT distinct product_code FROM transactions where market_code='Mark001';

• Show transactions where currency is US dollars.
           
           SELECT * from transactions where currency="USD"

• Show transactions in 2020 join by date table.
           
           SELECT transactions., date. FROM transactions INNER JOIN date ON 
           transactions.order_date=date.date where date.year=2020;

• Show total revenue in year 2020.
           
           SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date 
           where date.year=2020 and transactions.currency="INR\r" or transactions.currency="USD\r";

• Show total revenue in year 2020, January Month.
    
           SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date 
           where date.year=2020 and and date.month_name="January" and (transactions.currency="INR\r" or transactions.currency="USD\r");


DATA ANALYSIS USING TABLEAU:
Tableau Public Dashboards: Revenue & Profit Analysis Tableau Creating Star Schema in Tableau
![image](https://github.com/Diksha-06/Sales_Analysis-Project-with-SQL-Tableau/assets/105701051/8cd3e0b4-c908-4193-b507-d7388f2575b2)

* TABLEAU DASHBOARD: REVENUE ANALYSIS

![image](https://github.com/Diksha-06/Sales_Analysis-Project-with-SQL-Tableau/assets/105701051/5175ff37-6b85-4756-aeca-99e81f16d15c)


* TABLEAU DASHBOARD: PROFIT ANALYSIS
  ![image](https://github.com/Diksha-06/Sales_Analysis-Project-with-SQL-Tableau/assets/105701051/4c8294eb-cc63-4c43-bc35-1085181297f0)

* Conclusion-

- Should Maintain healthy relationships with the customers in Bhubaneshwar, Hyderabad, and Chennai as they have the highest profit % by market.
- Make some strategy for the Bengaluru market as its revenue is less and also profit margin is negative.
- Kanpur is having negative profit margin. We can give KPIs to the regional manager to  maintain good margins in orders & work closely on negotiation with the sales team.
- Create more marketing activities/campaigns in Bengaluru to increase the customer database & that will increase revenue also.

* References-
Project Inspiration: @codebasics YouTube channel.

  
