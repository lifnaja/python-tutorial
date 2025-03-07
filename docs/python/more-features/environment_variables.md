# Environment Variables

Environment Variables (ตัวแปรสภาพแวดล้อม) เป็นตัวแปรที่ถูกตั้งค่าไว้ในระบบปฏิบัติการและสามารถเข้าถึงได้จากโปรแกรม

## Using os.environ
```py linenums="1"
import os

home_path = os.environ.get("HOME")
python_path = os.environ.get("PYTHONPATH")

print("HOME:", home_path)
print("PYTHONPATH:", python_path)
```


## Using os.getenv()
```py linenums="1"
import os

api_key = os.getenv("API_KEY")
db_user = os.getenv("DB_USER", "default_user")
db_pass = os.getenv("DB_PASS", "default_pass")

print("API Key:", api_key)
print("Database User:", db_user)
print("Database Password:", db_pass)

```