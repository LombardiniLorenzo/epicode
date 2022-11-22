### PUNTO 1
SELECT orders.OrderID, customers.ContactName, customers.ContactTitle<br />
FROM orders<br />
INNER JOIN customers ON orders.CustomerID = customers.CustomerID;

