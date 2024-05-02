# Analytics Engineering 

 ### สร้าง Analytics Workflow ด้วย dbt และการนำเอาแนวคิด Analytics Engineering มาใช้


เปิด file 06-analytics-engineering

```sh
cd  06-analytics-engineering 
```
รันเพื่อเปิดการใช้งานเชื่อมต่อกับการใช้งาน postgres บน dbt 
```sh
docker compose up
```
เชื่อมต่อกับการใช้งาน postgres บน dbt ได้ที่ port 3000 และ sign in เข้าระบบ

เปิดการใช้ virtual env
```sh
$ python -m venv ENV
$ source ENV/bin/activate
```
ติดตั้งการงาน dbt กับ postgres
```sh
pip install dbt-core dbt-postgres
```
สร้าง  dbt project
```sh
dbt init
```
(สร้าง project , dbname , host ,pass , port , shchema , threads , type , user)


แก้ไข the dbt profiles --> folder ds525 --> folder model ---> สร้าง file profiles.yml (เอา code ที่ได้มาเก็บไว้)

```sh
code ~/.dbt/profiles.yml
```

Test การเชื่อมต่อกับ dbt

```sh
dbt debug
```
You should see "All checks passed!". <-- ถ้า check แล้ว ok 

code dbt 
create models
```sh
dbt run
```
To test models
```sh
dbt test
```