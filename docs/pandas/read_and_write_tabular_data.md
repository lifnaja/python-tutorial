# Read and Write tabular data

pandas สามารถอ่านข้อมูลจากไฟล์ได้หลายประเภท เพื่อนำมาวิเคราห์


![dataframe](../images/read_and_write_tabular.png "dataframe")


ตัวอย่าง อ่านข้อมูลจาก csv

```py linenums="1"
titanic = pd.read_csv("data/titanic.csv")
```

ตัวอย่าง เขัยนข้อมูล dataframe เป็น csv
```py linenums="2"
titanic.to_csv("file_name.csv")
```