### PUNTO 1
CREATE VIEW FornitoriProdotti AS<br />
SELECT Suppliers.CompanyName, Products.ProductName<br />
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

