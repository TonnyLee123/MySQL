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
