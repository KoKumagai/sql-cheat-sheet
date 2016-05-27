# SELECT

## Syntax

```sql
SELECT
  column_name1,
  column_name2
FROM
  table_name
;
```

## Order of Operations
1. FROM clause
2. WHERE clause
3. GROUP BY clause
4. HAVING clause
5. SELECT clause
6. ORDER BY clause

## Example

```sql
SELECT
  id,
  name,
  email,
  encrypted_password
FROM
  Users
;
```

#### Users table

| id | name       | email                  | encrypted_password |
|:---|:----------:| :---------------------:|:------------------:|
| 1  | Jobs       | jobs@example.com       | dsfsfdssjnenvnnvfq |
| 2  | Page       | page@example.com       | kjfghdfsbernevnedr |
| 3  | Brin       | brin@example.com       | fajskfjnvdsnspnofe |
| 4  | Zuckerberg | zuckerberg@example.com | vncscsdvnksfdfjskw |
