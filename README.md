# Yamdb_final
![example workflow](https://github.com/YablokovaIrina/yamdb_final/blob/master/.github/workflows/yamdb_workflow.yml)

## Описание проекта:
Проект YaMDb собирает отзывы пользователей на произведения. Сами произведения в YaMDb не хранятся, здесь нельзя посмотреть фильм или послушать музыку.   
Произведения делятся на категории, а также им может быть присвоен жанр из списка предустановленных (например, «Сказка», «Рок» или «Артхаус»).  
Благодарные или возмущённые пользователи оставляют к произведениям текстовые отзывы и ставят произведению оценку в диапазоне от одного до десяти; из пользовательских оценок формируется усреднённая оценка произведения — рейтинг.
Пользователи могут оставлять комментарии к отзывам.


### Как запустить проект:
Клонировать репозиторий и перейти в него в командной строке:

```
git clone git@github.com:YablokovaIrina/yamdb_final.git
```

```
$ cd infra
```

Запустить

```
$ docker-compose up -d --build
```

Выполнить миграции 

```
$ docker-compose exec web python manage.py makemigrations
$ docker-compose exec web python manage.py migrate
```

Создать суперпользователя

```
$ docker-compose exec web python manage.py createsuperuser
```

Собрать статику

```
$ docker-compose exec web python manage.py collectstatic --no-input
```

Остановить контейнеры

```
$ docker-compose down -v
```

Шаблон наполнения .env (не включен в текущий репозиторий) расположенный по пути infra/.env

```
DB_ENGINE=django.db.backends.postgresql
DB_NAME=postgres
POSTGRES_USER=postgres
POSTGRES_PASSWORD=postgres
DB_HOST=db
DB_PORT=5432
```

Документация: http://127.0.0.1/redoc/

### Использованные технологии:
Python 3.9  
Django 3.2  
DRF  
Docker


### Авторы проекта:
[Яблокова Ирина](https://github.com/YablokovaIrina) 
