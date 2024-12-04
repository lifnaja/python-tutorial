# Importing Modules

โมดูลใน Python คือไฟล์ python ที่มีนามสกุล .py ชื่อของโมดูลจะเหมือนกับชื่อไฟล์นั้น ๆ โดยในโมดูล Python สามารถมี functions, classes, หรือ variables ที่ถูกกำหนดและใช้งานได้ภายในไฟล์นั้น.

The example above includes two files:
ตัวอย่าง จะมี python 2 ไฟล์

```sh
project/
├── math_operations.py
├── main.py
```

```py  title="math_operations.py" linenums="1"
def add(a: int, b: int) -> int:
    return a + b

def subtract(a: int, b: int) -> int:
    return a - b
```

```py title="main.py" linenums="1"
import math_operations

result = math_operations.add(5, 3)
print(result)
```
