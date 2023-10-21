## api_final - API, дающая возможность связывать приложения с Yatube для чтения и отправки данных.  


### Как запустить проект:

Клонировать репозиторий и перейти в него в командной строке:

```
git clone https://github.com/Bogdan-Malina/api_final_yatube.git
```

```
cd api_final_yatube
```

Cоздать и активировать виртуальное окружение:

```
python -m venv venv
```

```
source venv/bin/activate
```

Установить зависимости из файла requirements.txt:

```
python -m pip install --upgrade pip
```

```
pip install -r requirements.txt
```

Выполнить миграции:
```
cd yatube_api
```
```
python manage.py makemigrations
```
```
python manage.py migrate
```

Запустить проект:
```
python manage.py runserver
```
### Примеры запросов

Получение публикаций (GET на /api/v1/posts/):

```
{

    "count": 123,
    "next": "http://api.example.org/accounts/?offset=400&limit=100",
    "previous": "http://api.example.org/accounts/?offset=200&limit=100",
    "results": 

[

        {
            "id": 0,
            "author": "string",
            "text": "string",
            "pub_date": "2021-10-14T20:41:29.648Z",
            "image": "string",
            "group": 0
        }
    ]

}
```
Создание публикации (POST на /api/v1/posts/)
```
{

    "text": "string",
    "image": "string",
    "group": 0

}
```
```
{

    "id": 0,
    "author": "string",
    "text": "string",
    "pub_date": "2019-08-24T14:15:22Z",
    "image": "string",
    "group": 0

}
```

### Автор
Данил Воронин https://github.com/Bogdan-Malina
