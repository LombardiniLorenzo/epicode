### PUNTO 1
CREATE VIEW FornitoriProdotti AS<br />
SELECT Suppliers.CompanyName, Products.ProductName<br />
&ensp;&ensp;&ensp;FROM Suppliers, Products<br />
&ensp;&ensp;&ensp;WHERE Suppliers.SupplierID = Products.SupplierID;<br />

### PUNTO 2
