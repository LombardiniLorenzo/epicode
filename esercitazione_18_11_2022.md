### PUNTO 1
CREATE DATABASE incidenti;<br />
sqlite3 incidenti

### PUNTO 2
CREATE TABLE proprietari(<br />
&ensp;&ensp;&ensp;CodF VARCHAR(16) PRIMARY KEY,<br />
&ensp;&ensp;&ensp;Nome VARCHAR(64) NOT NULL,<br />
&ensp;&ensp;&ensp;Residenza VARCHAR(128) NOT NULL<br />
);
