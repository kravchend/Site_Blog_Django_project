# Django Blog

## О проекте

**Django Blog** — это простой сайт для ведения блога на Django. Пользователи могут регистрироваться, создавать и редактировать заметки, сохранять их как черновики или публиковать, а также просматривать опубликованные записи других пользователей.

## Основные возможности

- Регистрация и вход пользователей
- Создание, редактирование и удаление заметок
- Сохранение заметок как черновиков
- Публикация заметок
- Просмотр опубликованных заметок на главной странице блога

## Установка

1. Клонируйте репозиторий:
    ```bash
    git clone <https://github.com/kravchend/Site_Blog_Django_project>
    cd mysite
    ```

2. Создайте виртуальное окружение и активируйте его:
    ```bash
    python3 -m venv venv
    source venv/bin/activate
    ```

3. Установите зависимости:
    ```bash
    pip install -r requirements.txt
    ```

4. Примените миграции базы данных:
    ```bash
    python manage.py migrate
    ```

5. Создайте суперпользователя (по желанию):
    ```bash
    python manage.py createsuperuser
    ```

6. Запустите сервер разработки:
    ```bash
    python manage.py runserver
    ```

## Использование

- Перейдите по адресу [http://127.0.0.1:8000/](http://127.0.0.1:8000/)
- Зарегистрируйтесь и войдите в свой аккаунт
- Создавайте новые заметки и сохраняйте их как черновики или публикуйте
- Просматривайте список ваших черновиков и опубликованных заметок

## Требования

- Python 3.10+
- Django 5.2.1

## Лицензия

Проект распространяется под MIT License.

---

Если есть вопросы, пишите!