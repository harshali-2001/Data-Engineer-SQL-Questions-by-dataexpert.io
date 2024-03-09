
# Determining the Order of Succession [🔗](https://www.dataexpert.io/question/order-of-succession)

 Given a table Successors with columns: name, birthday, and gender, write a SQL query to list the names of the King's children in order of their succession to the throne and their birthday("name", "birthday"). Succession is based on age seniority. Prefix the name with "King" for males and "Queen" for females. The result should be sorted by birthday in ascending order to determine the succession order.

 
```` sql
SELECT
  CASE
    WHEN gender = 'M' THEN
      CASE
        WHEN name LIKE 'King%' THEN CONCAT('King ', SUBSTRING(name, LENGTH('King') + 1))
        ELSE CONCAT('King ', name)
      END
    WHEN gender = 'F' THEN
      CASE
        WHEN name LIKE 'Queen%' THEN CONCAT('Queen ', SUBSTRING(name, LENGTH('Queen') + 1))
        ELSE CONCAT('Queen ', name)
      END
  END AS name,
  birthday
FROM playground.successors
ORDER BY birthday ASC

````
