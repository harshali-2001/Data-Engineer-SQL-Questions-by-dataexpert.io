# Total Number of Births Per Year [link](https://www.dataexpert.io/question/total-births-per-year)
Write a SQL query to calculate the total number of births recorded for each year in the playground.us_birth_stats table. Order the results by year.

```` sql
SELECT year
, sum(births) as total_births
FROM playground.us_birth_stats
group by 1
order by 1
````
