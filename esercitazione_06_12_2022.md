### PUNTO 1
SELECT Customers.cust_name, Customers.city, Orders.ord_no, Orders.ord_date, Orders.purch_amt<br />
FROM Customers LEFT JOIN Orders ON Customers.customer_id = Orders.customer_id<br />
ORDER BY ord_date;
