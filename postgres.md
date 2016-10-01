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
COUNT and GROUP BY. Note that COUNT is an aggregate function that changes how the query acts and the GROUP BY keyword is required
``` sql
SELECT first_name, COUNT(first_name)
FROM actor
WHERE actor_id BETWEEN 100 AND 200
GROUP BY first_name;
```
When you use an "aggregate function" you need to use "HAVING" to add requirements not "WHERE"
``` sql
SELECT first_name, COUNT(first_name)
FROM actor
WHERE actor_id BETWEEN 100 AND 200
GROUP BY first_name
HAVING COUNT(first_name) > 1;
```
INSERT INTO statement. Make sure to check the schema for automatically filled columns.
``` sql
INSERT INTO actor (first_name, last_name)
VALUES ('Robert', 'Johnson');
```
DELETE
``` sql
DELETE
FROM actor
WHERE first_name = 'Robert';
```
