Link report:
https://datastudio.google.com/reporting/bf3ba436-6747-4932-a1de-b82c2391d25c


### PUNTO 1
SELECT Customers.cust_name, Customers.city, Orders.ord_no, Orders.ord_date, Orders.purch_amt<br />
FROM Customers LEFT JOIN Orders ON Customers.customer_id = Orders.customer_id<br />
ORDER BY ord_date;

### PUNTO 2
CREATE VIEW vista_clienti('data','n_clienti', 'avg_acquisti', 'tot_acquisti') AS<br />
SELECT Orders.ord_date, count(DISTINCT(Orders.customer_id)), avg(Orders.purch_amt), sum(Orders.purch_amt)<br />
FROM Orders<br />
GROUP BY Orders.ord_date;
