# SQL Injection Lab 7

 Lab ka naam:SQL injection UNION attack, determining the number of columns returned by the query.
 Difficulty:PRACTITIONER

# kya karna ha 

This lab contains a SQL injection vulnerability in the product category filter. The results from the query are returned in the application's response, so you can use a UNION attack to retrieve data from other tables. The first step of such an attack is to determine the number of columns that are being returned by the query. You will then use this technique in subsequent labs to construct the full attack.

## Kya kiya

1. Use Burp Suite to intercept and modify the request that sets the product category filter.
2. Modify the category parameter, giving it the value '+UNION+SELECT+NULL--. Observe that an error occurs.
3. Modify the category parameter to add an additional column containing a null value:

'+UNION+SELECT+NULL,NULL--.
4. Continue adding null values until the error disappears and the response includes additional content containing the null values.


## Result

To solve the lab, determine the number of columns returned by the query by performing a SQL injection UNION attack that returns an additional row containing null values.

## Screenshot
<img width="1821" height="944" alt="Screenshot 2026-09-27 150214" src="https://github.com/user-attachments/assets/b4a5d223-e9ce-4b20-9813-85281b3abace" />

<img width="1871" height="968" alt="Screenshot 2026-09-27 150157" src="https://github.com/user-attachments/assets/c8ede02c-eb09-4cad-986e-38a8bbeb8541" />

