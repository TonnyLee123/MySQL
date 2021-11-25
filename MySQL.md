# Data_Type
- INT 
- DECIMAL(9, 02)
  - 9.02
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
