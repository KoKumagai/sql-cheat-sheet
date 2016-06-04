# ALIAS

## Syntax

```sql
SELECT
  column_name1 AS alias_column_name1,
  column_name2 AS alias_column_name2,
  ...
FROM
  table_name AS alias_table_name
;
```
Or
```sql
SELECT
  column_name1 alias_column_name1,
  column_name2 alias_column_name2,
  ...
FROM
  table_name alias_table_name
;
```
The as keyword is optional on almost all RDBMS(MySQL, PostgreSQL, SQLite, SQL Server) but you can't use on Oracle it's illegal.

## Example

### Users table

| id | name       | email                  | encrypted_password | country |
|:---|:----------:|:----------------------:|:------------------:|:-------:|
| 1  | Jobs       | jobs@example.com       | dsfsfdssjnenvnnvfq | USA     |
| 2  | Page       | page@example.com       | kjfghdfsbernevnedr | USA     |
| 3  | Brin       | brin@example.com       | fajskfjnvdsnspnofe | USA     |
| 4  | Zuckerberg | zuckerberg@example.com | vncscsdvnksfdfjskw | USA     |
| 5  | Ma         | ma@example.com         | sdhlkvowvsdknvslvn | China   |
| 6  | Wang       | wang@example.com       | ewdsggggergergegge | China   |
| 7  | Ko         | ko@example.com         | qwertyuioplkjhgfds | Japan   |

### Execute
---

```sql
SELECT
  u.id   AS user_id,
  u.name AS user_name
FROM
  Users AS u
;
```
Or
```sql
SELECT
  u.id   user_id,
  u.name user_name
FROM
  Users u
;
```

#### Users table using alias clause

| user_id | user_name       |
|:--------|:---------------:|
| 1       | Jobs            |
| 2       | Page            |
| 3       | Brin            |
| 4       | Zuckerberg      |
| 5       | Ma              |
| 6       | Wang            |
| 7       | Ko              |
