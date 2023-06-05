# Using SQL Case , Cross Join , full outer join:-
### 1.SQL query using CASE:-
```sql
SELECT customer_name, order_date,
  CASE
    WHEN order_total >= 1000 THEN 'High'
    WHEN order_total >= 500 THEN 'Medium'
    ELSE 'Low'
  END AS order_priority
FROM Orders;

```
### 2.SQL query using CROSS JOIN:-
```sql
SELECT Customers.customer_name, Orders.order_number
FROM Customers
CROSS JOIN Orders;

```
### 3.SQL query using INNER JOIN:-
```sql
SELECT Customers.customer_name, Orders.order_number
FROM Customers
INNER JOIN Orders ON Customers.customer_id = Orders.customer_id;

```
### 4.SQL query using FULL OUTER JOIN:-
```sql
SELECT Customers.customer_name, Orders.order_number
FROM Customers
FULL OUTER JOIN Orders ON Customers.customer_id = Orders.customer_id;

```