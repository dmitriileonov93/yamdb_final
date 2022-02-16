![yamdb_final workflow](https://github.com/dmitriileonov93/yamdb_final/actions/workflows/yamdb_workflow.yml/badge.svg)

### Описание
API YAMDB - API-приложение для обсуждений разных произведений.

Готовый проект: 84.252.142.100

### Запуск проекта
- Для загрузки введите в командную строку:
```
docker clone https://github.com/dmitriileonov93/yamdb_final.git
```
- Остановите все существующие контейнеры:
```
docker-compose stop
docker-compose rm web
```
- Создайте файл .env для переменных окружения в корневой папке проекта:
```
touch .env
```
- Добайте в этот файл переменные окруженмя:
```
echo <ПЕРЕМЕННАЯ>=<значение> >> .env
```
- Запуск приложения:
```
docker-compose up -d
```
- Применить миграции:
```
docker-compose exec web python manage.py migrate --noinput
```
- Создать суперпользователя:
```
docker-compose exec web python manage.py createsuperuser
```
- Собрать статику:
```
docker-compose exec web python manage.py collectstatic --no-input
```
- Заполнение БД тестовыми данными:
```
docker-compose exec web python manage.py loaddata fixtures.json
```
