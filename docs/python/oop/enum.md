## Enum

Enum (Enumeration) เป็น ประเภทข้อมูลพิเศษ ใน Python ใช้สร้าง ชุดค่าคงที่ ที่อ่านง่ายและเข้าใจง่าย

- ใช้แทน ค่าคงที่ (Constants) ที่มีความหมาย
- ทำให้โค้ด อ่านง่ายขึ้น แทนการใช้ตัวเลขหรือตัวอักษรธรรมดา
- ป้องกันข้อผิดพลาดจากการใช้ค่าผิดพลาด


```py linenums="1"
from enum import Enum

class Color(Enum):
    RED = 1
    GREEN = 2
    BLUE = 3

print(Color.RED)
print(Color.RED.name)
print(Color.RED.value)
```

การใช้ Enum กับเงื่อนไข

```py linenums="11"
def get_color_name(color):
    if color == Color.RED:
        return "This is Red"
    elif color == Color.GREEN:
        return "This is Green"
    elif color == Color.BLUE:
        return "This is Blue"
    else:
        return "Unknown Color"

print(get_color_name(Color.GREEN))
```