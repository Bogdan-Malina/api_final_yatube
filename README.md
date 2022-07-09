# api_final

API, дающая возможность связывать приложения с Yatube для чтения и отправки данных.  


### Как запустить проект:

Клонировать репозиторий и перейти в него в командной строке:

```
https://github.com/Bogdan-Malina/api_final_yatube.git
```

```
cd api_final_yatube
```

Cоздать и активировать виртуальное окружение:

```
python3 -m venv env
```

```
source env/bin/activate
```

Установить зависимости из файла requirements.txt:

```
python3 -m pip install --upgrade pip
```

```
pip install -r requirements.txt
```

Выполнить миграции:

```
python3 manage.py migrate
```

Запустить проект:

```
python3 manage.py runserver
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
