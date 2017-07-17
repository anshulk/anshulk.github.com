---
layout: page
title: How to delete multiple keys from redis using cli
---

***Note to self***

This is how you delete multiple keys matching a pattern from redis -

```sh
redis-cli KEYS "prefix:*" | xargs redis-cli DEL
```

[source](https://stackoverflow.com/a/4006575/3476344)
