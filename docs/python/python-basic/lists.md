# List and Tuples
List เป็นโครงสร้างข้อมูลชนิดหนึ่งใน Python ที่ใช้เก็บ ข้อมูลหลายค่าในตัวแปรเดียวกัน สามารถเก็บข้อมูลชนิดใดก็ได้ (String, Number, Boolean, Object ฯลฯ) และสามารถเปลี่ยนแปลงค่าได้ (Mutable)


## การสร้าง List

```py linenums="1"
# List ที่มีข้อมูลประเภทต่างๆ
numbers = [1, 2, 3, 4, 5]           # List ของตัวเลข
fruits = ["apple", "banana", "cherry"]  # List ของ string
mixed = [10, "Hello", True, 3.14]   # List ที่มีข้อมูลหลายประเภท

print(numbers)   # [1, 2, 3, 4, 5]
print(fruits)    # ['apple', 'banana', 'cherry']
print(mixed)     # [10, 'Hello', True, 3.14]
```


## การเข้าถึงค่าภายใน List

สามารถเข้าถึงสมาชิกใน list ได้โดยใช้ index (เริ่มต้นที่ 0)

```py linenums="1"
fruits = ["apple", "banana", "cherry"]

print(fruits[0])   # apple
print(fruits[1])   # banana
print(fruits[2])   # cherry
```

หากใช้ index ติดลบ จะนับจากท้ายสุดของ list
```py linenums="1"
print(fruits[-1])  # cherry
print(fruits[-2])  # banana
```


## การแก้ไขค่าใน List

```py linenums="1"
fruits = ["apple", "banana", "cherry"]
fruits[1] = "orange"  # เปลี่ยน 'banana' เป็น 'orange'

print(fruits)  # ['apple', 'orange', 'cherry']
```


## การเพิ่มค่าเข้า List

- append() → เพิ่มค่าที่ท้าย list
    ```py linenums="1"
    fruits.append("mango")
    print(fruits)  # ['apple', 'orange', 'cherry', 'mango']
    ```

- insert(index, value)
    ```py linenums="1"
    fruits.insert(1, "grape")
    print(fruits)  # ['apple', 'grape', 'orange', 'cherry', 'mango']
    ```

## การลบค่าออกจาก List

- remove(value) → ลบค่าที่กำหนด (ตัวแรกที่เจอ)
    ```py linenums="1"
    fruits = ["apple", "banana", "cherry", "orange"]
    fruits.remove("orange")
    print(fruits)  # ["apple", "banana", "cherry"]
    ```

- pop(index) → ลบค่าตาม index (ถ้าไม่ระบุ index จะลบตัวสุดท้าย)
    ```py linenums="1"
    fruits = ["apple", "banana", "cherry", "orange"]
    fruits.pop(2)  # ลบ index ที่ 2 ('cherry')
    print(fruits)  # ['apple', 'cherry', 'orange']
    ```

- del → ลบค่าตาม index หรือ ลบทั้ง list
    ```py linenums="1"
    fruits = ["apple", "banana", "cherry", "orange"]
    del fruits[1]  # ลบ index 1 ('banana')
    print(fruits)  # ['apple', 'cherry'. 'orange']

    del fruits  # ลบทั้ง list
    ```

- clear() → ล้างค่าทั้งหมด แต่ไม่ลบตัวแปร
    ```py linenums="1"
    fruits = ["apple", "banana", "cherry", "orange"]
    fruits.clear()
    print(fruits)  # []
    ```

## String Methods

- lowerlen(list)	หาจำนวนสมาชิกใน list
    ```py linenums="1"
    numbers = [3, 1, 4, 1, 5, 9, 2]
    ```

- lowerlist.sort()	เรียงลำดับสมาชิก (น้อย -> มาก, A -> Z)
    ```py linenums="1"
    numbers = [3, 1, 4, 1, 5, 9, 2]
    numbers.sort()
    ```

- lowerlist.reverse()	เรียงลำดับแบบกลับกัน
    ```py linenums="1"
    numbers = [3, 1, 4, 1, 5, 9, 2]
    numbers.reverse()
    ```

- lowerlist.count(value)	นับจำนวนครั้งที่ค่าปรากฏใน list
    ```py linenums="1"
    numbers = [3, 1, 4, 1, 5, 9, 2]
    print(numbers.count(1))  # 2
    ```

- lowerlist.index(value)	หาตำแหน่ง index ของค่าที่ระบุ
    ```py linenums="1"
    numbers = [3, 1, 4, 1, 5, 9, 2]
    print(numbers.index(5))  # 4
    ```


## Slicing

เป็นการตัดแบ่งหรือเลือกบางส่วนของ `list` หรือ `tuple` โดยใช้ ช่วง index และมีรูปแบบดังนี้:

```py
list[start:stop:step]
```

- start: index ของสมาชิกตัวแรกที่จะดึงออกมา (ค่าเริ่มต้นคือ 0)
- stop: index ของสมาชิกตัวสุดท้ายที่จะดึงออกมา (ค่าเริ่มต้นคือ index สุดท้าย)
- step: ระบุจำนวนขั้นที่ข้ามระหว่าง index (ค่าเริ่มต้นคือ 1)

ตัวอย่าง
```py linenums="1"
my_list = [1, 2, 3, 4, 5, 6, 7]

# ดึงสมาชิกตั้งแต่ตำแหน่งที่ 1 ถึงก่อนตำแหน่งที่ 4
print(my_list[1:4])
# ผลลัพธ์: [2, 3, 4]

# ดึงสมาชิกตั้งแต่ต้นจนถึงก่อนตำแหน่งที่ 3
print(my_list[:3])
# ผลลัพธ์: [1, 2, 3]

# ดึงสมาชิกตั้งแต่ตำแหน่งที่ 2 ไปจนถึงสุดท้าย
print(my_list[2:])
# ผลลัพธ์: [3, 4, 5, 6, 7]

# ดึงสมาชิกทุกตัวเว้น 2 ตัว
print(my_list[::2])
# ผลลัพธ์: [1, 3, 5, 7]

# ดึงสมาชิกย้อนกลับ
print(my_list[::-1])
# ผลลัพธ์: [7, 6, 5, 4, 3, 2, 1]
```

### String Indexing & Slicing

```py linenums="1"
text = "Hello, World!"

print(text[0])   # H
print(text[-1])  # !
print(text[0:5]) # Hello
print(text[:5])  # Hello (เริ่มจาก index 0)
print(text[7:])  # World! (ถึงตัวสุดท้าย)
```