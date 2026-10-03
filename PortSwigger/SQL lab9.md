# SQL Injection Lab 9

 Lab ka naam: SQL injection UNION attack, retrieving data from other tables.
 Difficulty:PRACTITIONER.

# kya karna ha 

This lab contains a SQL injection vulnerability in the product category filter. The results from the query are returned in the application's response, so you can use a UNION attack to retrieve data from other tables. To construct such an attack, you need to combine some of the techniques you learned in previous labs.

## Kya kiya

1. Use Burp Suite to intercept and modify the request that sets the product category filter.
2. Determine the number of columns that are being returned by the query and which columns contain text data. Verify that the query is returning two columns, both of which contain text, using a payload like the following in the category parameter:

'+UNION+SELECT+'abc','def'--.
3. Use the following payload to retrieve the contents of the users table:

'+UNION+SELECT+username,+password+FROM+users--.
4. Verify that the application's response contains usernames and passwords.

## Screenshot

<img width="635" height="352" alt="Screenshot 2026-10-03 135820" src="https://github.com/user-attachments/assets/59433cc5-302f-486c-8fed-c713bce9598f" />
<img width="1886" height="954" alt="Screenshot 2026-10-03 135908" src="https://github.com/user-attachments/assets/6c8aa3cc-50ce-4f57-a209-48cbe013062e" />




