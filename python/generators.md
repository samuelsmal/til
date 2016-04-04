```
import random

def die_roller(throws):
    """generates throws rolls of a die"""
    for _ in xrange(throws):
        yield random.randint(1, 6)

roller = die_roller(10)
print type(roller)      # => <type 'generator'>
print list(roller)      # => [6, 6, 3, 1, 6, 3, 1, 5, 4, 4]
print sum(roller)       # roller was exhausted, generates null list thus 0 sum

big_roller = die_roller(10**5)
print sum(big_roller)   # => 3500238
```

Source: http://stackoverflow.com/a/2660574


