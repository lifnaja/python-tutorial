# Context Manager
เป็นเครื่องมือใน Python ที่ใช้จัดการ ทรัพยากร เช่น ไฟล์, database connection, network socket ให้ปิดหรือคืนค่าโดยอัตโนมัติหลังจากใช้งานเสร็จ โดยที่เราไม่ต้องจัดการเอง

ตัวอย่างการเปิดไฟล์ แบบไม่ใช้ context manager

```py
file = open("my_file.txt", "r")

# อ่านข้อมูลจากไฟล์
data = file.read()

# ทำงานกับข้อมูล
print(data)

# ปิดไฟล์
file.close()
```

ตัวอย่างการเปิดไฟล์ แบบใช้ context manager
```py
with open("my_file.txt", "r") as file:
    data = file.read()
    print(data)
```


### ข้อดีของ with

ไฟล์จะถูกปิดอัตโนมัติแม้เกิดข้อผิดพลาด ลดโอกาสเกิด Resource Leak โค้ดอ่านง่ายขึ้น
