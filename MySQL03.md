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
