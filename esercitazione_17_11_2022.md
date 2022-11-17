### PUNTO 1
CREATE DATABASE DB_azienda;<br />
sqlite3 DB_azienda

### PUNTO 2
CREATE TABLE dipendenti(<br />
&ensp;&ensp;&ensp;ID_dipendente INTEGER PRIMARY KEY,<br />
&ensp;&ensp;&ensp;nome VARCHAR(64) NOT NULL,<br />
&ensp;&ensp;&ensp;cognome VARCHAR(64) NOT NULL,<br />
&ensp;&ensp;&ensp;eta INTEGER NOT NULL,<br />
&ensp;&ensp;&ensp;data_assunzione DATE NOT NULL<br />
);

### PUNTO 3
INSERT INTO dipendenti (ID_dipendente, nome, cognome, eta, data_assunzione)<br />
&ensp;&ensp;&ensp;VALUES (1234, 'Lorenzo', 'Lombardini', 20, '2021-08-23');
   
INSERT INTO dipendenti (ID_dipendente, nome, cognome, eta, data_assunzione)<br />
&ensp;&ensp;&ensp;VALUES (1238, 'Mario', 'Rossi', 33, '2018-04-21');

INSERT INTO dipendenti (ID_dipendente, nome, cognome, eta, data_assunzione)<br />
&ensp;&ensp;&ensp;VALUES (1239, 'Giovanni', 'Verdi', 27, '2012-01-19');

### PUNTO 4
CREATE TABLE progetti(<br />
&ensp;&ensp;&ensp;ID_progetto INTEGER PRIMARY KEY AUTOINCREMENT,<br />
&ensp;&ensp;&ensp;nome_progetto VARCHAR(128) NOT NULL,<br />
&ensp;&ensp;&ensp;ID_dipendente INTEGER NOT NULL,<br />
&ensp;&ensp;&ensp;FOREIGN KEY (ID_dipendente)<br />
&ensp;&ensp;&ensp;REFERENCES dipendenti(ID_dipendente)<br />
);

### PUNTO 5
INSERT INTO progetti (nome_progetto, ID_dipendente)<br />
&ensp;&ensp;&ensp;VALUES ('Gestionale impianto 3DS', 1234);

INSERT INTO progetti (nome_progetto, ID_dipendente)<br />
&ensp;&ensp;&ensp;VALUES ('Rete Strutturata B512', 1238);

INSERT INTO progetti (nome_progetto, ID_dipendente)<br />
&ensp;&ensp;&ensp;VALUES ('Smart FV', 1234);

INSERT INTO progetti (nome_progetto, ID_dipendente)<br />
&ensp;&ensp;&ensp;VALUES ('FindWorld', 1239);
   
INSERT INTO progetti (nome_progetto, ID_dipendente)<br />
&ensp;&ensp;&ensp;VALUES ('DiscoveryPlace', 1234);

### PUNTO 6
SELECT Composer, COUNT(TrackId) AS 'Tracks' FROM tracks<br />
&ensp;&ensp;&ensp;GROUP BY Composer<br />
&ensp;&ensp;&ensp;ORDER BY Tracks DESC;

### PUNTO 7
SELECT SUM(Total) FROM invoices<br />
&ensp;&ensp;&ensp;WHERE BillingCountry='USA';

### PUNTO 8
SELECT MIN(Total), MAX(Total) FROM invoices<br />
&ensp;&ensp;&ensp;WHERE BillingCountry='USA';
