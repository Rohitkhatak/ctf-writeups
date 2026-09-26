# SQL Injection Lab 1

 Lab ka naam:SQL injection attack, querying the database type and version on MySQL and Microsoft.
 Difficulty: APPRENTICE

# kya karna ha 

This lab contains a SQL injection vulnerability in the product category filter. You can use a UNION attack to retrieve the results from an injected query.

To solve the lab, display the database version string.

## Kya kiya
1. Use Burp Suite to intercept and modify the request that sets the product category filter.
2. Determine the number of columns that are being returned by the query and which columns contain text data. Verify that the query is returning two columns, both of which contain text, using a payload like the following in the category parameter:

'+UNION+SELECT+'abc','def'#.
3. Use the following payload to display the database version:

'+UNION+SELECT+@@version,+NULL#.

## Result

You can find some useful payloads on our SQL injection cheat sheet.

## Screenshot

<img width="1911" height="1058" alt="Screenshot 2026-09-26 162923" src="https://github.com/user-attachments/assets/9127bc4b-6477-440b-aa0b-a9418e19db3d" />
<img width="1898" height="1079" alt="Screenshot 2026-09-26 162859" src="https://github.com/user-attachments/assets/15a5733e-5792-47f9-b60d-03f8d2190766" />
