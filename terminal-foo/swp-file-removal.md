---
tags: terminal, vim, swp, find
created_on: 2016-02-24
updated_on: 2016-02-24
---

# Method 1

How to interactively remove all `swp` files in the current its children directories:

```
find . -name '*.swp' -exec rm -i '{}' \;
```

# Method 2

If the directories do not contain any white space in their names you can also use this:

```
rm -i `find . | grep .swp$`
```
