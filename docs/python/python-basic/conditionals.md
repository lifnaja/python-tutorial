# conditionals

ใน Python, Condition  ที่ใช้ในการตรวจสอบค่าและตัดสินใจว่าจะทำอะไรในกรณีต่าง ๆ โดยใช้คำสั่ง เช่น if, elif, และ else


### IF
```py linenums="1"
x = 10
if x > 5:
    print("x is greater than 5")
```


### IF ELSE
```py linenums="1"
x = 10
if x > 5:
    print("x is greater than 5")
else
    print("x is less than 5")
```


### IF ELIF ELSE
```py linenums="1"
x = 7
if x > 10:
    print("x is greater than 10")
elif x > 5:
    print("x is greater than 5 but less than or equal to 10")
else:
    print("x is 5 or less")
```


### And-Or-Not
```py linenums="1"
x = 7
y = 10

# ใช้ `and`:
if x > 5 and y > 5:
    print("Both x and y are greater than 5")

# ใช้ `or`:
if x > 5 or y > 15:
    print("At least one of x or y is greater than 5")

# ใช้ `not`:
if not x > 10:
    print("x is not greater than 10")

```