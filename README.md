![my workflow](https://github.com/dmitriileonov93/yamdb_final/actions/workflows/yamdb_workflow.yml/badge.svg)

API YAMDB - API-приложение для обсуждений разных произведений.

Как запустить проект:
1. Для загрузки введите в командную строку: "docker pull dimaleonov93/yamdb_final"
2. Остановите все существующие контейнеры: "sudo docker-compose stop"
                                           "sudo docker-compose rm web"
3. Создайте файл .env для переменных окружения: "touch .env"
4. Добайте в этот файл переменные окруженмя: "echo <ПЕРЕМЕННАЯ>=<значение> >> .env"
5. Запуск приложения: терминале выполнить команду "docker-compose up -d"
6. Применить миграции: "docker-compose exec web python manage.py migrate --noinput"
7. Создать суперпользователя: "docker-compose exec web python manage.py createsuperuser"
8. Собрать статику: "docker-compose exec web python manage.py collectstatic --no-input"
9. Заполнение БД тестовыми данными: "docker-compose exec web python manage.py loaddata fixtures.json"