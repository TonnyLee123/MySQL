### Build connection between Python and MySQL.
```python
import mysql.connector

myDB = mysql.connector.connect(
    host = 'localhost',
    user = 'root',
    passwd = 'sql123'
)

print(myDB)
```

### Create table via py
- Cursor: Object that communicates with entire SQL server
- 想成: 在Python和MySQL之間，傳遞各種指令的司機。
***
- .execute("SQL指令")
```python
myCursor = myDB.cursor()
myCursor.execute("CREATE DATABASE my_second_schema")
```

### 查看目前有的DataBase
- 這裡的Cursor可以儲存來自execute()產生的值
```python
myCursor = myDB.cursor()
myCursor.execute("SHOW DATABASES")

for db in myCursor:
    print(db)
```

### 輸入一筆資料到Table
INSERT INTO table_name(th_name, th_name) VALUES (%s, %s)", (1, 'Tonny', 20)
```python
myCursor.execute("INSERT INTO students(student_id, name, age) VALUES (%s, %s, %s)", (1, 'Tonny', 20))

# commit後，才會執行任何改變(如insert)
myDB.commit()
```

### 一次輸入多筆資料
用**executemany**執行多筆資料
```python
sqlFormula = "INSERT INTO students(name, age, major) VALUES (%s, %s, %s)"
students = [
    ('甲', 23, 'x'),
    ('乙', 93, 'y'),
    ('丙', 53, 'z')
]
myCursor.executemany(sqlFormula, students)

myDB.commit()
```
### 讀取資料
.fetchall() 獲取SQL執行的資料
```python
myCursor.execute('SELECT * FROM students')

# 創建一個var儲存資上行在sql執行所獲的資料
result = myCursor.fetchall()

for row in result:
    print(row)
```
