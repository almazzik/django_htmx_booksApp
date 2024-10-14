# pull the official base image
FROM python:3.12.0-alpine

# set work directory
WORKDIR /usr/src/app

# set environment variables
# Не позволяет Python копировать файлы .pyc в контейнер
ENV PYTHONDONTWRITEBYTECODE 1

# Гарантирует, что вывод Python регистрируется в терминале,
# что позволяет отслеживать журналы Django в режиме реального времени.
ENV PYTHONUNBUFFERED 1

# install dependencies
RUN pip install --upgrade pip
COPY requirements.txt /usr/src/app
RUN pip install -r requirements.txt

# copy project
# Копирует весь исходный код проекта в рабочий каталог в контейнере.
COPY .. /usr/src/app

