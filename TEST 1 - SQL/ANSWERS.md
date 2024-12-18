# Explore the Schema
## SQL Queries
To identify all the tables in the `kinternship2025` database: `SHOW TABLES;`
To determine, for each table, their column names, data types, primary keys and foreign keys: `SHOW COLUMNS FROM <TABLE>;`
Note : to see the keys, I used `SHOW KEYS FROM table;`, but it returned "Empty set", but we can guess which columns should be keys with their name (example: customer_id).
## Tables in the kinternship2025 database :
mysql> SHOW TABLES;
+---------------------------+
| Tables_in_kinternship2025 |
+---------------------------+
| customers                 |
| order_items               |
| orders                    |
| payments                  |
| products                  |
+---------------------------+

mysql> SHOW COLUMNS FROM customers;
+-------------+--------------+------+-----+---------+-------+
| Field       | Type         | Null | Key | Default | Extra |
+-------------+--------------+------+-----+---------+-------+
| customer_id | varchar(255) | YES  |     | NULL    |       | (primary key)
| first_name  | varchar(255) | YES  |     | NULL    |       |
| last_name   | varchar(255) | YES  |     | NULL    |       |
| email       | varchar(255) | YES  |     | NULL    |       |
| phone       | varchar(255) | YES  |     | NULL    |       |
| address     | varchar(255) | YES  |     | NULL    |       |
| city        | varchar(255) | YES  |     | NULL    |       |
| state       | varchar(255) | YES  |     | NULL    |       |
| postal_code | varchar(255) | YES  |     | NULL    |       |
| country     | varchar(255) | YES  |     | NULL    |       |
+-------------+--------------+------+-----+---------+-------+

mysql> SHOW COLUMNS FROM order_items;
+------------+--------------+------+-----+---------+-------+
| Field      | Type         | Null | Key | Default | Extra |
+------------+--------------+------+-----+---------+-------+
| order_id   | varchar(255) | YES  |     | NULL    |       | (foreign key)
| product_id | varchar(255) | YES  |     | NULL    |       | (foreign key)
| quantity   | varchar(255) | YES  |     | NULL    |       |
| price      | varchar(255) | YES  |     | NULL    |       |
+------------+--------------+------+-----+---------+-------+

mysql> SHOW COLUMNS FROM orders;
+--------------+--------------+------+-----+---------+-------+
| Field        | Type         | Null | Key | Default | Extra |
+--------------+--------------+------+-----+---------+-------+
| order_id     | varchar(255) | YES  |     | NULL    |       | (foreign key)
| customer_id  | varchar(255) | YES  |     | NULL    |       | (foreign key)
| order_date   | varchar(255) | YES  |     | NULL    |       |
| status       | varchar(255) | YES  |     | NULL    |       |
| total_amount | varchar(255) | YES  |     | NULL    |       |
+--------------+--------------+------+-----+---------+-------+

mysql> SHOW COLUMNS FROM payments;
+----------------+--------------+------+-----+---------+-------+
| Field          | Type         | Null | Key | Default | Extra |
+----------------+--------------+------+-----+---------+-------+
| order_id       | varchar(255) | YES  |     | NULL    |       | (foreign key)
| payment_date   | varchar(255) | YES  |     | NULL    |       |
| amount         | varchar(255) | YES  |     | NULL    |       |
| payment_method | varchar(255) | YES  |     | NULL    |       |
| status         | varchar(255) | YES  |     | NULL    |       |
+----------------+--------------+------+-----+---------+-------+

mysql> SHOW COLUMNS FROM products;
+--------------+--------------+------+-----+---------+-------+
| Field        | Type         | Null | Key | Default | Extra |
+--------------+--------------+------+-----+---------+-------+
| product_id   | varchar(255) | YES  |     | NULL    |       | (primary key)
| product_name | varchar(255) | YES  |     | NULL    |       |
| description  | varchar(255) | YES  |     | NULL    |       |
| price        | varchar(255) | YES  |     | NULL    |       |
| stock        | varchar(255) | YES  |     | NULL    |       |
| category_id  | varchar(255) | YES  |     | NULL    |       | (I'm not sure if it's a foreign key, since there are no table named category)
+--------------+--------------+------+-----+---------+-------+