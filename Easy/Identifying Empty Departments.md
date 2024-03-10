# Identifying Empty Departments [🔗](https://dataexpert.io/question/empty-departments-list)

Given two tables, playground.employees and playground.departments, with employees containing id, full_name, and department, and departments containing id (unique department ID) and dep_name (department name), write a SQL query to build a table with one column, dep_name. This table should list all the departments that currently have no employees, sorted by the department id.

These are the tables for this question:

```` sql
SELECT dp.dep_name
FROM playground.departments AS dp
LEFT JOIN playground.employees AS ep
 ON dp.id = ep.department
WHERE ep.department IS NULL
````
 
