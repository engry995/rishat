Тестовое задание для ООО Ришат
==============================
Простой сервер Django + Stripe API бэкенд


Реализовано:
-----------
 - страницы /buy/{id} и /item/{id} с требуемыми функциями
 - страница /item/ со списком всех товаров и возможностью перехода на страницу каждого товара
 - просмотр товаров в админ панели django, создание нового товара с синхронным созданием товара и его цены на stripe.com
 - ключи от API Stripe подключаются через переменные окружения
 

Порядок запуска проекта
-----------------------

1.  Зарегистрироваться и получить ключи от API Stripe.com
     - Зарегистрироваться на [странице регистрации stripe.com](https://dashboard.stripe.com/register)
     - Подтвердить свой e-mail
     - Перейти на страницу Settings -> [Account details](https://dashboard.stripe.com/settings/account). Задать имя аккаунта.
     - Ключ для API можно посмотреть на странице Developers -> [API keys](https://dashboard.stripe.com/test/apikeys) в разделе Standard keys -> Secret key


2. Скопировать файлы проекта
    ```commandline
    git clone https://github.com/denis2603/rishat
    ```
    Эта команда создаст папку `rishat`  и сохранит в ней все требуемые файлы.
   

3. Установить зависимости:
    ```commandline
    pip install -r requirements.txt
    ```
    *Рекомендуется настроить [виртуальное окружение](https://docs.python.org/3/library/venv.html).*


4. Переименовать файл `.env.template` в `.env`, указать в нем полученные ключи от Stripe API  
SECRET_DJANGO_KEY изменить на свой или оставить без изменения

Пример файла `.env`:
```dotenv
SK_STRIPE_KEY='sk_test_51Lhx3GECEws------------------------------------------------------------'
PK_STRIPE_KEY='pk_test_51Lhx3GECEws------------------------------------------------------------'
SECRET_DJANGO_KEY='django-insecure-----------------------------------------'
```

5. 