# 🐬 Create database on Mariadb

1. Once we have finished with the installation of mariadb we must create the database and the user for the WordPress. First we must access mariadb with ne command:

```sh
mariadb
```

2. We create a database for the WordPress. In my case I'm going to call it wp\_database. I will do all this with the command:

```sql
CREATE DATABASE wp_database;
```

3. To make sure that the database for WordPress has been created we can view all existing databases with the command:

```sql
SHOW DATABASES;
```

4. Next we need to create a user inside the database. We will use the command:

```sql
 CREATE USER 'gemartin'@'localhost' IDENTIFIED BY '12345';
```

5. We bind the new user to our database so that we grant him the necessary permissions to be able to work. We will use the command:

```sql
GRANT ALL PRIVILEGES ON wp_database.* TO 'gemartin'@'localhost';
```

6. We update the permissions for the changes to take effect with the command:

```sql
FLUSH PRIVILEGES;
```

7. Once we have completed the previous step, we can exit mariadb:

```sql
exit
```

