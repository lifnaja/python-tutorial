# Loops


ใน python จะมี loops 2 แบบคือ `while` และ `for`

## while
while ใช้สำหรับการวนซ้ำเมื่อเงื่อนไขที่กำหนดยังคงเป็นจริง (True) โดยเหมาะกับสถานการณ์ที่จำนวนรอบไม่แน่นอน

ตัวอย่าง  prints 0,1,2,3,4

<div data-datacamp-exercise data-lang="python">
  <code data-type="sample-code">
    # Prints out 0,1,2,3,4

    count = 0
    while count < 5:
        print(count)
        count += 1  # This is the same as count = count + 1

  </code>
</div>


## for
for ใช้สำหรับการวนซ้ำตามจำนวนที่แน่นอน หรือเมื่อเราต้องการวนซ้ำผ่านรายการ (เช่น list, string, range)

ตัวอย่าง  prints 0,1,2,3,4

<div data-datacamp-exercise data-lang="python">
  <code data-type="sample-code">
    # Prints out 0,1,2,3,4

    for num in range(0,5):
        print(num)

  </code>
</div>

### for with dictionaries
for สามารถใช้ในการเข้าถึงข้อมูลของ dict ได้
โดยสามารถเข้าถึงเฉพาะ keys, values, หรือทั้ง key-value คู่ โดยใช้เมธอดต่าง ๆ เช่น .keys(), .values(), และ .items()

ตัวอย่างการวรซ้ำเฉาะ keys

<div data-datacamp-exercise data-lang="python">
  <code data-type="sample-code">
    data = {'name': 'Alice', 'age': 25, 'city': 'Bangkok'}

    # วนซ้ำผ่าน keys โดยตรง
    for key in data:
        print(key)

    # หรือใช้ .keys() ก็ได้
    for key in data.keys():
        print(key)
  </code>
</div>

ตัวอย่างการวรซ้ำเฉาะ values
<div data-datacamp-exercise data-lang="python">
  <code data-type="sample-code">
    data = {'name': 'Alice', 'age': 25, 'city': 'Bangkok'}

    for value in data.values():
        print(value)
  </code>
</div>


ตัวอย่างการวรซ้ำทั้ง key และ value
<div data-datacamp-exercise data-lang="python">
  <code data-type="sample-code">
    data = {'name': 'Alice', 'age': 25, 'city': 'Bangkok'}

    for key, value in data.items():
        print(key, value)
  </code>
</div>

### enumerate
เป็นฟังก์ชันที่ช่วยให้เราวนซ้ำผ่านลำดับข้อมูล (เช่น ลิสต์, สตริง หรือ tuple) โดยให้ค่าดัชนี (index) และค่าขององค์ประกอบในลำดับนั้นพร้อมกันในการวนซ้ำ

<div data-datacamp-exercise data-lang="python">
  <code data-type="sample-code">
    fruits = ['apple', 'banana', 'cherry']

    for index, fruit in enumerate(fruits):
        print(index, fruit)

  </code>
</div>


## "break" and "continue" statements
- continue: ใช้เพื่อข้ามไปยังรอบถัดไป
- break: ใช้เพื่อออกจากลูป

<div data-datacamp-exercise data-lang="python">
  <code data-type="sample-code">
    fruits = ['apple', 'banana', 'cherry']

    for num in range(10):
        if num == 3:
            continue
        elif num == 6:
            break

        print(num)

  </code>
</div>

## loops with else
else จะทำงาน เมื่อลูปทำงานครบโดยไม่มีการ break
else จะไม่ทำงาน เมื่อมีการใช้ break ออกจากลูปก่อนครบ

<div data-datacamp-exercise data-lang="python">
  <code data-type="sample-code">
    numbers = [1, 2, 3, 4, 5]
    target = 7

    for num in numbers:
        if num == target:
            print("พบค่า ", target)
            break
    else:
        print("ไม่พบค่า ", target)

  </code>
</div>
