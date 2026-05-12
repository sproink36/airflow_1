# Сгенерировать один раз
python -c "import secrets; import base64; print(base64.urlsafe_b64encode(secrets.token_bytes(32)).decode())"

полученное значение установить в AIRFLOW__CORE__FERNET_KEY

после выполнить:
    docker-compose up airflow-init
    docker-compose up
    docker-compose down -v
    docker build . --tag extending_airflow:latest
        проверить версию на https://downloads.apache.org/spark/ для
            RUN wget https://downloads.apache.org/spark/spark-3.5.8/spark-3.5.8-bin-hadoop3.tgz
    docker compose up -d --no-deps --build airflow-apiserver airflow-scheduler
    docker compose down
    docker-compose up

из https://github.com/bryzgaloff/airflow-clickhouse-plugin взять содержимое airflow-clickhouse-plugin
    и положить в dags
    папки clickhouse_data и config удалить