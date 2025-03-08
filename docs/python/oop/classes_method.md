# Classes and Objects

## Instance Method
ใช้สำหรับ อ่าน/แก้ไขข้อมูลของ object

```py linenums="1"
class A():
    value = "123"

    def get_value(self):
        return self.value

a = A()
print(a.get_value())
```

## Class Method
ใช้สำหรับ อ่าน/แก้ไข Class Attribute

```py linenums="1"
class A():
    value = "123"

    @classmethod
    def set_value_with_cls(cls, value):
        cls.value = value

    def get_value(self):
        return self.value
    
    def set_value(self, value):
        self.value = value


a1 = A()
a2 = A()


print("set value `456` with out classmethod in object a1")
a1.set_value("456")
print(f"a1.value -> {a1.get_value()}")
print(f"a2.value -> {a2.get_value()}")

print("\n")

b1 = A()
b2 = A()
print("set value `c` with classmethod in object b1")
b1.set_value_with_cls("c")
print(f"b1.value -> {b1.get_value()}")
print(f"b2.value -> {b2.get_value()}")
```


## Static Method
ฟังก์ชันที่เกี่ยวข้องกับคลาส แต่ไม่ต้องใช้ข้อมูลของอ็อบเจ็กต์หรือคลาส

```py linenums="1"
class Employee:
    company = "TechCorp"

    @staticmethod
    def is_high_salary(salary):
        return salary > 50000
```
