#  PostgreSQL commands


### Create the backup
```
 PGPASSWORD=user123 pg_dump -U postgres -h localhost -p 5432 fenyx > ~/Downloads/fenyx_backup.sql
```
### Once the file exists, restore it with:

```
psql -U postgres -h localhost -d fenyx < ~/Downloads/fenyx_backup.sql
```

### Connect to PostgreSQL server
```
psql -U postgres
```
### or connect directly to a database
```
psql -U postgres -d your_db_name
```
### Create a new database
```
CREATE DATABASE your_db_name;
```
### Drop a database
```
Drop a database
```

### Inside psql shel

```
\l
```
## User (Role) operations
### Create user
```
CREATE USER your_username WITH PASSWORD 'your_password';
```
### Grant privileges on a database
```
GRANT ALL PRIVILEGES ON DATABASE your_db_name TO your_username;
```
### Connecting to a database
```
psql -U your_username -d your_db_name
```
### List tables in the current database
```
\dt
```
### Describe a table schema
```
\d your_table_name
```
### Export (Backup) database to a file
```
pg_dump -U your_username your_db_name > backup_file.sql
```

### Import (Restore) database from a file

```
psql -U your_username your_db_name < backup_file.sql
```

