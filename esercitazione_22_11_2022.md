### PUNTO 1
SELECT orders.OrderID, customers.ContactName, customers.ContactTitle<br />
&ensp;&ensp;&ensp;FROM orders<br />
&ensp;&ensp;&ensp;INNER JOIN customers ON orders.CustomerID = customers.CustomerID;

### PUNTO 2
SELECT orders.OrderID, employees.FirstName, employees.LastName<br />
&ensp;&ensp;&ensp;FROM orders<br />
&ensp;&ensp;&ensp;LEFT JOIN employees ON orders.EmployeeID = employees.EmployeeID;

### PUNTO 3
SELECT City FROM suppliers<br />
UNION<br />
SELECT ShipCity FROM orders;

### PUNTO 4
SELECT City FROM suppliers<br />
EXCEPT<br />
SELECT ShipCity FROM orders;

### PUNTO 5
SELECT products.ProductName, products.UnitPrice, categories.CategoryName<br />
&ensp;&ensp;&ensp;FROM products<br />
&ensp;&ensp;&ensp;INNER JOIN categories ON products.CategoryID = categories.CategoryID;
