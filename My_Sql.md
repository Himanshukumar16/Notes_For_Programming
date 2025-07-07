```
                MySql
```
1) Database :-> A database in MySQL is a collection of tables, views, procedures, triggers, and other objects that work together to store and manage data.
it consists of many tables. tables consist of rows and columns.

2) SQL :-> SQL is programming language used to interact with relational databases. it helps in create , read, update, delete data...It is not a case sensitive small likho ya capital sab same !

3) creating a database :-> ```CREATE DATBASE dtabaseName;```
```
   mysql> CREATE DATABASE practice;
   Query OK, 1 row affected (0.01 sec)
```
5) delete a database :-> ```drop database databaseName;```
```
   mysql> drop Database Practice;
   Query OK, 0 rows affected (0.01 sec)
```
7) to use database :-> ```use databaseName```
```
   mysql> use practice;
   Database changed
```
9) to create table for using :-> ```create table tableName(columnName 1 datatype,columnName 2 datatype,columnName 3 datatype);```
```
mysql> create table student(id int primary key,name varchar(50),age int not null);
Query OK, 0 rows affected (0.07 sec)
```
10) to see the tables in database :->```show tables;```
```
    mysql> show tables;
+--------------------+
| Tables_in_practice |
+--------------------+
| student            |
+--------------------+
1 row in set (0.01 sec)
```
