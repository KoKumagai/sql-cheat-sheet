# HAVING

## Syntax

```sql
SELECT
  column_name1,
  ...
FROM
  table_name
GROUP BY
  column_name1,
  ...
HAVING
  conditions
;
```

## Example

### Orders table

| id | user_id | amount | order_date |
|:---|:-------:|:------:|:----------:|
| 1  | 1       | 7000   | 2010-02-24 |
| 2  | 1       | 3000   | 2010-05-03 |
| 3  | 4       | 4000   | 2011-04-02 |
| 4  | 4       | 1500   | 2012-05-14 |
| 5  | 7       | 1000   | 2015-10-19 |
| 6  | 7       | 2100   | 2015-12-22 |
| 7  | 7       | 4500   | 2016-03-15 |

### Execute
---

```sql
SELECT
  user_id,
  SUM(amount)
FROM
  Orders
GROUP BY
  user_id
HAVING
  SUM(amount) > 6000
;
```

#### Orders table using having clause

| user_id | SUM(amount) |
|:-------:|:-----------:|
| 1       | 10000       |
| 7       | 7600        |
