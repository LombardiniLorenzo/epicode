# PUNTO 1
SELECT BillingCity, BillingCountry, Total FROM invoices<br />
WHERE BillingCountry = 'Canada' AND Total < 4;

# PUNTO 2
SELECT Name, Composer FROM Tracks<br />
WHERE Name LIKE '%Dog%';

# PUNTO 3
SELECT FirstName, LastName, Country FROM Customers;

SELECT FirstName, LastName, Country FROM Customers<br />
WHERE Country = 'Brazil' AND LastName LIKE 'R%';

# PUNTO 4
SELECT * FROM invoices<br />
WHERE Total > 8 OR Total < 2; 

# PUNTO 5
SELECT * FROM invoices<br />
WHERE InvoiceDate < '2012-01-31'<br />
ORDER BY InvoiceDate;

# PUNTO 6
SELECT DISTINCT Country FROM customers<br />
ORDER BY Country DESC;
