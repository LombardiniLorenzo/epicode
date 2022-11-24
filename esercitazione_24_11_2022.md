### PUNTO 1
CREATE VIEW FornitoriProdotti AS<br />
SELECT Suppliers.CompanyName, Products.ProductName<br />
FROM Suppliers, Products<br />
WHERE Suppliers.SupplierID = Products.SupplierID;<br />
