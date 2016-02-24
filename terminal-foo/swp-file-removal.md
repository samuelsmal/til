---
tags: terminal, vim, swp, find
created_on: 2016-02-24
updated_on: 2016-02-24
---

How to interactivly remove all `swp` files in the current its children directories:

```
find . -name '*.swp' -exec rm -i '{}' \;
```
