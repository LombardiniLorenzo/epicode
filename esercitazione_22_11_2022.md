### PUNTO 1
SELECT orders.OrderID, customers.ContactName, customers.ContactTitle<br />
&ensp;&ensp;&ensp;FROM orders<br />
&ensp;&ensp;&ensp;INNER JOIN customers ON orders.CustomerID = customers.CustomerID;

