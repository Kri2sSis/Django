# Вытаскиваем базовый образ
FROM python:3.7-slim

# Устанавливаем переменные среды
ENV PYTHONDONTWRITEBYTECODE 1
ENV PYTHONUNBUFFERED 1

# Настраиваем рабочий каталог
WORKDIR /code

# Устанавливаем зависимости
RUN pip install pipenv
COPY Pipfile Pipfile.lock /code/
RUN pipenv install --system

# Копируем проект
COPY . /code/