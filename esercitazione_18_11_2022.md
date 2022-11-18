### PUNTO 1
CREATE DATABASE incidenti;<br />
sqlite3 incidenti

### PUNTO 2
CREATE TABLE proprietari(<br />
CodF VARCHAR(16) PRIMARY KEY,<br />
Nome VARCHAR(64) NOT NULL,<br />
Residenza VARCHAR(128) NOT NULL<br />
);
