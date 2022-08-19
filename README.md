### Описание:

Это учебный проект по Django Rest Framework, добавляющий API к функционалу Yatube

### Как запустить проект:

Клонировать репозиторий и перейти в него в командной строке:

```
git clone https://github.com/l33tm3s3ack/api_final_yatube.git
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

```
python3 -m pip install --upgrade pip
```

Установить зависимости из файла requirements.txt:

```
pip install -r requirements.txt
```

Выполнить миграции:

```
python3 yatube_api/manage.py migrate
```

Запустить проект:

```
python3 yatube_api/manage.py runserver
```
### Примеры API запросов.

GET запрос по этому адресу выдаст список всех публикаций на сайте:
```
http://127.0.0.1:8000/api/v1/posts/
```
POST запрос по нему же позволит создать еще одну публикацию:
{
  "text": "Your Text here",
  "group": "group id here",
}

GET запрос по адресу ниже выдаст все комментарии к указанному id публикации:
```
http://127.0.0.1:8000/api/v1/posts/{post_id}/comments/
```
