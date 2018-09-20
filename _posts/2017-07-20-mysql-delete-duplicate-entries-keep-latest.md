---
layout: page
title: How to delete duplicate entries from MySQL keeping only latest entry
image: /image/a1.png
description: This is how you delete duplicate entries from MySQL keeping only latest entry
---

***Note to self***

This is how you delete duplicate entries from MySQL keeping only latest entry -

```sql
DELETE FROM test
WHERE id NOT IN (
  SELECT a.max_id FROM (
    SELECT MAX(id) as max_id FROM test GROUP BY email
  ) a
)
```

[source 1](https://stackoverflow.com/questions/6107167/mysql-delete-duplicate-records-but-keep-latest)
[source 2](https://stackoverflow.com/questions/45494/mysql-error-1093-cant-specify-target-table-for-update-in-from-clause)
