# Big Data Spark

Процесс формирования снежинки был перенесён в Spark, все csv файлы парсятся и редактируются внутри Jupyter Notebook'а и 
потом записываются в PostgreSQL базу данных.

Затем были реализованы 6 Data Mart'ов, записываемых в базу данных ClickHouse:
1) datamart_products
2) datamart_customers
3) datamart_seasonal
4) datamart_stores
5) datamart_suppliers
6) datamart_product_quality

Инструкция:
1) Запустить Docker: `docker-compose up`
2) Подключиться к Jupyter Notebook'у через `localhost:8888` с токеном: `77b1e2a0561f125aafe62686a954b64f33a00e5c81b99700`
3) Открыть файл `./work/spark_snowflake.ipynb` и запустить все ячейки
4) Открыть файл `./work/spark_datamarts.ipynb` и запустить все ячейки
5) Запустить DBeaver и подключиться к PostgreSQL (порт `5433`) и ClickHouse (порт `18123`) по логинам и паролям: `postgres:admin` и `default:admin` соответственно. Для ClickHouse необходимо подключиться к базе данных `datamarts`.