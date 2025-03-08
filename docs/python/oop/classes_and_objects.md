# Classes and Objects

Objects คือการรวบรวมตัวแปรและฟังก์ชันเข้าไว้ในหน่วยเดียวกัน วัตถุจะได้รับตัวแปรและฟังก์ชันมาจาก Classes ซึ่ง Classes ทำหน้าที่เป็น template สำหรับการสร้าง Objects


ตัวอย่างการสร้าง class และ object

```py linenums="1"
class ชื่อคลาส:
    # ตัวแปรของ class (class attributes)
    ตัวแปร = ค่าเริ่มต้น

    # คอนสตรัคเตอร์ (constructor)
    def __init__(self, พารามิเตอร์):
        # ตัวแปรของ object (instance attributes)
        self.ตัวแปร = ค่า

    # เมธอด (self, methods)
    def ชื่อเมธอด(self):
        # พฤติกรรมของ object
        pass
```


- `__init__` คือ constructor ใน Python ซึ่งเป็น method พิเศษที่ถูกเรียกโดยอัตโนมัติเมื่อมีการสร้าง object ใหม่จาก class หนึ่ง ๆ
- `self` ใน Python, self เป็นตัวแทนของ object ปัจจุบัน (current instance) ที่ใช้เรียก method หรือ attributes ของ object นั้น ๆ


### ตัวอย่าง Class Cat

- มี constructor `__init__` ที่รับชื่อ (name) และสี (color) เป็นพารามิเตอร์
- มี method meow ที่ให้แมวร้องเสียง "Meow!"


```py linenums="1"
class Cat:
    def __init__(self, name, color):
        self.name = name
        self.color = color

    def meow(self):
        print(self.name, "says Meow!")


cat1 = Cat("Kitty", "Black")
cat2 = Cat("Mittens", "White")

# เข้าถึง attributes
print(cat1.name)
print(cat2.color)

# เรียกใช้ method
cat1.meow()
cat2.meow()
```


## Inheritance
 การสืบทอดจากคลาสแม่

```py linenums="1"
# คลาสแม่ (Parent class)
class Animal:
    def __init__(self, name):
        self.name = name

    def speak(self):
        print(self.name, " makes a sound.")

# คลาสลูก (Child class) สืบทอดจาก Animal
class Cat(Animal):
    def __init__(self, name, color):
        super().__init__(name)
        self.color = color

    def speak(self):
        print(self.name, " says Meow!")

# สร้าง object จากคลาสลูก
cat1 = Cat("Buddy", "White")

# เรียกใช้เมธอดจากคลาสแม่
cat1.speak()  # Buddy says Meow!
```

### Multiple Inheritance
การสืบทอดจากหลายคลาสใน Python สามารถทำได้โดยการระบุหลายคลาสในลำดับการสืบทอด (separated by commas) เมื่อคุณสร้างคลาสลูก (child class) ซึ่งจะสืบทอดคุณสมบัติและเมธอดจากคลาสทั้งสอง

```py linenums="1"
# คลาสแม่ 1
class A:
    def show(self):
        return "A"

class B():
    def show(self):
        return "B"

class C(B, A):
    pass

obj = C()
print(obj.show())  # B
```
