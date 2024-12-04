# Virtual Environment

Virtual Environment หรือ สภาพแวดล้อมเสมือน ใน Python คือเครื่องมือที่ใช้เพื่อสร้างแยกสภาพแวดล้อมการพัฒนา (development environment) สำหรับโปรเจคหนึ่งๆ โดยไม่ให้กระทบกับระบบ Python หรือโปรเจคอื่นที่อาจใช้งาน Python เดียวกันอยู่ การใช้ Virtual Environment ช่วยให้คุณสามารถติดตั้งไลบรารีและเครื่องมือที่ต้องการแยกออกจากกันตามโปรเจค

## การสร้างและใช้งาน Virtual Environment

- การสร้าง Virtual Environment
```bash
python -m venv .venv
```

    - `.venv`: ชื่อของ Virtual Environment ที่จะถูกสร้าง

- การเปิดใช้งาน Virtual Environment
    - Windows:
    ```bash
    .venv\Scripts\activate
    ```

    - macOS หรือ Linux:
    ```bash
    source .venv/bin/activate
    ```

    เมื่อเปิดใช้งานแล้วจะเห็นชื่อ Virtual Environment แสดงอยู่ใน prompt เพื่อยืนยันว่าใช้งาน Virtual Environment แล้ว (เช่น (.venv))

- การติดตั้งไลบรารีใน Virtual Environment
```bash
pip install httpx
```

- การยกเลิกการใช้งาน Virtual Environment
```bash
deactivate
```

## เครื่องมือในการจัดการ dependencies
 - [poetry](https://python-poetry.org/)
 - [uv](https://github.com/astral-sh/uv)
