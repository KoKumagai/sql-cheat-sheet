# INSERT INTO SELECT

## Syntax

```sql
INSERT INTO table_name2
SELECT
  *
FROM
  table_name1
;
```
Or
```sql
INSERT INTO table2
(
  column_name1,
  column_name2,
  ...
)
SELECT
  column_name3,
  column_name4,
  ...
FROM
  table_name1
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

### USandJP table

| id | name       | email                  | encrypted_password | country |
|:---|:----------:|:----------------------:|:------------------:|:-------:|
|    |            |                        |                    |         |

### Execute
---

```sql
INSERT INTO USandJP
SELECT
  *
FROM
  Users
WHERE
  country = 'USA'
  OR country = 'Japan'
;
```
Or
```sql
INSERT INTO USandJP
(
  id,
  name,
  email,
  encrypted_password,
  country
)
SELECT
  id,
  name,
  email,
  encrypted_password,
  country
FROM
  Users
WHERE
  country = 'USA'
  OR country = 'Japan'
;
```

### USandJP table

| id | name       | email                  | encrypted_password | country |
|:---|:----------:|:----------------------:|:------------------:|:-------:|
| 1  | Jobs       | jobs@example.com       | dsfsfdssjnenvnnvfq | USA     |
| 2  | Page       | page@example.com       | kjfghdfsbernevnedr | USA     |
| 3  | Brin       | brin@example.com       | fajskfjnvdsnspnofe | USA     |
| 4  | Zuckerberg | zuckerberg@example.com | vncscsdvnksfdfjskw | USA     |
| 7  | Ko         | ko@example.com         | qwertyuioplkjhgfds | Japan   |
