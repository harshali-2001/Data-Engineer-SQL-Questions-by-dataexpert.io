# Find Viewers with Multiple Article Views in a Day [link] (https://www.dataexpert.io/question/find-multiple-article-viewers)

Using the table playground.views, write a SQL query to identify all viewers who viewed more than one article on the same day. The table includes columns viewer_id (the ID of the viewer), article_id (the ID of the article viewed), and view_date (the date of the view). The result should contain a single column named viewer_id, listing each viewer who meets the criteria without duplicates, and should be sorted in ascending order of viewer_id.

These are the tables for this question:

```` sql
with solution as
(
SELECT
    viewer_id,
    view_date,
    COUNT(DISTINCT article_id) AS articles_count
  FROM 
    playground.views
  GROUP BY viewer_id, view_date
)
select viewer_id
from solution
where articles_count >1
order by viewer_id
````
