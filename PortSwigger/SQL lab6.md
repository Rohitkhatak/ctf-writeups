# SQL Injection Lab 6

 Lab ka naam: SQL injection attack, listing the database contents on Oracle.
 Difficulty: APPRENTICE

# kya karna ha 

This lab contains a SQL injection vulnerability in the product category filter. The results from the query are returned in the application's response so you can use a UNION attack to retrieve data from other tables.

## Kya kiya

1. Use Burp Suite to intercept and modify the request that sets the product category filter.
2. Determine the number of columns that are being returned by the query and which columns contain text data. Verify that the query is returning two columns, both of which contain text, using a payload like the following in the category parameter:

'+UNION+SELECT+'abc','def'+FROM+dual--.
3. Use the following payload to retrieve the list of tables in the database:

'+UNION+SELECT+table_name,NULL+FROM+all_tables--.
4. Find the name of the table containing user credentials.
5. Use the following payload (replacing the table name) to retrieve the details of the columns in the table:

'+UNION+SELECT+column_name,NULL+FROM+all_tab_columns+WHERE+table_name='USERS_ABCDEF'--.
6. Find the names of the columns containing usernames and passwords.
7. Use the following payload (replacing the table and column names) to retrieve the usernames and passwords for all users:

'+UNION+SELECT+USERNAME_ABCDEF,+PASSWORD_ABCDEF+FROM+USERS_ABCDEF--.
8. Find the password for the administrator user, and use it to log in.

## Result

To solve the lab, log in as the administrator user.

## Screenshot
<img width="1545" height="893" alt="Screenshot 2026-09-27 142656" src="https://github.com/user-attachments/assets/fedd7858-a7b2-4d90-81dd-53dd075b372c" />

<img width="1545" height="893" alt="image" src="https://github.com/user-attachments/assets/a90fcb05-b2a1-42a0-828b-73dba09aca05" />
