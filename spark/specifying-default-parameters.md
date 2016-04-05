---
tags: spark
created_on: 2016-04-05
updated_on: 2016-04-05
---

Goal: To specify default packages used for `spark-submit`.

Reason: Testing is hard without this - not really possible when you rely on
some packages.

Create a file `spark-defaults.conf` in the directory from where you call spark
(to keep it project based). But the following string in it, the packages are
comma separated.

```
spark.jars.packages com.databricks:spark-csv_2.10:1.4.0
```
