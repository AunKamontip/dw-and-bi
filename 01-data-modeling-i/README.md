# Data-Modeling-I 

 ### Building a Data Modeling with Postgres (SQL)

## Getting Started

```sh
python -m venv ENV
source ENV/bin/activate
pip install -r requirements.txt
```

### Prerequisite when install psycopg2 package

For Debian/Ubuntu users:

```sh
sudo apt install -y libpq-dev
```

For Mac users:

```sh
brew install postgresql
```

## Running Postgres

```sh
docker-compose up
```

To shutdown, press Ctrl+C and run:

```sh
docker-compose down
```

## Running ETL Scripts

```sh
python create_tables.py
python etl.py
```
## Project Structure
โฟลเดอร์ 01-data-modeling-i จัดเก็บไฟล์ 
```sh
docker-compose.yml : เป็นไฟล์การกำหนดค่าสำหรับ Docker Compose ใช้สำหรับการกำหนดคอนเทนเนอร์ของฐานข้อมูล PostgreSQL
create_table.py : เป็นสคริปต์ Python ที่ใช้สำหรับสร้างตารางในฐานข้อมูล PostgreSQL โดยใช้คำสั่ง SQL
etl.py : เป็นสคริปต์ Python ที่ใช้สำหรับกระบวนการ ETL 

ใช้โครงสร้างข้อมูลที่ได้รับการสร้างจากไฟล์ create_table.py หลังจากนั้น ไฟล์ etl.py จะทำการอ่านไฟล์ JSON และนำข้อมูลลงในฐานข้อมูล PostgreSQL 
โดยใช้การเชื่อมต่อกับฐานข้อมูลผ่าน psycopg2 ซึ่งเป็นไลบรารี Python ที่ใช้ในการจัดการกับฐานข้อมูล PostgreSQL ผ่าน Python
