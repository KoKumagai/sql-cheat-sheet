# INSERT

## Syntax

```sql
INSERT INTO table_name (column_name1, column_name2, column_name3, ...)
VALUES (value1, value2, value3, ...)
;
```
or
```sql
INSERT INTO table_name
VALUES (value1,value2,value3,...)
;
```

## Example

### Before insert
---

#### Users table

| id | name       | email                  | encrypted_password |
|:---|:----------:| :---------------------:|:------------------:|
| 1  | Jobs       | jobs@example.com       | dsfsfdssjnenvnnvfq |
| 2  | Page       | page@example.com       | kjfghdfsbernevnedr |
| 3  | Brin       | brin@example.com       | fajskfjnvdsnspnofe |
| 4  | Zuckerberg | zuckerberg@example.com | vncscsdvnksfdfjskw |

### Execute

```sql
INSERT INTO Users (id, name, email, encrypted_password)
VALUES (5, 'Ko', 'ko@example.com', 'qwertyuioplkjhgfds')
;
```
Or
```sql
INSERT INTO Users
VALUES (5, 'Ko', 'ko@example.com', 'qwertyuioplkjhgfds')
;
```

### After insert
---

#### Users table

| id | name       | email                  | encrypted_password |
|:---|:----------:| :---------------------:|:------------------:|
| 1  | Jobs       | jobs@example.com       | dsfsfdssjnenvnnvfq |
| 2  | Page       | page@example.com       | kjfghdfsbernevnedr |
| 3  | Brin       | brin@example.com       | fajskfjnvdsnspnofe |
| 4  | Zuckerberg | zuckerberg@example.com | vncscsdvnksfdfjskw |
| 5  | Ko         | ko@example.com         | qwertyuioplkjhgfds |
