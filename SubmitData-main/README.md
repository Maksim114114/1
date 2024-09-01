# Pereval
Итоговое задание (HW-03)

Приложение для походов и покорителей вершин. Позволяет делиться своими подъемами, описанием местности, добавление фотографий и координат объектов.

Этап 1

Создание базы данных.

public - основные модели приложения

gallery - модели для отображения фото пользователей

profiles - модели профеля пользователя 

media - тут храгятся фото пользователей

Создание класса по работе с данными, с помощью которого добавлены новые значения в таблицу перевалов.
Написание REST API, который вызывает метод из класса по работе с данными.

SubmitDataList - все данные о перевалах

SubmitDataDetail - детально оперевале

Этап 2
Добавлено ещё три метода:

GET /submitData/<slug>/ — получить одну запись (перевал) по её slug. 

PATCH /submitData/<int:pk>/ — редактирование существующей записи, если она в статусе new. Редактировать можно все поля, кроме тех, что содержат в себе ФИО, адрес email и номер телефона. Метод принимает тот же самый json, который принимал уже реализованный метод submitdatalist. Возвращаются 2 значения: status и message. 

PATCH /delete-pereval/<int:pk>/ - удаление данных о перевале

GET /submitData/ — список данных обо всех объектах, которые зарегестрированный пользователь с почтой отправил на сервер.

Этап 3

Добавление в Readme.md документации к REST API

Документация с помощью Swagger

http://127.0.0.1:8000/swagger/

Покрыть код тестами

tests.py