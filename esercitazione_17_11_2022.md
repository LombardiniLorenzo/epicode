### PUNTO 1
CREATE DATABASE DB_azienda;<br />
sqlite3 DB_azienda

### PUNTO 2
CREATE TABLE dipendenti(<br />
   ID_dipendente INTEGER PRIMARY KEY,<br />
   nome VARCHAR(64) NOT NULL,<br />
   cognome VARCHAR(64) NOT NULL,<br />
   eta INTEGER NOT NULL,<br />
   data_assunzione DATE NOT NULL<br />
);

### PUNTO 3
INSERT INTO dipendenti (ID_dipendente, nome, cognome, eta, data_assunzione)<br />
   VALUES (1234, 'Lorenzo', 'Lombardini', 20, '2021-08-23');
   
INSERT INTO dipendenti (ID_dipendente, nome, cognome, eta, data_assunzione)<br />
   VALUES (1238, 'Mario', 'Rossi', 33, '2018-04-21');

INSERT INTO dipendenti (ID_dipendente, nome, cognome, eta, data_assunzione)<br />
   VALUES (1239, 'Giovanni', 'Verdi', 27, '2012-01-19');

### PUNTO 4
CREATE TABLE progetti(<br />
&nbsp;ID_progetto INTEGER PRIMARY KEY AUTOINCREMENT,<br />
&ensp;nome_progetto VARCHAR(128) NOT NULL,<br />
&ensp;ID_dipendente INTEGER NOT NULL,<br />
&ensp;FOREIGN KEY (ID_dipendente)<br />
&ensp;REFERENCES dipendenti(ID_dipendente)<br />
);
