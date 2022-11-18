### PUNTO 1
CREATE DATABASE incidenti;<br />
sqlite3 incidenti

### PUNTO 2
CREATE TABLE proprietari(<br />
&ensp;&ensp;&ensp;CodF VARCHAR(16) PRIMARY KEY,<br />
&ensp;&ensp;&ensp;Nome VARCHAR(64) NOT NULL,<br />
&ensp;&ensp;&ensp;Residenza VARCHAR(128) NOT NULL<br />
);

CREATE TABLE assicurazione(<br />
&ensp;&ensp;&ensp;CodAss INTEGER PRIMARY KEY AUTOINCREMENT,<br />
&ensp;&ensp;&ensp;Nome VARCHAR(64) NOT NULL,<br />
&ensp;&ensp;&ensp;Sede VARCHAR(64) NOT NULL<br />
);

CREATE TABLE auto(<br />
&ensp;&ensp;&ensp;Targa VARCHAR(7) PRIMARY KEY,<br />
&ensp;&ensp;&ensp;Marca VARCHAR(32) NOT NULL,<br />
&ensp;&ensp;&ensp;Cilindrata INTEGER NOT NULL,<br />
&ensp;&ensp;&ensp;Potenza INTEGER NOT NULL,<br />
&ensp;&ensp;&ensp;CodF VARCHAR(16) NOT NULL,<br />
&ensp;&ensp;&ensp;CodAss INTEGER NOT NULL,<br />
&ensp;&ensp;&ensp;FOREIGN KEY (CodF)<br />
&ensp;&ensp;&ensp;REFERENCES proprietari(CodF),<br />
&ensp;&ensp;&ensp;FOREIGN KEY (CodAss)<br />
&ensp;&ensp;&ensp;REFERENCES assicurazione(CodAss)<br />
);

CREATE TABLE sinistro(<br />
&ensp;&ensp;&ensp;CodS INTEGER PRIMARY KEY AUTOINCREMENT,<br />
&ensp;&ensp;&ensp;Localita VARCHAR(64) NOT NULL,<br />
&ensp;&ensp;&ensp;Data DATETIME NOT NULL<br />
);

CREATE TABLE autocoinvolte(<br />
&ensp;&ensp;&ensp;CodAc INTEGER PRIMARY KEY AUTOINCREMENT,<br />
&ensp;&ensp;&ensp;CodS INTEGER NOT NULL,<br />
&ensp;&ensp;&ensp;Targa VARCHAR(7) NOT NULL,<br />
&ensp;&ensp;&ensp;ImportoDelDanno FLOAT NOT NULL, <br />
&ensp;&ensp;&ensp;FOREIGN KEY (CodS)<br />
&ensp;&ensp;&ensp;REFERENCES sinistro(CodS),<br />
&ensp;&ensp;&ensp;FOREIGN KEY (Targa)<br />
&ensp;&ensp;&ensp;REFERENCES auto(Targa)<br />
);

### PUNTO 3
SELECT Targa, Marca FROM auto<br />
&ensp;&ensp;&ensp;WHERE Cilindrata > 1500 OR Potenza > 100;

### PUNTO 4
SELECT COUNT(CodF), Residenza FROM proprietari<br />
&ensp;&ensp;&ensp;GROUP BY Residenza;

