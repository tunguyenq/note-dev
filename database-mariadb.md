### Install
 
```bash
mysql_secure_installation
```

### Show user
	SELECT User,Host FROM mysql.user;
### Show database

```sh
show databases;
```

### Grant

```sh
GRANT ALL ON [db].* TO '[username]'@'%' IDENTIFIED BY '[password]' WITH GRANT OPTION;
GRANT ALL PRIVILEGES ON dbTest.* To 'user'@'%' IDENTIFIED BY 'password';
```

### Grant prefix
```sh
GRANT ALL ON `bds_%`.* TO 'bds'@'localhost' ;
```

### WITH GRANT OPTION can make role
	GRANT ALL PRIVILEGES ON [db].* TO '[username]'@'%' IDENTIFIED BY '[password]' WITH GRANT OPTION;
	GRANT ALL PRIVILEGES ON mydb.* TO '[username]'@'%' WITH GRANT OPTION;

### Show grant
```sh
SHOW GRANTS FOR 'bloguser'@'%';
```

### Drop user
 	DROP USER IF EXISTS demo
 	DROP USER demo


### Revoke all grants for a mysql user
	mariadb> REVOKE ALL PRIVILEGES, GRANT OPTION FROM 'bloguser'@'localhost';
	grant all on *.* to [username]@'%' identified by '[password]'; flush privileges;

### export
	mysqldump -u root -p --opt --all-databases > alldb.sql
	mysqldump -u root -p --all-databases --skip-lock-tables > alldb.sql
	mysqldump -u root -p --databases db_name ...


### Import
	mysql database_name < database_dump.sql


	