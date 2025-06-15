# new-springboot

CREATE USER "barath"@"%" IDENTIFIED BY "2521";   ----------->To create a USER in SQL


GRANT ALL PRIVILEGES ON *.* TO 'barath'@'%' WITH GRANT OPTION;   -------------> To set All Permission to the USER

FLUSH PRIVILEGES;


SELECT User, Host FROM mysql.user;    ------> to list all user

mysql -u barath -p   --------->  To Set or Change PASSWD to the USER

create database notes_app;   ------> To create a database.


 vi /etc/mysql/mysql.conf.d/mysqld.cnf   _-------> open this file in mysql database server and add bind address as a 
 
 bind-address            = 0.0.0.0
mysqlx-bind-address     = 127.0.0.1


and in vi src/main/resources/application.properties FILE 

 jdbc:mysql://13.214.203.153:3306/notes_app?useSSL=false&serverTimezone=UTC&useLegacyDatetimeCode=false&allowPublicKeyRetrieval=true&useSSL=false  
 
 add like this
 
  {
        "id": 4,
        "title": "book-4",
        "content": "new book-4"
 }
 
 
