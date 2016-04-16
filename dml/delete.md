# DELETE

## Syntax

```sql
DELETE FROM table_name
[WHERE conditions]
;
```

## Example

### Before delete
---

#### Users table

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
DELETE FROM Users
WHERE
  id = 5
  AND name = 'Ko'
;
```

### After delete
---

#### Users table

| id | name       | email                  | encrypted_password |
|:---|:----------:| :---------------------:|:------------------:|
| 1  | Jobs       | jobs@example.com       | dsfsfdssjnenvnnvfq |
| 2  | Page       | page@example.com       | kjfghdfsbernevnedr |
| 3  | Brin       | brin@example.com       | fajskfjnvdsnspnofe |
| 4  | Zuckerberg | zuckerberg@example.com | vncscsdvnksfdfjskw |
