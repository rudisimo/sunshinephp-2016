# MySQL Server Performance Tuning 101
> by: [Ligaya Turmelle][1]  
> [https://legacy.joind.in/16770][2]

## Preface

### Step 0

* Tune your OS first
  * Filesystem
  * Network
* Under allocate your memory resources
* Optimize your queries/database schema

### Memory Allocation

```
Global Memory + (Max Connections * Per Connection Buffers)
```

### Settings

```sql
SHOW GLOBAL VARIABLES;
SELECT * FROM INFORMATION_SCHEMA.GLOBAL_STATUS;
SELECT * FROM PERFORMANCE_SCHEMA.GLOBAL_STATUS; /* MySQL 5.7 */
```

## Tuning

### InnoDB

#### `innodb_buffer_pool_size`

* Max value: Documentation 80% ;Suggested 60-70%

#### `innodb_log_file_size`

* Larger the log file, the less checkpoint activity (**good**)
* Larger the log file, longer recovery time (**bad**)

#### `innodb_file_per_table`

* Default value: Off <= 5.6.5 > On
* Easier to reclaim space
* TRUNCATE  for a table is faster
* Can store specific tables on different storage devices


[1]: https://twitter.com/lig
[2]: https://legacy.joind.in/16770
