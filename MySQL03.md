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

### 輸入資料到Table
INSERT INTO table_name(th_name, th_name) VALUES (%s, %s)", (1, 'Tonny', 20)
```python
myCursor.execute("INSERT INTO students(student_id, name, age) VALUES (%s, %s, %s)", (1, 'Tonny', 20))

# commit後，才會執行任何改變(如insert)
myDB.commit()
```
