# IS NULL

## Syntax

```sql
SELECT
  column_name1,
  column_name2,
  ...
FROM
  table_name
WHERE
  column_name1 IS [NOT] NULL
;
```

## Example

### Users table

| id | first_name | middle_name  | last_name  | email                  | encrypted_password | country |
|:---|:----------:|:------------:| :---------:|:----------------------:|:------------------:|:-------:|
| 1  | Steven     | Paul         | Jobs       | jobs@example.com       | dsfsfdssjnenvnnvfq | USA     |
| 2  | Lawrence   |              | Page       | page@example.com       | kjfghdfsbernevnedr | USA     |
| 3  | Sergey     | Mikhaylovich | Brin       | brin@example.com       | fajskfjnvdsnspnofe | USA     |
| 4  | Mark       | Elliot       | Zuckerberg | zuckerberg@example.com | vncscsdvnksfdfjskw | USA     |
| 5  | Ko         |              | Kumagai    | ko@example.com         | qwertyuioplkjhgfds | Japan   |

### Execute
---

```sql
SELECT
  id,
  first_name,
  middle_name,
  last_name,
  email,
  encrypted_password,
  country
FROM
  Users
WHERE
  middle_name IS NULL
;
```

#### Users table using is null clause

| id | first_name | middle_name  | last_name  | email                  | encrypted_password | country |
|:---|:----------:|:------------:| :---------:|:----------------------:|:------------------:|:-------:|
| 2  | Lawrence   |              | Page       | page@example.com       | kjfghdfsbernevnedr | USA     |
| 5  | Ko         |              | Kumagai    | ko@example.com         | qwertyuioplkjhgfds | Japan   |
