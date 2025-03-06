# Dictionaries
โครงสร้างข้อมูลที่เก็บข้อมูลในรูปแบบคู่ของ key และ value ซึ่ง key ใช้ในการเข้าถึง value โดยสามารถเก็บข้อมูลหลายชนิดได้ (heterogeneous) และ key จะต้องไม่ซ้ำกัน

key : สามารถเป็นได้หลายชนิด: เช่น string, int, float, tuple
value: ค่าสามารถเป็นชนิดข้อมูลอะไรก็ได้

### ตัวอย่างการสร้าง dict
```py
my_dict = {"name": "Alice", "age": 30, "city": "Bangkok"}
print(my_dict)
```

### เข้าถึงค่าจาก key
```py
my_dict = {"name": "Alice", "age": 30, "city": "Bangkok"}
print(my_dict["name"])
print(my_dict["age"])
```

การใช้ get() เพื่อเข้าถึง value (ถ้า key ไม่มีจะคืนค่า None หรือค่าที่กำหนด)
```py
my_dict = {"name": "Alice", "age": 30, "city": "Bangkok"}
print(my_dict.get("city"))
print(my_dict.get("country", "Unknown"))
```

การเพิ่มข้อมูล การแก้ไขข้อมูล การลบ และการใช้ pop
```py
# การเพิ่มข้อมูล
my_dict["country"] = "USA"
print(my_dict)

# การแก้ไขข้อมูล
my_dict["age"] = 26
print(my_dict)

# การลบข้อมูล
del my_dict["city"]
print(my_dict)

# ใช้ pop() เพื่อลบและคืนค่าข้อมูล
age = my_dict.pop("age")
print(age)
print(my_dict)
```