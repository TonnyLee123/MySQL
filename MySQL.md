# Data_Type
- INT 
- DECIMAL(3, 2)
  - 總共: 3位數，2位小數點
- VARCHAR(100)
  - Variable Character 
  - 最多可存100字

- BLOB
  - Binary Large Object
  - Store large data

- DATE
  - 'YYYY-MM-DD'

- TIMESTAMP
  -  'YYYY-MM-DD' HH:MM:SS
  -  紀錄資料被insert的當下時間

# Create Table
- CREATE TABLE table_name (th_name, data_type, PRIMARY KEY, 等等);
- 注意: PRIMARY KEY
```sql
-- (column name and type)
CREATE TABLE my_first_table (
  student_id	INT PRIMARY KEY,
  name VARCHAR(15),
  major VARCHAR(15)
-- PRIMARY KEY(student_id) 
);
```
See Description
```sql
DESCRIBE my_first_table;
```

# Modify Table
ALTER TABLE table_name ADD/DROP... th_name th_data_type
```sql
ALTER TABLE my_first_table ADD gpa DECIMAL(3, 2);
ALTER TABLE my_first_table DROP column gpa;
```
# Delete Table
```sql
DROP TABLE my_first_table
```

# Insert data into table
- INSERT INTO table_name VALUE()

```sql
INSERT INTO my_first_table VALUE(
	1,
	'Tonny',
  'Biology'
);
```
