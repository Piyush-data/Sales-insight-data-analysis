# Sales-insight-data-analysis
Project for real life use case of predicting sales insights for a hardware supplier company.
# Tools : <br />
Excel , MySQL & Tableau <br />
 ![Screenshot (40)](https://user-images.githubusercontent.com/85888663/216770394-185f9219-210a-4c46-a858-8d508107544f.png)
![Screenshot (41)](https://user-images.githubusercontent.com/85888663/216770396-84597fa8-6ced-4535-96b9-f1f643af100e.png)

 # Works 
Connected MySQL database to Tableau <br />
Make Tableau relationship <br /> 
# calculated fields
  IF[currency]=='USD' THEN [Sales Amount]*74 <br />
  ELSE[Sales Amount] END <br/>
### Data Analysis Using SQL

1. Show all customer records

    `SELECT * FROM customers;`

1. Show total number of customers

    `SELECT count(*) FROM customers;`

1. Show transactions for Chennai market (market code for chennai is Mark001

    `SELECT * FROM transactions where market_code='Mark001';`

1. Show distrinct product codes that were sold in chennai

    `SELECT distinct product_code FROM transactions where market_code='Mark001';`

1. Show transactions where currency is US dollars

    `SELECT * from transactions where currency="USD"`

1. Show transactions in 2020 join by date table

    `SELECT transactions.*, date.* FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020;`

1. Show total revenue in year 2020,

    `SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and transactions.currency="INR\r" or transactions.currency="USD\r";`
	
1. Show total revenue in year 2020, January Month,

    `SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and and date.month_name="January" and (transactions.currency="INR\r" or transactions.currency="USD\r");`

1. Show total revenue in year 2020 in Chennai

    `SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020
and transactions.market_code="Mark001";`

