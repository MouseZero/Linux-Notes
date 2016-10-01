# PostgreSQL
----
To open postgres as an admin in linux use
``` sh
sudo -u postgres psql postgres
```
To import a tar with an account that has a password
``` sh
pg_restore -U dev -d dvdrental /tmp/dvd.tar -W -h localhost
```
#### PSQL Commands
``` sql
CREATE DATABASE name;
```
Copy a table to a CSV file
``` sql
COPY actor TO '/tmp/exported.csv' DELIMITER ',' CSV;
```
Where statement
``` sql
SELECT *
FROM actor
WHERE actor_id < 11;
```
