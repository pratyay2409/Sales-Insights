# Sales-Insights

### Data Analysis Using SQL
1. Show all customer records
    `SELECT * FROM customers;`
2. Show total number of customers
    `SELECT count(*) FROM customers;`
3. Show transactions for Chennai market (market code for chennai is Mark001
    `SELECT * FROM transactions where market_code='Mark001';`
4. Show distrinct product codes that were sold in chennai
    `SELECT distinct product_code FROM transactions where market_code='Mark001';`
5. Show transactions where currency is US dollars
    `SELECT * from transactions where currency="USD"`
6. Show transactions in 2020 join by date table
    `SELECT transactions.*, date.* FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020;`
6. Show total revenue in year 2020,
    `SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and transactions.currency="INR\r" or transactions.currency="USD\r";`
7. Show total revenue in year 2020, January Month,
    `SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and and date.month_name="January" and (transactions.currency="INR\r" or transactions.currency="USD\r");`
8. Show total revenue in year 2020 in Chennai
    `SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and transactions.market_code="Mark001";`

### Power BI Dashboard
![Screenshot (435)](https://github.com/pratyay2409/Sales-Insights/assets/92170433/d1177d72-ae58-454e-aebc-1140b2ace785)
![Screenshot (436)](https://github.com/pratyay2409/Sales-Insights/assets/92170433/84c4061a-686e-44bd-ac04-740561629c8e)
![Screenshot (437)](https://github.com/pratyay2409/Sales-Insights/assets/92170433/914adbe7-b0b1-414d-b1ca-bf6eaf573848)

### Database Schema
![Screenshot (438)](https://github.com/pratyay2409/Sales-Insights/assets/92170433/0a718413-fa6d-47f6-b20e-2d3218bfe7f1)
