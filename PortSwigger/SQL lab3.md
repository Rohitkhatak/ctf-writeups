# SQL Injection Lab 3

 Lab ka naam: SQL injection attack, querying the database type and version on Oracle.       
 Difficulty: PRACTITIONER

## Kya kiya
1. Use Burp Suite to intercept and modify the request that sets the product category filter.
2. Determine the number of columns that are being returned by the query and which columns contain text data. Verify that the query is returning two columns, both of which contain text, using a payload like the following in the category parameter:
'+UNION+SELECT+'abc','def'+FROM+dual--.

3. Use the following payload to display the database version:
'+UNION+SELECT+BANNER,+NULL+FROM+v$version--

## Result
To solve the lab, display the database version string.

## Screenshot
<img width="1879" height="1068" alt="Screenshot 2026-09-26 160224" src="https://github.com/user-attachments/assets/5fe29acf-39ee-4189-b123-a83ba6745095" />
<img width="1879" height="1068" alt="Screenshot 2026-09-26 160224" src="https://github.com/user-attachments/assets/0f840119-854a-4ca5-867b-ca413e82eb97" />
