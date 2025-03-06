# Basic Operators

## Arithmetic Operators

ใน python มีตัวดำเนินการบวก ลบ คูณ และหาร สามารถใช้งานกับตัวเลขได้

- `+`   Addition (บวก)

    ```py linenums="1"
    number = 5 + 3
    print(number)
    # 8
    ```

- `-`	Subtraction (ลบ)

    ```py linenums="1"
    number = 5 - 3
    print(number)
    # 2
    ```

- `*`	Multiplication (คูณ)

    ```py linenums="1"
    number = 5 * 3
    print(number)
    # 15
    ```

- `/`	Division (หารแบบทศนิยม)

    ```py linenums="1"
    number = 5 / 2
    print(number)
    # 2.5
    ```

- `//`	Floor Division (หารแบบปัดเศษลง)

    ```py linenums="1"
    number = 5 // 2
    print(number)
    # 2
    ```

- `%`	Modulus (หารเอาเศษ)

    ```py linenums="1"
    number = 5 % 2
    print(number)
    # 1
    ```

- `**`	Exponentiation (ยกกำลัง)

    ```py linenums="1"
    number = 5 ** 2
    print(number)
    # 25
    ```

## Comparison Operators

ใช้เปรียบเทียบค่าระหว่างตัวแปรและคืนค่าเป็น True หรือ False


- `==`      Equal to (เท่ากัน)	

    ```py linenums="1"
    result = 5 == 2
    print(result)
    # False
    ```

- `!=`      Not equal to (ไม่เท่ากัน)

    ```py linenums="1"
    result = 5 != 2
    print(result)
    # True
    ```

- `>`       Greater than (มากกว่า)

    ```py linenums="1"
    result = 5 > 2
    print(result)
    # True
    ```

- `<`       Less than (น้อยกว่า)

    ```py linenums="1"
    result = 5 < 2
    print(result)
    # False
    ```

- `>=`      Greater than or equal to (มากกว่าหรือเท่ากับ)

    ```py linenums="1"
    result = 5 >= 2
    print(result)
    # True
    ```

- `<=`      Less than or equal to (น้อยกว่าหรือเท่ากับ)

    ```py linenums="1"
    result = 5 <= 3
    print(result)
    # False
    ```

## Logical Operators

ใช้สำหรับทำงานกับค่าทางตรรกศาสตร์ (True / False)

- `and`     Returns True if both conditions are True

    ```py linenums="1"
    result = (10 > 5) and (5 < 10)
    print(result)
    # True
    ```

- `or`      Returns True if at least one condition is True

    ```py linenums="1"
    result = (5 > 3) or (10 < 5)
    print(result)
    # True
    ```

- `not`      Returns the opposite boolean value

    ```py linenums="1"
    result = not(5 > 3)
    print(result)
    # False
    ```
