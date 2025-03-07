# Exception handling
Exception Handling คือการจัดการข้อผิดพลาดที่เกิดขึ้นขณะรันโปรแกรม เพื่อป้องกันไม่ให้โปรแกรมหยุดทำงานกะทันหัน

Python มีการจัดการข้อผิดพลาดด้วย try-except ซึ่งช่วยให้เราสามารถจัดการกับ Exception ที่เกิดได้

## try except
ตัวอย่างการใช้ try except
```py linenums="1"
try:
    x = 0
    y = 10 / x
    print(y)
except ZeroDivisionError:
    print("คุณไม่สามารถหารด้วยศูนย์ได้")
```


เราสามารถใช้ except หลายๆ อัน เพื่อจัดการกับข้อผิดพลาด หลายๆ แบบได้
```py linenums="1"
try:
    x = "0"
    y = 10 / x
    print(y)
except ZeroDivisionError:
    print("คุณไม่สามารถหารด้วยศูนย์ได้")
except TypeError:
    print("ตัวหารต้องเป็นตัวเลขเท่านั้น")
```

**Question**
ถ้าเปลี่ยนค่า `x` เป็น True ที่เป็น type boolean โปรแกรมจะเกิด error ?

### else, finally
- else: จะทำงานเมื่อโค้ดใน try ไม่มีข้อผิดพลาดเกิดขึ้น
- finally: จะทำงานเสมอหลังจาก try หรือ except ไม่ว่าจะเกิดข้อผิดพลาดหรือไม่

```py linenums="1"
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

เราสามารถสร้าง exception ของตัวเองโดยการ extend จาก class Exception
```py
class CustomException(Exception):
    pass

try:
    raise CustomException("เกิดข้อผิดพลาดที่กำหนดเอง.")
except CustomException as e:
    print(f"Caught an error: {e}")
```
