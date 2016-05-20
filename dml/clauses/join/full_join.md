# FULL JOIN

## Syntax

```sql
SELECT
  table1.column_name1,
  table2.column_name2
  ...
FROM
  table1
  FULL JOIN table2
    ON table1.column_name1 = table2.column_name2
;
```
Or  
For unsupported full join clause
```sql
SELECT
  table1.column_name1,
  table2.column_name2
  ...
FROM
  table1
  LEFT JOIN table2
    ON table1.column_name1 = table2.column_name2
UNION
SELECT
  table1.column_name1,
  table2.column_name2
  ...
FROM
  table1
  RIGHT JOIN table2
    ON table1.column_name1 = table2.column_name2
;
```

## Example

### Users table

| id | name       | email                  | encrypted_password | country |
|:---|:----------:| :---------------------:|:------------------:|:-------:|
| 1  | Jobs       | jobs@example.com       | dsfsfdssjnenvnnvfq | USA     |
| 2  | Page       | page@example.com       | kjfghdfsbernevnedr | USA     |
| 3  | Brin       | brin@example.com       | fajskfjnvdsnspnofe | USA     |
| 4  | Zuckerberg | zuckerberg@example.com | vncscsdvnksfdfjskw | USA     |
| 5  | Ma         | ma@example.com         | sdhlkvowvsdknvslvn | China   |
| 6  | Wang       | wang@example.com       | ewdsggggergergegge | China   |
| 7  | Ko         | ko@example.com         | qwertyuioplkjhgfds | Japan   |

### Orders table

| id | user_id | amount | order_date |
|:---|:-------:|:------:|:----------:|
| 1  | 1       | 7000   | 2010-02-24 |
| 2  | 4       | 1500   | 2012-05-14 |
| 3  | 4       | 4000   | 2004-04-02 |
| 4  | 7       | 1000   | 2015-12-06 |
| 5  | 10      | 9999   | 2016-05-18 |

### Execute
---

```sql
SELECT
  Users.id,
  Users.name,
  Users.email,
  Users.encrypted_password,
  Users.country,
  Orders.id,
  Orders.user_id,
  Orders.amount,
  Orders.order_date
FROM
  Users
  FULL JOIN Orders
    ON Users.id = Orders.user_id
ORDER BY
  Users.id,
  Orders.id
;
```
Or  
For unsupported full join clause
```sql
SELECT
  Users.id,
  Users.name,
  Users.email,
  Users.encrypted_password,
  Users.country,
  Orders.id,
  Orders.user_id,
  Orders.amount,
  Orders.order_date
FROM
  Users
  LEFT JOIN Orders
    ON Users.id = Orders.user_id
UNION
SELECT
  Users.id,
  Users.name,
  Users.email,
  Users.encrypted_password,
  Users.country,
  Orders.id,
  Orders.user_id,
  Orders.amount,
  Orders.order_date
FROM
  Users
  RIGHT JOIN Orders
    ON Users.id = Orders.user_id
;
```

#### Using full join clause

| id   | name       | email                  | encrypted_password | country | id   | user_id | amount | order_date |
|:-----|:----------:| :---------------------:|:------------------:|:-------:|:-----|:-------:|:------:|:----------:|
| 1    | Jobs       | jobs@example.com       | dsfsfdssjnenvnnvfq | USA     | 1    | 1       | 7000   | 2010-02-24 |
| 2    | Page       | page@example.com       | kjfghdfsbernevnedr | USA     | NULL | NULL    | NULL   | NULL       |
| 3    | Brin       | brin@example.com       | fajskfjnvdsnspnofe | USA     | NULL | NULL    | NULL   | NULL       |
| 4    | Zuckerberg | zuckerberg@example.com | vncscsdvnksfdfjskw | USA     | 2    | 4       | 1500   | 2012-05-14 |
| 4    | Zuckerberg | zuckerberg@example.com | vncscsdvnksfdfjskw | USA     | 3    | 4       | 4000   | 2004-04-02 |
| 5    | Ma         | ma@example.com         | sdhlkvowvsdknvslvn | China   | NULL | NULL    | NULL   | NULL       |
| 6    | Wang       | wang@example.com       | ewdsggggergergegge | China   | NULL | NULL    | NULL   | NULL       |
| 7    | Ko         | ko@example.com         | qwertyuioplkjhgfds | Japan   | 4    | 7       | 1000   | 2015-12-06 |
| NULL | NULL       | NULL                   | NULL               | NULL    | 5    | 10      | 9999   | 2016-05-18 |
