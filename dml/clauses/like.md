# LIKE

## Syntax

```sql
SELECT
  column_name1,
  column_name2,
  ...
FROM
  table_name
WHERE
  column_name1 LIKE '%XXXX%'
;
```
Or
```sql
SELECT
  column_name1,
  column_name2,
  ...
FROM
  table_name
WHERE
  column_name1 LIKE '_XXXX_'
;
```
The percent sign (%) represents zero, one, or multiple characters.  
The underscore (\_) represents a single number or character.  
The symbols can be used in combinations.

## Example

### Users table

| id | name       | email                  | encrypted_password | country |
|:---|:----------:|:----------------------:|:------------------:|:-------:|
| 1  | Jobs       | jobs@example.com       | dsfsfdssjnenvnnvfq | USA     |
| 2  | Page       | page@example.com       | kjfghdfsbernevnedr | USA     |
| 3  | Brin       | brin@example.com       | fajskfjnvdsnspnofe | USA     |
| 4  | Zuckerberg | zuckerberg@example.com | vncscsdvnksfdfjskw | USA     |
| 5  | Duda       | duda@example.com       | pqwiwcnnsaggkjfsad | Poland  |
| 6  | Higgins    | higgins@example.com    | ruernjvrtghvrtyklh | Ireland |
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
  country LIKE '%land'
;
```

#### Users table using like clause

| id | name       | email                  | encrypted_password | country |
|:---|:----------:|:----------------------:|:------------------:|:-------:|
| 5  | Duda       | duda@example.com       | pqwiwcnnsaggkjfsad | Poland  |
| 6  | Higgins    | higgins@example.com    | ruernjvrtghvrtyklh | Ireland |
