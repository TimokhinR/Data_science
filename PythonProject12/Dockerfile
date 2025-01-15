FROM python:3.9-slim

RUN pip install redis

RUN pip install flask

EXPOSE 5000

RUN apt-get update && apt-get install -y redis-server

COPY . /app
WORKDIR /app

RUN pip install -r requirements.txt

# Запуск Redis сервера та програми
CMD service redis-server start && python app.py
