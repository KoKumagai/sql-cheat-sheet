# UPDATE

## Syntax

```sql
UPDATE table_name
SET
  column_name1 = value1,
  column_name2 = value2,
  ...
[WHERE conditions]
;
```

## Example

### Before update
---

#### Users table

| id | name       | email                  | encrypted_password |
|:---|:----------:| :---------------------:|:------------------:|
| 1  | Jobs       | jobs@example.com       | dsfsfdssjnenvnnvfq |
| 2  | Page       | page@example.com       | kjfghdfsbernevnedr |
| 3  | Brin       | brin@example.com       | fajskfjnvdsnspnofe |
| 4  | Zuckerberg | zuckerberg@example.com | vncscsdvnksfdfjskw |
| 5  | Kyoo       | kyoo@example.com       | qwertyuioplkjhgfds |

### Execute
---

```sql
UPDATE Users
SET
  name  = 'Ko',
  email = 'ko@example.com'
WHERE
  id = 5
;
```

### After update
---

#### Users table

| id | name       | email                  | encrypted_password |
|:---|:----------:| :---------------------:|:------------------:|
| 1  | Jobs       | jobs@example.com       | dsfsfdssjnenvnnvfq |
| 2  | Page       | page@example.com       | kjfghdfsbernevnedr |
| 3  | Brin       | brin@example.com       | fajskfjnvdsnspnofe |
| 4  | Zuckerberg | zuckerberg@example.com | vncscsdvnksfdfjskw |
| 5  | Ko         | ko@example.com         | qwertyuioplkjhgfds |
