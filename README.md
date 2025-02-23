![Workflow Status](https://github.com/leonidz92/kittygram_final/actions/workflows/main.yml/badge.svg)

**Описание проекта**

Kittygram - это веб-приложение для обмена фотографиями и достижениями о домашних животных. Проект позволяет пользователям создавать учетные записи, загружать фотографии своих питомцев, добавлять достижения.

**Функционал:**

Регистрация и аутентификация пользователей.
Загрузка и просмотр фотографий котов.
Выбор достижений ваших питомцев.

**Стек технологий:**

Backend: Python, Django, Django REST Framework.
Frontend: React, Redux.
База данных: PostgreSQL.
Контейнеризация: Docker.
CI/CD: GitHub Actions.
Тестирование: Pytest.
Как развернуть проект

**Клонируйте репозиторий:**

git clone https://github.com/leonidz92/kittygram.git

Перейдите в директорию проекта:

cd kittygram

Создайте и активируйте виртуальное окружение:

python -m venv venv source venv/bin/activate # Для Linux/macOS venv\Scripts\activate # Для Windows

Установите зависимости:

pip install -r backend/requirements.txt

**Заполните файл .env с необходимыми переменными окружения. Пример:**

Создайте файл .env в корневой директории проекта и заполните его следующим образом:

```
POSTGRES_DB=kittygram 
POSTGRES_USER=kittygram_user 
POSTGRES_PASSWORD=kittygram_password 
DB_NAME=kittygram 
DB_HOST=db 
DB_PORT=5432 
 
SECRET_KEY='your_secret_key'
DEBUG=True 
ALLOWED_HOSTS=localhost,127.0.0.1
```

**Запустите проект локально:**

```
python manage.py migrate python manage.py runserver
```

Развертывание проекта в Docker

Заполните файл .env с необходимыми переменными окружения.

Соберите и запустите контейнеры:

```
docker-compose up --build
```

**Автор**

Проект разработал Зыков Леонид (https://github.com/leonidz92).
