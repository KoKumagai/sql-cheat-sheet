# BETWEEN

## Syntax

```sql
SELECT
  column_name1,
  column_name2,
  ...
FROM
  table_name
WHERE
  column_name1 [NOT] BETWEEN value1 AND value2
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
  id,
  user_id,
  amount,
  order_date
FROM
  Orders
WHERE
  order_date BETWEEN '2011-01-01' AND '2015-11-01'
;
```

#### Orders table using between clause

| id | user_id | amount | order_date |
|:---|:-------:|:------:|:----------:|
| 3  | 4       | 4000   | 2011-04-02 |
| 4  | 4       | 1500   | 2012-05-14 |
| 5  | 7       | 1000   | 2015-10-19 |
