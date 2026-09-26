# SQL Injection Lab 1

 Lab ka naam:SQL injection attack, querying the database type and version on MySQL and Microsoft.
 Difficulty: APPRENTICE

## Kya kiya
1. Use Burp Suite to intercept and modify the request that sets the product category filter.
2. Determine the number of columns that are being returned by the query and which columns contain text data. Verify that the query is returning two columns, both of which contain text, using a payload like the following in the category parameter:

'+UNION+SELECT+'abc','def'#.
3. Use the following payload to display the database version:

'+UNION+SELECT+@@version,+NULL#.

## Result
To solve the lab, perform a SQL injection attack that causes the application to display one or more unreleased products.

## Screenshot

<img width="943" height="521" alt="Screenshot 2026-09-26 140844" src="https://github.com/user-attachments/assets/18624e03-d97e-402c-8282-dae52c5a3743" />
