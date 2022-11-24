### PUNTO 1
CREATE VIEW FornitoriProdotti AS<br />
SELECT Suppliers.CompanyName, Products.ProductName<br />
&ensp;&ensp;&ensp;FROM Suppliers, Products<br />
&ensp;&ensp;&ensp;WHERE Suppliers.SupplierID = Products.SupplierID;<br />

### PUNTO 2
CREATE VIEW Spedizioni AS<br />
SELECT Customers.City, Orders.ShipCity<br />
&ensp;&ensp;&ensp;FROM Customers, Orders<br />
&ensp;&ensp;&ensp;WHERE Customers.CustomerID = Orders.CustomerID;

### PUNTO 3

