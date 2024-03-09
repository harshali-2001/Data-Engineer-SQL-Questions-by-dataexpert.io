# Customers with More Than 25 Orders 🔗[https://www.dataexpert.io/question/loyal-customers]

```` sql
SELECT customer_id
, customer_name
, count(order_id) as order_count
 FROM playground.superstore
group by customer_id , customer_name
having count(order_id) >20
order by 3 desc , 2 asc
````
