### PUNTO 1
CREATE VIEW FornitoriProdotti AS<br />
&ensp;&ensp;&ensp;SELECT Suppliers.CompanyName, Products.ProductName<br />
&ensp;&ensp;&ensp;FROM Suppliers, Products<br />
&ensp;&ensp;&ensp;WHERE Suppliers.SupplierID = Products.SupplierID;<br />

### PUNTO 2
CREATE VIEW Spedizioni(cliente, cittaResidenza, cittaSpedizione) AS<br />
&ensp;&ensp;&ensp;SELECT Customers.ContactName, Customers.City, Orders.ShipCity<br />
&ensp;&ensp;&ensp;FROM Customers, Orders<br />
&ensp;&ensp;&ensp;WHERE Customers.CustomerID = Orders.CustomerID;

SELECT DISTINCT cliente FROM Spedizioni<br />
&ensp;&ensp;&ensp;WHERE cittaResidenza <> cittaSpedizione<br />
&ensp;&ensp;&ensp;ORDER BY cliente;

### PUNTO 3
CREATE VIEW ProdottiPiuCariDellaMedia(nome, media) AS<br />
&ensp;&ensp;&ensp;SELECT ProductName, UnitPrice<br />
&ensp;&ensp;&ensp;FROM Products<br />
&ensp;&ensp;&ensp;WHERE UnitPrice > (SELECT AVG(UnitPrice) FROM Products);

### PUNTO 4
CREATE VIEW Fatture(ShipAddress, ShipCity, ShipCountry, ShipName, OrderDate, ShippedDate, ProductName, UnitPrice, Quantity, Discount, Amount) AS<br />
&ensp;&ensp;&ensp;SELECT Orders.ShipAddress, Orders.ShipCity, Orders.ShipCountry, Customers.CompanyName, Orders.OrderDate, Orders.ShippedDate, Products.ProductName, [Order Details].UnitPrice, [Order Details].Quantity, [Order Details].Discount, ([Order Details].UnitPrice - ([Order Details].UnitPrice * [Order Details].Discount)) * [Order Details].Quantity<br />
&ensp;&ensp;&ensp;FROM Orders, Products, [Order Details], Customers<br />
&ensp;&ensp;&ensp;WHERE Orders.OrderID = [Order Details].OrderID AND [Order Details].ProductID = Products.ProductID AND Customers.CustomerID = Orders.CustomerID;

