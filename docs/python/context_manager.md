# Context Manager
เป็นเครื่องมือที่ช่วยให้เราจัดการทรัพยากรต่างๆ เช่น ไฟล์ การเชื่อมต่อฐานข้อมูล หรือการล็อก ได้อย่างปลอดภัย โดยไม่ต้องกังวลว่าจะลืมปล่อยทรัพยากรเหล่านั้นเมื่อใช้งานเสร็จสิ้น

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
