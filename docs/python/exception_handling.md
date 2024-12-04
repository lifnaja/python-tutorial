# Exception handling
การข้อผิดพลาดที่เกิดขึ้นในระหว่างการทำงานของโปรแกรม โดยไม่ให้โปรแกรมหยุดทำงานทันที เมื่อเกิดข้อผิดพลาด (exception) ขึ้น เช่น การหารด้วยศูนย์

ตัวอย่างการใช้ try except
```py
try:
    x = 0
    y = 10 / x
    print(y)
except ZeroDivisionError:
    print("คุณไม่สามารถหารด้วยศูนย์ได้")
except TypeError:
    print("ตัวหารต้องเป็นตัวเลขเท่านั้น")
```


เราสามารถใช้ except หลายๆ อัน เพื่อจัดการกับข้อผิดพลาด หลายๆ แบบได้
```py
try:
    x = "0"
    y = 10 / x
    print(y)
except ZeroDivisionError:
    print("คุณไม่สามารถหารด้วยศูนย์ได้")
except TypeError:
    print("ตัวหารต้องเป็นตัวเลขเท่านั้น")
```

?? ถ้าเปลี่ยนค่า `x เป็น True จะเกิด exception อะไร 

### else, finally
- else: จะทำงานเมื่อโค้ดใน try ไม่มีข้อผิดพลาดเกิดขึ้น
- finally: จะทำงานเสมอหลังจาก try หรือ except ไม่ว่าจะเกิดข้อผิดพลาดหรือไม่

```py
try:
    num1 = 10
    num2 = 2
    result = num1 / num2
except ZeroDivisionError:
    print("ไม่สามารถหารด้วยศูนย์ได้.")
else:
    print(f"ผลลัพธ์: {result}")
finally:
    print("โปรแกรมเสร็จสิ้น.")
```



## Custom Exception

เราสามารถสร้าง exception ของตัวเองโดยการ extend จาก Exception class
```py
class CustomException(Exception):
    pass

try:
    raise CustomException("เกิดข้อผิดพลาดที่กำหนดเอง.")
except CustomException as e:
    print(f"Caught an error: {e}")
```
