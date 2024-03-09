# Customers with More Than 25 Orders 🔗[https://www.dataexpert.io/question/loyal-customers]

Write a SQL query to display all loyal customers from the playground.superstore table. A customer is considered loyal if they have placed more than 20 orders. The query should return the customer ID, customer name, and the total number of orders for each of these customers. Display the result in descending order of their orders and then ascending order of their names

```` sql
SELECT customer_id
, customer_name
, count(order_id) as order_count
 FROM playground.superstore
group by customer_id , customer_name
having count(order_id) >20
order by 3 desc , 2 asc
````
