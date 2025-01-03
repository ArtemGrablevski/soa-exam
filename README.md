# Auction & notfication services

## Использованные технологии:
- Python
- FastAPI (фреймворк для разработки REST API)
- FastStream (фреймворк для работы с очередями сообщений)
- Pydantic для валидации данных
- PostgreSQL
- RabbitMQ
- SQLALchemy (Python ORM) & alembic (инструмент для миграций БД)
- locust для нагрузочного тестирования
- Docker & docker compose
- Swagger UI (интерактивная документация к REST API)
- Git VSC

## Запуск по шагам:
1) Запуск RabbitMQ
- Перейдите в папку rabbitmq:
```
cd rabbitmq
```
- Создайте `.env` файл по примеру файла `.env.example`
- Запустите RabbitMQ:
```
docker compose up --build
```
2) Запуск сервиса auction-service
- Перейдите в папку auction-service:
```
cd auction-service
```
- Создайте `.env` файл по примеру файла `.env.example`
- Запустите docker:
```
docker compose up --build
```
- SwaggerUI будет доступен по адресу `http://127.0.0.1:8000/api/docs`
3) Запуск сервиса notification-service
- Перейдите в папку notification-service:
```
cd notification-service
```
- Создайте `.env` файл по примеру файла `.env.example`
- Соберите и запустите docker образ:
```
docker compose up --build
```
- SwaggerUI будет доступен по адресу `http://127.0.0.1:8000/docs`
