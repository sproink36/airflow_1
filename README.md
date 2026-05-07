# Сгенерировать один раз
python -c "import secrets; import base64; print(base64.urlsafe_b64encode(secrets.token_bytes(32)).decode())"

полученное значение установить в AIRFLOW__CORE__FERNET_KEY

после выполнить:
    docker-compose up airflow-init
    docker-compose up