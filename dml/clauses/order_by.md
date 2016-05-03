# ORDER BY

## Syntax

```sql
SELECT
  column_name1,
  column_name2,
  ...
FROM
  table_name
ORDER BY
  column_name1 [ASC | DESC],
  column_name2,[ASC | DESC],
  ...
;
```
The order by clause sorts the records in ***ascending*** order by default.

## Example

### Users table

| id | name       | email                  | encrypted_password |
|:---|:----------:| :---------------------:|:------------------:|
| 1  | Jobs       | jobs@example.com       | dsfsfdssjnenvnnvfq |
| 2  | Page       | page@example.com       | kjfghdfsbernevnedr |
| 3  | Brin       | brin@example.com       | fajskfjnvdsnspnofe |
| 4  | Zuckerberg | zuckerberg@example.com | vncscsdvnksfdfjskw |
| 5  | Ko         | ko@example.com         | qwertyuioplkjhgfds |

### Execute
---

```sql
SELECT
  id,
  name,
  email,
  encrypted_password
FROM
  Users
ORDER BY
  name DESC
;
```

#### Users table using order by clause

| id | name       | email                  | encrypted_password |
|:---|:----------:| :---------------------:|:------------------:|
| 4  | Zuckerberg | zuckerberg@example.com | vncscsdvnksfdfjskw |
| 2  | Page       | page@example.com       | kjfghdfsbernevnedr |
| 5  | Ko         | ko@example.com         | qwertyuioplkjhgfds |
| 1  | Jobs       | jobs@example.com       | dsfsfdssjnenvnnvfq |
| 3  | Brin       | brin@example.com       | fajskfjnvdsnspnofe |
