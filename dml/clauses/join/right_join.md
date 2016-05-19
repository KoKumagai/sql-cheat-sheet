# RIGHT JOIN

## Syntax

```sql
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
  Orders.id,
  Users.name,
  Orders.amount,
  Orders.order_date
FROM
  Users
  RIGHT JOIN Orders
    ON Users.id = Orders.user_id
;
```

#### Using right join clause

| id   | name       | amount | order_date |
|:-----|:----------:|:------:|:----------:|
| 1    | Jobs       | 7000   | 2010-02-24 |
| 2    | Zuckerberg | 1500   | 2012-05-14 |
| 3    | Zuckerberg | 4000   | 2004-04-02 |
| 4    | Ko         | 1000   | 2015-12-06 |
| 5    | NULL       | 9999   | 2016-05-18 |
