# TableauProject
All my TableauProjects
View all my Tableau-Projects Dashboards on my Tableau Public Profile link -
https://github.com/priya1100/TableauProjects
## Project-1 Sales insights
### step 1: Data Analysis using mysql
-- Show total number of customers
<pre>
SELECT * FROM customers;
</pre>
-- Show total count of customers
<pre>
SELECT count(*) FROM customers;
</pre>
--Show transactions for Chennai market (market code for chennai is Mark001
<pre>
SELECT * FROM transactions where market_code='Mark001';
</pre>
-- Show distrinct product codes that were sold in chennai
<pre>
SELECT distinct product_code FROM transactions where market_code='Mark001';
</pre>
--Show transactions where currency is US dollars
<pre>
SELECT * from transactions where currency="USD"
</pre>
-- Show transactions in 2020 join by date table
<pre>
SELECT transactions.*, date.* FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020;
</pre>
-- Show total revenue in year 2020,
<pre>
SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and transactions.currency="INR\r" or transactions.currency="USD\r";
</pre>
-- Show total revenue in year 2020, January Month,
<pre>
SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and and date.month_name="January" and (transactions.currency="INR\r" or transactions.currency="USD\r");
</pre>
-- Show total revenue in year 2020 in Chennai
<pre>
SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and transactions.market_code="Mark001";
</pre>
### step-2:Data Visualization using Tableau
<image src="sales_project_finalresult.png">
