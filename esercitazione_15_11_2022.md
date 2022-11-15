### Punto 1
SELECT BillingCity, BillingCountry, Total FROM invoices<br />
WHERE BillingCountry = 'Canada' AND Total < 4;

### Punto 2
SELECT Name, Composer FROM Tracks<br />
WHERE Name LIKE '%Dog%';

### Punto 3
SELECT FirstName, LastName, Country FROM Customers;

SELECT FirstName, LastName, Country FROM Customers<br />
WHERE Country = 'Brazil' AND LastName LIKE 'R%';

### Punto 4
SELECT * FROM invoices<br />
WHERE Total > 8 OR Total < 2; 

### Punto 5
SELECT * FROM invoices<br />
WHERE InvoiceDate < '2012-01-31'<br />
ORDER BY InvoiceDate;

### Punto 6
SELECT DISTINCT Country FROM customers<br />
ORDER BY Country DESC;
