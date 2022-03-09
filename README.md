mysql> CREATE TABLE Persons (
    ->     PersonID int,
    ->     LastName varchar(255),
    ->     FirstName varchar(255),
    ->     Address varchar(255),
    ->     City varchar(255)
    -> );
Query OK, 0 rows affected (0.03 sec)

mysql> insert into Persons ('PersonID') values(1);
ERROR 1064 (42000): You have an error in your SQL syntax; check the manual that corresponds to your MySQL server version for the right syntax to use near ''PersonID') values(1)' at line 1
mysql> insert into Persons  values(1, 'amit','amit', 'elyahu', 'gedera');
Query OK, 1 row affected (0.01 sec)

mysql> insert into Persons  values(2, 'maya','amit', 'elyahu', 'gedera');
Query OK, 1 row affected (0.01 sec)

mysql> insert into Persons  values(2, 'orit','amit', 'elyahu', 'gedera');
Query OK, 1 row affected (0.00 sec)

mysql> insert into Persons  values(3, 'orit','amit', 'elyahu', 'gedera');
Query OK, 1 row affected (0.01 sec)

mysql> insert into Persons  values(3, 'omer','amit', 'elyahu', 'gedera');
Query OK, 1 row affected (0.01 sec)

mysql> select * from Persons;
+----------+----------+-----------+---------+--------+
| PersonID | LastName | FirstName | Address | City   |
+----------+----------+-----------+---------+--------+
|        1 | amit     | amit      | elyahu  | gedera |
|        2 | maya     | amit      | elyahu  | gedera |
|        2 | orit     | amit      | elyahu  | gedera |
|        3 | orit     | amit      | elyahu  | gedera |
|        3 | omer     | amit      | elyahu  | gedera |
+----------+----------+-----------+---------+--------+
5 rows in set (0.00 sec)

mysql> CREATE TABLE animals (ID int, name varchar(255) );
Query OK, 0 rows affected (0.02 sec)

mysql> insert into animals  values(1, 'kelev');
Query OK, 1 row affected (0.01 sec)

mysql> insert into animals  values(2, 'hatul');
Query OK, 1 row affected (0.01 sec)

mysql> insert into animals  values(3, 'atalef');
Query OK, 1 row affected (0.00 sec)

GRANT LOCK TABLES,SELECT, RELOAD, SHOW DATABASES, REPLICATION SLAVE, REPLICATION CLIENT ON *.* TO 'my_user';
