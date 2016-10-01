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
#### Basic Commands
``` sql
create database name
```
