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

	or
  mysql> create database if not exists databaseName; preferred
```
5) delete a database :-> ```drop database databaseName;```
```
   mysql> drop Database Practice;
   Query OK, 0 rows affected (0.01 sec)

	or

  mysql> drop database if exists databaseName; preferred
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
11) Add values in table :-> ```insert into tableName values(id,name,age);```
```
mysql> insert into student values(1,"Himanshu",50);
Query OK, 1 row affected (0.02 sec)
```
12) SQL Datatypes :-> 

Numerical Datatypes:

| Datatype       | Description                  | Example                      |
| -------------- | ---------------------------- | ---------------------------- |
| `INT`          | Integer number               | `5`, `-20`                   |
| `BIGINT`       | Large integer                | `9876543210`                 |
| `FLOAT`        | Floating point (approximate) | `3.14`                       |
| `DOUBLE`       | Double precision float       | `2.718281828`                |
| `DECIMAL(M,D)` | Fixed point, precise         | `DECIMAL(10,2)` → `12345.67` |

String / Text Data Types

| Datatype     | Description                 | Example                          |
| ------------ | --------------------------- | -------------------------------- |
| `CHAR(n)`    | Fixed-length string         | `CHAR(5)` → `'abc  '`            |
| `VARCHAR(n)` | Variable-length string      | `VARCHAR(50)` → `'hello world'`  |
| `TEXT`       | Large text block            | Long article                     |
| `ENUM`       | One value from a list       | `'small'`, `'medium'`, `'large'` |
| `SET`        | Multiple values from a list | `'red,blue'`                     |

date and time datatypes

| Datatype    | Description                  | Example                 |
| ----------- | ---------------------------- | ----------------------- |
| `DATE`      | Date only                    | `'2025-07-07'`          |
| `TIME`      | Time only                    | `'14:30:00'`            |
| `DATETIME`  | Date and time                | `'2025-07-07 14:30:00'` |
| `TIMESTAMP` | Date and time (auto updates) | `'2025-07-07 14:30:00'` |
| `YEAR`      | Year only                    | `2025`                  |

Binary Data Types

| Datatype       | Description                         | Example         |
| -------------- | ----------------------------------- | --------------- |
| `BLOB`         | Binary Large Object (images, files) | Image file      |
| `VARBINARY(n)` | Variable-length binary              | Raw binary data |

13) types of SQL commands :-> 

| Category | Example Commands                             |
| -------- | -------------------------------------------- |
| DDL      | CREATE, ALTER, DROP, TRUNCATE, RENAME        |
| DML      | INSERT, UPDATE, DELETE                       |
| DQL      | SELECT                                       |
| DCL      | GRANT, REVOKE                                |
| TCL      | COMMIT, ROLLBACK, SAVEPOINT, SET TRANSACTION |
