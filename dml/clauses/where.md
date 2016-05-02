# WHERE

## Syntax

```sql
SELECT
  column_name1,
  column_name2,
  ...
FROM
  table_name
WHERE
  conditions
;
```

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
WHERE
  id = 5
;
```

#### Users table using where clause

| id | name       | email                  | encrypted_password |
|:---|:----------:| :---------------------:|:------------------:|
| 5  | Ko         | ko@example.com         | qwertyuioplkjhgfds |
