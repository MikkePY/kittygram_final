Kittygram 

[![Main Kittygramm workflow](https://github.com/MikkePY/kittygram_final/actions/workflows/main.yml/badge.svg?branch=main)](https://github.com/MikkePY/kittygram_final/actions/workflows/main.yml)

Описание 
Проект о домашних питомцах, в котором можно зарегистрироваться и добавлять питомцев, необходимо указать имя и год рождения питомца, а так же добавить фотографию и указать его умения. 

Технологии 

Python - язык программирования. 
Django - свободный фреймворк для веб-приложений на языке Python. 
Django REST Framework - мощный и гибкий набор инструментов для создания веб-API. 
Simple JWT - плагин аутентификации JSON Web Token для Django REST Framework. 
Gunicorn 20.1.0 
Фронтенд-приложение на React 
npm 9.5.1 
База данных - SQLite3 
Docker 
DockerHub 
CI/CD 
GitHub Actions 
PostgreSQL 
Docker network

Запуск проекта 

Клонировать репозиторий и перейти в него в командной строке: 
git clone https://github.com/MikkePY/kittygram_final 

cd kittygram_final 
В корне проекта создать файл .env и прописать в него свои данные. Пример: 
POSTGRES_DB=kittygram 
POSTGRES_USER=kittygram_user 
POSTGRES_PASSWORD=kittygram_password 

Запустить проект через docker-compose: 
docker compose -f docker-compose.yml up 

Выполнить миграции: 
docker compose -f docker-compose.yml exec backend python manage.py migrate 

Создать суперюзера: 
sudo docker compose -f docker-compose.yml exec backend python manage.py createsuperuser 
Собрать статику и скопировать ее: 

docker compose -f docker-compose.yml exec backend python manage.py collectstatic 
docker compose -f docker-compose.yml exec backend cp -r /app/static_backend/. /backend_static/static/ 

Автор 
- Cоколов Михаил