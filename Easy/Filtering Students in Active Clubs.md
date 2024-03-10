# Filtering Students in Active Clubs [🔗](https://dataexpert.io/question/active-club-members)
 Given tables clubs (id: unique club id, name: club name) and students (id: unique student id, name: student name, club_id: club's id), return a list from the students table for those who are in clubs that still exist in the clubs table. The result should have three columns (id, name, club_id) and be sorted by students' ids (id) and include only those students whose club_id matches an id in the clubs table.


 ```` sql
Select s.customer_id , sum( m.price) as Money_Spend
FROM SALES AS S
JOIN MENU AS M
on s.product_id = m.product_id
GROUP BY s.customer_id;
````
