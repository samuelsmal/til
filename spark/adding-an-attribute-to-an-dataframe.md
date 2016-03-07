---
tags: spark, python
created_on: 2016-03-07
updated_on: 2016-03-07
---

[Source](http://stackoverflow.com/a/30992905)

```
from pyspark.sql import Row

df.rdd.map(lambda row: Row(**dict(row.asDict(), day=row.date_time.day)))
```

Another option is to register a function and run SQL query:

```
sqlContext.registerFunction("day", lambda x: x.day)
sqlContext.registerDataFrameAsTable(df, "df")
sqlContext.sql("SELECT *, day(date_time) as day FROM df")
```

Finally you can define udf like this:

```
from pyspark.sql.functions import udf
from pyspark.sql.types import IntegerType

day = udf(lambda date_time: date_time.day, IntegerType())
df.withColumn("day", day(df.date_time))
```
