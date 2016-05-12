# CREATE VIEW

## Syntax

```sql
CREATE VIEW view_name AS
SELECT
  column_name1,
  column_name2,
  ...
FROM
  table_name
WHERE
  [condition]
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


### Create USandJP view
---

```sql
CREATE VIEW USandJP AS
SELECT
  id,
  name,
  email,
  country
FROM
  Users
WHERE
  country = 'USA'
  OR country = 'Japan'
;
```

### After create USandJP view
---

```sql
SELECT
  *
FROM
  USandJP
;
```

#### USandJP view

| id | name       | email                  | country |
|:---|:----------:| :---------------------:|:-------:|
| 1  | Jobs       | jobs@example.com       | USA     |
| 2  | Page       | page@example.com       | USA     |
| 3  | Brin       | brin@example.com       | USA     |
| 4  | Zuckerberg | zuckerberg@example.com | USA     |
| 7  | Ko         | ko@example.com         | Japan   |
