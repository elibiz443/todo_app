# Todo_App 

Requirements:

* DB ---------->>> Mysql version 8.0.26
* OS ---------->>> Ubuntu 21.04
* Language ---->>> PHP 8.0.10
                   HTML5, CSS, JS
* Server ------>>> Apache/2.4.46

Login to mysql:

```
  mysql -u your_user_name -p
  password: your_pasword

```
Create DB:(Make sure you have full permissions, otherwise; follow this tutorial --->>> https://www.digitalocean.com/community/tutorials/how-to-create-a-new-user-and-grant-permissions-in-mysql)

```
  create database testdb1;
```
Show DB:
```
  SHOW DATABASES;
```

Select DB:
```
  use testdb1;
```
Create tables: 
  ```
  CREATE TABLE login(username VARCHAR(30), pasword VARCHAR(30));
  CREATE TABLE signup(username VARCHAR(30), email VARCHAR(30), password VARCHAR(30), confirm_password VARCHAR(30));
  CREATE TABLE todo_list(item_id INT AUTO_INCREMENT, title VARCHAR(255), content VARCHAR(255), PRIMARY KEY(item_id));
  ```
Show all the tables: 
```
  SHOW TABLES;
```
Populate tables:
```
  insert into login values("myname", "password");
  insert into signup values("myname", "myname@gmail.com", "password", "password");
  insert into todo_list values(1, "The Dream", "I have a dream!");
```
Show table data:(Example todo_list)
```
  select * from todo_list; 
```
Quite: 
```
  exit OR \q
```
## Additional Commands for DB:

Delete DB:
```
  DROP DATABASE testdb1;
```
Rename tables:
```
  ALTER TABLE todo_list RENAME TO my_todo_list;
```
Delete table:
```
  DROP TABLE todo_list;
```
Delete data from table:
```
  DELETE FROM todo_list WHERE item_id=2;
```
Update table data:
```
  UPDATE todo_list SET content="I still do have a dream" WHERE item_id = 2;
```
Rename column in a table:
```
  ALTER TABLE signup CHANGE COLUMN email my_email varchar(40) NOT NULL;
```
Drop column from a table:
```
  ALTER TABLE my_todo_list DROP COLUMN title;
```
Add new column in a table: 
```
  ALTER TABLE my_todo_list ADD title VARCHAR(255) NOT NULL AFTER item_id;
```

## creating your project:

* Go to terminal:
```
  sudo -i
  chmod -R 777 /var/www/html
  cd /var/www/html
  mkdir my_project_name
  cd my_project_name
  touch index.php
```
After writing your code, start the apache server:
```
  sudo service apache2 start
```
In your browser, go to:
```
  localhost/my_project_name/index.php
```
#### Voilà
