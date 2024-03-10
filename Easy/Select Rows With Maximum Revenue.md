# Select Rows With Maximum Revenue [🔗](https://dataexpert.io/question/select-max-revenue-rows)

Using the table playground.revenue, write a SQL query to select rows from a given table that have the maximum revenue value for each id. The resultant table should have three columns - "id", "rev", "content". Additionally, the results should be ordered in descending order by revenue.

```` sql
Select s.customer_id , sum( m.price) as Money_Spend
FROM SALES AS S
JOIN MENU AS M
on s.product_id = m.product_id
GROUP BY s.customer_id;
````
