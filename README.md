# API Yatube
## Описание
API социальной сети Yatube.

Реализованный фунционал:
Просмотр, создание, редактирование, удаление статей и комментариев. Подписка и просмотр подписок на авторов. Просмотр групп сообщества.  Аутентификация по JWT-токену. 

## Как запустить проект
#### Клонировать репозиторий и перейти в него в командной строке:
```
https://github.com/bog2530/api_final_yatube.git
```

```
cd api_final_yatube
```

#### Cоздать и активировать виртуальное окружение:
```
python3 -m venv env
```

```
. env/bin/activate
```
#### Установить зависимости из файла requirements.txt:

```
python3 -m pip install --upgrade pip
```

```
pip install -r requirements.txt
```

#### Выполнить миграции:

```
python3 manage.py migrate
```

#### Запустить проект:

```
python3 manage.py runserver
```

## Некоторые примеры запросов к API.
http://127.0.0.1:8000/api/v1/posts/?limit=10&offset=14

GET
```
{
    "count": 123,  
    "next": "http://127.0.0.1:8000/api/v1/posts/?limit=10&offset=24",
    "previous": "http://127.0.0.1:8000/api/v1/posts/?limit=10&offset=4",
    "results": [
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

http://127.0.0.1:8000/api/v1/groups/

GET
```
[
    {
        "id": 0, 
        "title": "string", 
        "slug": "string", 
        "description": "string"
    }
]
```