# Functions
Functions เป็นวิธีที่สะดวกในการแบ่งโค้ด ออกเป็นบล็อก ช่วยให้เราสามารถจัดระเบียบโค้ด ทำให้โค้ดอ่านง่ายขึ้น ใช้ซ้ำได้




## การสร้าง Function
การสร้างฟังก์ชันใช้คำสั่ง `def` ตามด้วยชื่อฟังก์ชันและวงเล็บ () เช่น

```py  title="math_operations.py" linenums="1"
def sum_two_numbers(a, b):
    return a + b

sum_two_numbers(1, 3)
```



```py  title="math_operations.py" linenums="1"
def sum_two_numbers(a: int, b: int) -> int:
    return a + b

sum_two_numbers(1, 3)
```

## การสร้าง Function พร้อมค่าเริ่มต้น (Default Parameters)
```py  title="math_operations.py" linenums="1"
def sum_two_numbers(a: int, b: int = 0) -> int:
    return a + b

sum_two_numbers(1)
```

##  ฟังก์ชันแบบไม่กำหนดจำนวน Arguments
Python รองรับการส่ง arguments แบบไม่จำกัดจำนวนโดยใช้
 - `*args`  (Arguments)
 - `**kwargs` (Keyword Arguments) ใช้สำหรับรับค่าพารามิเตอร์ในรูปแบบ key-value จำนวนไม่จำกัดเมื่อเรียกใช้ฟังก์ชัน

```py  linenums="1"
def add_all(*args):
    return sum(args)

def print_info(**kwargs):
    for key, value in kwargs.items():
        print(f"{key}: {value}")

print(add_all(1, 2, 3, 4))

print_info(name="Alice", age=25, city="Bangkok")
```



หากฟังก์ชันรับ *args และ **kwargs ต้องจัดลำดับดังนี้:
```py  linenums="1"
def func(positional_args, *args, **kwargs)
    pass
```

ตัวอย่าง
```py  linenums="1"
def example_function(a, b, *args, **kwargs):
    print(f"a: {a}, b: {b}")
    print(f"args: {args}")
    print(f"kwargs: {kwargs}")

example_function(1, 2, 3, 4, name="Alice", age=25)
```
