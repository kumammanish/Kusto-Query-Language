# now()

Returns the current UTC clock time, optionally offset by a given timespan.
This function can be used multiple times in a statement and the clock time being referenced will be the same for all instances.

<!-- csl -->
```
now()
now(-2d)
```

**Syntax**

`now(`[*offset*]`)`

**Arguments**

* *offset*: A `timespan`, added to the current UTC clock time. Default: 0.

**Returns**

The current UTC clock time as a `datetime`.

`now()` + *offset* 

**Example**

Determines the interval since the event identified by the predicate:

<!-- csl -->
```
T | where ... | extend Elapsed=now() - Timestamp
```
