# 创建数据库

```
mysql> create DATABASE <数据库名>;
```

**实战：**

先查看一下现有的数据库列表

```
mysql> show DATABASES;
+--------------------+
| Database           |
+--------------------+
| information_schema |
| mysql              |
| performance_schema |
| sakila             |
| sys                |
| world              |
+--------------------+
6 rows in set (0.08 sec)
```

创建数据库 school

```
mysql> create DATABASE school;
Query OK, 1 row affected (0.02 sec)
```

再次检查数据库列表，可以发现已经创建了一个 school 数据库

```
mysql> show DATABASES;
+--------------------+
| Database           |
+--------------------+
| information_schema |
| mysql              |
| performance_schema |
| sakila             |
| school             |
| sys                |
| world              |
+--------------------+
7 rows in set (0.00 sec)
```

# 删除数据库

```
mysql> drop DATABASE <数据库名>;
```

**实战：**

检查现有数据库列表

```
 mysql> show DATABASES;
+--------------------+
| Database           |
+--------------------+
| information_schema |
| mysql              |
| performance_schema |
| sakila             |
| school             |
| sys                |
| world              |
+--------------------+
7 rows in set (0.00 sec)
```

删除 school 数据库

```
mysql> drop DATABASE school;
Query OK, 0 rows affected (0.01 sec)
```

检查删除后的数据库列表

```
mysql> show DATABASES;
+--------------------+
| Database           |
+--------------------+
| information_schema |
| mysql              |
| performance_schema |
| sakila             |
| sys                |
| world              |
+--------------------+
6 rows in set (0.00 sec)
```

# 选择指定数据库

查看一下现有数据库列表（刚刚删除的 school 我又创建回来了）

```
mysql> show DATABASES;
+--------------------+
| Database           |
+--------------------+
| information_schema |
| mysql              |
| performance_schema |
| sakila             |
| school             |
| sys                |
| world              |
+--------------------+
7 rows in set (0.00 sec)
```

现在选中 school 以便进行后续操作

```
mysql> use school;
Database changed
```

**注意：**所有的数据库名、表名、字段名都是区分大小写的








