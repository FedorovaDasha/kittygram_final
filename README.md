# Проект «Kittygram»😺😺😺

## _Описание проекта:_

#### **Проект _Kittygram_ дает возможность пользователям поделиться своим пушистым счастьем и рассказать о его достижениях!**
### _С собачками не входить !!!_ 😉
![This is an alt text.]( https://media.tenor.com/2ZyWBNo-3sQAAAAC/%D0%BC%D0%B8%D0%BB%D1%8B%D0%B9-%D0%BA%D0%BE%D1%82%D0%B8%D0%BA.gif "Mau-mau-mauuu")

### _Технологии:_

* Django REST
* Python 3.9
* Nginx
* Gunicorn
* Docker
* PostgreSQL
* Djoser
* Pillow

### _Возможности проекта:_
* Регистрация пользователей
* Возможность добавления/редактирования/удаления своих котиков
* Просмотр котиков других пользователей
* Возможность добавления фото любимца с указанием цвета
* Возможность добавления достижений котика

### _Запуск проекта из образов с Docker hub_
- Для запуска необходимо создать папку проекта, например _kittygram_ и перейти в нее:
```
mkdir kittygram
cd kittygram
```
- В папку проекта скачиваем файл _docker-compose.production.yml_ и запускаем его:
```
sudo docker compose -f docker-compose.production.yml up
```
Произойдет скачивание образов, создание и включение контейнеров, создание томов и сети.
- Проверяем доступность проекта по адресу:

https://mykittygram.sytes.net/

### _Запуск проекта локально из исходников GitHub_
- Клонируем себе репозиторий:
```
git clone git@github.com:FedorovaDasha/kittygram_final.git
```
- Выполняем запуск:
```
sudo docker compose -f docker-compose.yml up
```
- После запуска необходимо выполнить миграции и собрать статику бэкенда. Статика фронтенда собирается во время запуска контейнера, после чего он останавливается.
```
sudo docker compose -f [имя-файла-docker-compose.yml] exec backend python manage.py migrate

sudo docker compose -f [имя-файла-docker-compose.yml] exec backend python manage.py collectstatic

sudo docker compose -f [имя-файла-docker-compose.yml] exec backend cp -r /app/collected_static/. /static/static/
```
- Проверяем доступность проекта по адресу:

http://localhost:9000/

##
### _Демо-версия проекта:_
[Kittygram](https://mykittygram.sytes.net)ᓚᘏᗢ

##
#### _Индикатор состояния рабочего процесса workflow:_

![example workflow](https://github.com/FedorovaDasha/kittygram_final/actions/workflows/main.yml/badge.svg)

##
Над проектом работала [FedorovaDasha](https://github.com/FedorovaDasha).

##