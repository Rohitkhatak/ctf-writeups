# SQL Injection Lab 7

 Lab ka naam:
 Difficulty:PRACTITIONER

# kya karna ha 
The lab will provide a random value that you need to make appear within the query results. To solve the lab, perform a SQL injection UNION attack that returns an additional row containing the value provided. This technique helps you determine which columns are compatible with string data.

## Kya kiya

1. Use Burp Suite to intercept and modify the request that sets the product category filter.
2. Determine the number of columns that are being returned by the query. Verify that the query is returning three columns, using the following payload in the category parameter:

'+UNION+SELECT+NULL,NULL,NULL--.
3. Try replacing each null with the random value provided by the lab, for example:

'+UNION+SELECT+'abcdef',NULL,NULL--.
4. If an error occurs, move on to the next null and try that instead.

## Screenshot


