# TRUNCATE TABLE

## Syntax

```sql
TRUNCATE TABLE table_name
;
```

## Example

### Users table

| id | name       | email                  | encrypted_password | country |
|:---|:----------:|:----------------------:|:------------------:|:-------:|
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
TRUNCATE TABLE Users
;
```

### After truncate
---

#### Users table

| id | name       | email                  | encrypted_password | country |
|:---|:----------:|:----------------------:|:------------------:|:-------:|
|    |            |                        |                    |         |
