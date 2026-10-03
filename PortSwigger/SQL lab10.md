# SQL Injection Lab 10

 Lab ka naam:SQL injection UNION attack, retrieving multiple values in a single column.
 Difficulty:PRACTITIONER.

# kya karna ha 

This lab contains a SQL injection vulnerability in the product category filter. The results from the query are returned in the application's response so you can use a UNION attack to retrieve data from other tables.

## Kya kiya

1. Use Burp Suite to intercept and modify the request that sets the product category filter.
2. Determine the number of columns that are being returned by the query and which columns contain text data. Verify that the query is returning two columns, only one of which contain text, using a payload like the following in the category parameter:

'+UNION+SELECT+NULL,'abc'--.
3. Use the following payload to retrieve the contents of the users table:

'+UNION+SELECT+NULL,username||'~'||password+FROM+users--.
4. Verify that the application's response contains usernames and passwords.

## Screenshot



