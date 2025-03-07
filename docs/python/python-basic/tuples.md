# Tuples
Tuple เป็นโครงสร้างข้อมูลที่คล้ายกับ List แต่มีคุณสมบัติที่ เปลี่ยนแปลงค่าไม่ได้ (Immutable) เมื่อสร้างแล้ว ไม่สามารถเพิ่ม, ลบ หรือแก้ไขค่าได้

## การสร้าง Tuple

```py linenums="1"
numbers = (1, 2, 3, 4, 5)  
fruits = ("apple", "banana", "cherry")  
mixed = (10, "Hello", True, 3.14)  

print(numbers)   # (1, 2, 3, 4, 5)
print(fruits)    # ('apple', 'banana', 'cherry')
print(mixed)     # (10, 'Hello', True, 3.14)
```

## การเข้าถึงค่าภายใน Tuple

ใช้ index เหมือน list (เริ่มจาก 0)

```py linenums="1"
fruits = ("apple", "banana", "cherry")

print(fruits[0])   # apple
print(fruits[1])   # banana
print(fruits[2])   # cherry

# ใช้ index ติดลบ
print(fruits[-1])  # cherry
print(fruits[-2])  # banana
```


## การเพิ่มค่าเข้า Tuple

เนื่องจาก tuple ไม่สามารถเพิ่มค่าตรงๆ ได้ แต่สามารถทำได้โดย นำ tuple มาต่อกัน

```py linenums="1"
fruits = ("apple", "banana")
new_fruits = fruits + ("cherry",)

print(new_fruits)  # ('apple', 'banana', 'cherry')
```