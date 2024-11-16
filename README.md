Бейджик успешного Workflow:
![Workflow Status (https://github.com/leonidz92/kittygram/actions/workflows/main.yml/badge.svg)](https://github.com/leonidz92/kittygram/actions)

Как работать с репозиторием финального задания

Описание проекта

Kittygram - это веб-приложение для обмена фотографиями и историями о домашних животных. Проект позволяет пользователям создавать учетные записи, загружать фотографии своих питомцев, оставлять комментарии и взаимодействовать с другими участниками сообщества.

Функционал:
- Регистрация и аутентификация пользователей.
- Загрузка и просмотр фотографий котов.
- Выбор достижений ваших питомцев.

Стек технологий:
- Backend: Python, Django, Django REST Framework.
- Frontend: React, Redux.
- База данных: PostgreSQL.
- Контейнеризация: Docker.
- CI/CD: GitHub Actions.
- Тестирование: Pytest.

Как развернуть проект

1. Клонируйте репозиторий:
git clone https://github.com/leonidz92/kittygram.git

2. Перейдите в директорию проекта:
cd kittygram

3. Создайте и активируйте виртуальное окружение:
python -m venv venv
source venv/bin/activate       # Для Linux/macOS
venv\Scripts\activate          # Для Windows

4. Установите зависимости:
pip install -r backend/requirements.txt

5. Заполните файл .env с необходимыми переменными окружения. Пример:
SECRET_KEY=your_secret_key
DEBUG=True
DB_NAME=your_db_name
DB_USER=your_db_user
DB_PASSWORD=your_db_password
DB_HOST=db_host
DB_PORT=db_port

6. Запустите проект локально:
python manage.py migrate
python manage.py runserver


Как проверить работу с помощью автотестов

1. В корне репозитория создайте файл tests.yml со следующим содержимым:
repo_owner: ваш_логин_на_гитхабе
kittygram_domain: полная ссылка (https://доменное_имя) на ваш проект Kittygram
taski_domain: полная ссылка (https://доменное_имя) на ваш проект Taski
dockerhub_username: ваш_логин_на_докерхабе

2. Скопируйте содержимое файла .github/workflows/main.yml в файл kittygram_workflow.yml в корневой директории проекта.
3. Для локального запуска тестов создайте виртуальное окружение, установите в него зависимости из backend/requirements.txt и запустите в корневой директории проекта pytest.
pytest


Чек-лист для проверки перед отправкой задания

- Проект Taski доступен по доменному имени, указанному в tests.yml.
- Проект Kittygram доступен по доменному имени, указанному в tests.yml.
- Пуш в ветку main запускает тестирование и деплой Kittygram, а после успешного деплоя вам приходит сообщение в Telegram.
- В корне проекта есть файл kittygram_workflow.yml.

**Как заполнить env**

Создайте файл `.env` в корневой директории проекта и заполните его следующим образом:
```
POSTGRES_DB=kittygram
POSTGRES_USER=kittygram_user
POSTGRES_PASSWORD=kittygram_password
DB_NAME=kittygram
DB_HOST=db
DB_PORT=5432

SECRET_KEY='django-insecure-cg6*%6d51ef8f#4!r3*$vmxm4)abgjw8mo!4y-q*uq1!4$-89$'
DEBUG=True
ALLOWED_HOSTS=localhost,127.0.0.1,ldkittygram.zapto.org
```

**Автор**

Проект разработал [Зыков Леонид](https://github.com/leonidz92).