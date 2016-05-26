# LIMIT, ROWNUM or TOP

## Syntax

For MySQL, PostgreSQL and SQLite
```sql
SELECT
  column_name1,
  column_name2,
  ...
FROM
  table_name
LIMIT number
;
```
For Oracle
```sql
SELECT
  column_name1,
  column_name2,
  ...
FROM
  table_name
WHERE
  ROWNUM <= number
;
```
For SQL Server
```sql
SELECT TOP number|percent
  column_name1,
  column_name2,
  ...
FROM
  table_name
;
```

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
For MySQL, PostgreSQL and SQLite
```sql
SELECT
  id,
  name,
  email,
  encrypted_password,
  country
FROM
  Users
LIMIT 3
;
```
For Oracle
```sql
SELECT
  id,
  name,
  email,
  encrypted_password,
  country
FROM
  Users
WHERE
  ROWNUM <= 3
;
```
For SQL Server
```sql
SELECT TOP 3
  id,
  name,
  email,
  encrypted_password,
  country
FROM
  Users
;
```

#### Users table using limit, rownum or top clause

| id | name       | email                  | encrypted_password | country |
|:---|:----------:|:----------------------:|:------------------:|:-------:|
| 1  | Jobs       | jobs@example.com       | dsfsfdssjnenvnnvfq | USA     |
| 2  | Page       | page@example.com       | kjfghdfsbernevnedr | USA     |
| 3  | Brin       | brin@example.com       | fajskfjnvdsnspnofe | USA     |
