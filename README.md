# Django Blog

## О проекте

**Django Blog** — это многофункциональный блог на Django, который позволяет пользователям вести собственные заметки, комментировать, искать, сортировать и получать актуальные подборки публикаций. Интуитивный интерфейс и современные возможности работы с контентом.

## Основные возможности

- **Блог**: комфортная платформа для публикации постов.
- **База данных(PostgreSQL)**: надёжное хранение данных о пользователях, постах, комментариях и тегах.
- **Заметки**: создание, редактирование и удаление личных и публичных записей.
- **Постраничная разбивка (pagination)**: удобная навигация по ленте постов.
- **Подключена почта**: отправка писем с постами и комментариями на email.
- **Комментарии**: пользователи могут комментировать публикации.
- **Тегирование**: возможность добавлять и использовать теги для поиска и группировки постов.
- **Рекомендации схожих постов**: отображение похожих записей на основе тегов.
- **Новостная лента**: список актуальных и популярных публикаций.
- **Поиск постов**: мгновенный поиск по записям блога.
- **Боковая панель**: отображение свежих или популярных постов сбоку основной ленты.

## Установка

1. **Клонируйте репозиторий:**
    ```bash
    git clone https://github.com/kravchend/Site_Blog_Django_project
    cd mysite
    ```
2. **Создайте виртуальное окружение и активируйте его:**
    ```bash
    python3 -m venv venv
    source venv/bin/activate
    ```
3. **Установите зависимости:**
    ```bash
    pip install -r requirements.txt
    ```
4. ** Настройка базы данных PostgreSQL**
    ```bash
   Для macOS:
   brew install postgresql
   brew services start postgresql
  
   Для Ubuntu/Debian:
   sudo apt update
   sudo apt install postgresql postgresql-contrib
   sudo service postgresql start
   
   **Создайте базу данных и пользователя**
   Войдите в терминале под пользователем : `postgres`
     sudo -u postgres psql
   Затем создайте базу данных и пользователя (замените `blog_db`, `blog_user` и `your_password` на ваши значения):
   CREATE DATABASE blog_db;
   CREATE USER blog_user WITH PASSWORD 'your_password';
   ALTER ROLE blog_user SET client_encoding TO 'utf8';
   ALTER ROLE blog_user SET default_transaction_isolation TO 'read committed';
   ALTER ROLE blog_user SET timezone TO 'UTC';
   GRANT ALL PRIVILEGES ON DATABASE blog_db TO blog_user;
   \q
    python manage.py migrate
    ```
   5. **Создайте суперпользователя (по желанию):**
       ```bash
       python manage.py createsuperuser
       ```

   6. **Обновите настройки подключения в файле `mysite/settings.py`**
      ```bash
      DATABASES = {
       'default': {
           'ENGINE': 'django.db.backends.postgresql',
           'NAME': 'blog_db',            # Имя вашей базы данных
           'USER': 'blog_user',          # Имя пользователя
           'PASSWORD': 'your_password',  # Пароль пользователя
           'HOST': 'localhost',          # Или другой адрес сервера БД
           'PORT': '5432',               # Порт PostgreSQL по умолчанию
           }
      }
      ```
   
7. **Установите пакет для работы с PostgreSQL**
Убедитесь, что в вашем окружении установлен пакет [psycopg2](https://pypi.org/project/psycopg2/):
   ```bash
    pip install psycopg2
    ```

8. **Запустите сервер разработки:**
    ```bash
    python manage.py runserver
    ```

## Использование

- Перейдите по адресу [http://127.0.0.1:8000/](http://127.0.0.1:8000/)
- Зарегистрируйтесь и войдите в свой аккаунт
- Создавайте, редактируйте и публикуйте заметки
- Добавляйте комментарии и обсуждайте новые посты
- Используйте теги и поиск для удобного доступа к нужной информации
- Просматривайте рекомендованные и свежие публикации в боковой панели

## Требования

- Python 3.13+
- Django 5.2.1

## Лицензия

Проект распространяется под [MIT License](LICENSE).

---

**Если возникнут вопросы — пишите!**

   Kravchend@gmail.com