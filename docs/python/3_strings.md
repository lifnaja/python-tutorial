# Strings & String Manipulation

Strings เป็นหนึ่งในประเภทข้อมูลพื้นฐานของ Python ที่ใช้เก็บข้อความ

## Creating Strings

```py linenums="1"
text1 = "Hello, World!"
text2 = 'Hello, World!'
text3 = """This is a 
multiline string"""
```

## String Indexing & Slicing
```py linenums="1"
text = "Hello, World!"

print(text[0])   # H
print(text[-1])  # !
print(text[0:5]) # Hello
print(text[:5])  # Hello (เริ่มจาก index 0)
print(text[7:])  # World! (ถึงตัวสุดท้าย)
```

## String Methods
- `lower`  แปลงเป็นตัวพิมพ์เล็ก
    ```py linenums="1"
    print("HELLO".lower())
    ```

-  `upper`  แปลงเป็นตัวพิมพ์ใหญ่
    ```py linenums="1"
    print("hello".lower())
    ```

- `strip`   ลบช่องว่างหัวท้าย
    ```py linenums="1"
    print(" hello ".strip())
    ```

- `replace` แทนที่ข้อความ
    ```py linenums="1"
    print("apple".replace("a", "o"))
    ```

- `split` แยกข้อความเป็น list
    ```py linenums="1"
    print("a,b,c".split(","))
    ```

- `join` รวม list เป็น string
    ```py linenums="1"
    print('"-".join(["a", "b", "c"])')
    ```

## String Formatting

-  `f-Strings`

    ```py linenums="1"
    name = "Alice"
    age = 25
    print(f"My name is {name} and I am {age} years old.")
    ```

- `.format()`

    ```py linenums="1"
    print("My name is {} and I am {} years old.".format(name, age))
    ```
