# CREATE TABLE

## Syntax

```sql
CREATE TABLE table_name
(
  column_name1 data_type [constraint],
  column_name2 data_type [constraint],
  column_name3 data_type [constraint],
  ...
  [optional]
)
;
```

## Example

### Create users table(MySQL)
---

```sql
CREATE TABLE Users
(
  id INT NOT NULL AUTO_INCREMENT,
  name VARCHAR(80) NOT NULL,
  email VARCHAR(50) NOT NULL,
  encrypted_password VARCHAR(300) NOT NULL,
  PRIMARY KEY (id),
  UNIQUE INDEX (email)
)
;
```

### After create
---

#### Users table

| id | name       | email                  | encrypted_password |
|:---|:----------:| :---------------------:|:------------------:|
|    |            |                        |                    |
