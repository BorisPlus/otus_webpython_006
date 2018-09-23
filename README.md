# Kiosk Django App

Проект простого Интернет-магазина "КИОСК"

## Описание

Проект отображает список товаров и их атрибутов и состоит из трех сущностей:
* Товары
* Атрибуты
* Значение атрибутов у товаров

, что схематично можно представить ER-моделью (3NF) базы данных как
![KIOSK_ER_model](https://raw.githubusercontent.com/BorisPlus/otus_webpython_004/master/README.files/images/simple_ER_model.png "Title")
[скачать проект схемы БД в формате DbWrench](https://raw.githubusercontent.com/BorisPlus/otus_webpython_004/master/README.files/docs/db_wrench_project.xml "Title")

Если углубляться в реальные требования к подобному приложению, даже без реализации функционала осуществления заказов пользователем, то не хватает многого (в т.ч. по БД), например:
* Отнесение товаров к категории
* Иерархия категорий
* Дополнительные изображения товара
* Учет типов атрибутов (целое, строка, период, множественный выбор, состоящий из других атрибутов атрибут) и их форматированный вывод пользователю
* Назначение товару группы атрибутов и их значений
* Упорядочивание атрибутов и их групп у товаров
* Фильтрация товаров по атрибутам
* Архив товаров
* Скрытие товаров
* Цены на товары с их динамикой
* Еще много и много чего...

... но это выходит, как я понял, за рамки данного домашнего задания.

### Требования

Данный проект использует:
* Django 2

Установите:

```bash
$ pip3 install 'django>=2.0'
```

или

```bash
$ pip3 install -r requirements.txt
```

### Установка

```bash
$ cd <your_dir>
$ git clone git://github.com/BorisPlus/dummy_wsgi_framework.git
```

### Использование

В качетве базы данных в данном проекте выбрана SQLite, поскольку она лучше всего подходит для демонстратиции работоспособности приложения. 

Чтобы запустить проект выполните
```bash
python3 /<absolute_path>/kiosk/manage.py migrate
python3 /<absolute_path>/kiosk/manage.py createsuperuser --username=admin --email=admin@example.com
python3 kiosk/manage.py runserver
```
Перейдите по адресу http://127.0.0.1:8000

административная панель  http://127.0.0.1:8000/admin

### Демонстрационный вариант базы данных

С целью демонстрации функционирования Веб-приложения "КИОСК" были подготовленны сведения о товарах, атрибутах и их значениях с сайта Интернет-магазина "Мвидео" (не реклама)

### Cкриншоты


### Фичеризм реализации

#### Мой подход к реализации маршрутов

#### Мой подход к реализации представлений (Django Class Based Views)

#### Мой подход к реализации расширенных представлений полей моделей

#### Мой виджет в форме

## Авторы

* **BorisPlus** - [https://github.com/BorisPlus/otus_webpython_006](https://github.com/BorisPlus/otus_webpython_006)

## Лицензия

В рамках лицензии Django - https://github.com/django/django/blob/master/LICENSE

## Дополнительные сведения

Проект в рамках трехдневного домашнего задания курса "Web-разработчик на Python" на https://otus.ru/learning
