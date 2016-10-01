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
WHERE statement
``` sql
SELECT *
FROM actor
WHERE actor_id < 11;
```
ORDER BY statement
``` sql
SELECT *
FROM actor
WHERE actor_id < 11
ORDER BY first_name;
```
COUNT and GROUP BY
``` sql
SELECT first_name, COUNT(first_name)
FROM actor
WHERE actor_id BETWEEN 100 AND 200
GROUP BY first_name;
```
