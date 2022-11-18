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

