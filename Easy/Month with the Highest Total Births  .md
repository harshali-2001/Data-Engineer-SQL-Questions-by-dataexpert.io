# Month with the Highest Total Births [link](https://www.dataexpert.io/question/highest-birth-month)

Determine the month with the highest total number of births in the playground.us_birth_stats table. The output should show the month and the total number of births.


```` sql
SELECT
   month
  ,sum(births) as total_births
FROM playground.us_birth_stats
group by 1 
order by 2 desc
limit 1

````
 
