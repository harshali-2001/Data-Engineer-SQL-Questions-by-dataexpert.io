
# Determining the Order of Succession [🔗](https://www.dataexpert.io/question/order-of-succession)
 
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
