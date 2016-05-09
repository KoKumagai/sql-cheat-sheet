# IN

## Syntax

```sql
SELECT
  column_name1,
  column_name2,
  ...
FROM
  table_name
WHERE
  column_name1 [NOT] IN (value1, value2, ...)
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

### Execute
---

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
  country IN ('USA', 'Japan');
;
```

#### Users table using in clause

| id | name       | email                  | encrypted_password | country |
|:---|:----------:| :---------------------:|:------------------:|:-------:|
| 1  | Jobs       | jobs@example.com       | dsfsfdssjnenvnnvfq | USA     |
| 2  | Page       | page@example.com       | kjfghdfsbernevnedr | USA     |
| 3  | Brin       | brin@example.com       | fajskfjnvdsnspnofe | USA     |
| 4  | Zuckerberg | zuckerberg@example.com | vncscsdvnksfdfjskw | USA     |
| 7  | Ko         | ko@example.com         | qwertyuioplkjhgfds | Japan   |
