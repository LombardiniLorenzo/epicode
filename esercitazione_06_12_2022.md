### PUNTO 1
SELECT Customers.cust_name, Customers.city, Orders.ord_no, Orders.ord_date, Orders.purch_amt<br />
FROM Customers LEFT JOIN Orders ON Customers.customer_id = Orders.customer_id<br />
ORDER BY ord_date;

### PUNTO 2
CREATE VIEW vista_clienti('data','n_clienti', 'avg_acquisti', 'tot_acquisti') AS<br />
SELECT Orders.ord_date, count(Customers.customer_id), avg(Orders.purch_amt), count(Orders.ord_no)<br />
FROM Customers, Orders<br />
WHERE Customers.customer_id = Orders.customer_id<br />
GROUP BY Orders.ord_date;
