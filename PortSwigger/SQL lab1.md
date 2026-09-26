# SQL Injection Lab 1

Lab ka naam: SQL injection vulnerability in WHERE clause allowing retrieval of hidden data
Difficulty: APPRENTICE

## Kya kiya
Use Burp Suite to intercept and modify the request that sets the product category filter.
Modify the category parameter, giving it the value '+OR+1=1--
Submit the request, and verify that the response now contains one or more unreleased products.

## Result
To solve the lab, perform a SQL injection attack that causes the application to display one or more unreleased products.

## Screenshot

<img width="943" height="521" alt="Screenshot 2026-09-26 140844" src="https://github.com/user-attachments/assets/18624e03-d97e-402c-8282-dae52c5a3743" />
