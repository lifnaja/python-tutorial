# Select Subset data

ในส่วนนี้จะใช้ข้อมูลจาก [titanic data](https://github.com/pandas-dev/pandas/blob/main/doc/data/titanic.csv)


## Select columns

![select_colums](../images/select_specific_columns.png "select_colums")


```py linenums="1"
import pandas as pd
titanic = pd.read_csv("data/titanic.csv")

ages = titanic["Age"]
```

### Select multiple columns
```py linenums="5"
age_sex = titanic[["Age", "Sex"]]
```

## Filter rows

![select_rows](../images/filter_specific_rows.png "select_rows")

ตัวอย่าง การ filter ข้อมูลที่ `age` > 35
```py linenums="6"
age_above_35 = titanic[titanic["Age"] > 35]
```

ตัวอย่างการ filter ข้อมูลใน rows หลายเงื่อนไข
```py linenums="7"
class_2_3 = titanic[(titanic["Pclass"] == 2) | (titanic["Pclass"] == 3)]

# หรือสามารถรวม 2 condition ได้แบบนี้
class_2_3 = titanic[titanic["Pclass"].isin([2, 3])]
```

### Select specific rows and columns

![select_rows_columns](../images/select_specific_rows_and_columns.png "select_rows_columns")


ตัวอย่าง การเลือกข้อมูล `Name` ที่ `Age` มากกว่า 35
```py  linenums="11"
adult_names = titanic.loc[titanic["Age"] > 35, "Name"]
```