# Домашнее задание к занятию "`Базы данных`" - `Потапов Василий`

### Легенда
Заказчик передал вам файл в формате Excel, в котором сформирован отчёт.

На основе этого отчёта нужно выполнить следующие задания.

### Задание 1
Опишите не менее семи таблиц, из которых состоит база данных:

какие данные хранятся в этих таблицах;
какой тип данных у столбцов в этих таблицах, если данные хранятся в PostgreSQL.
Приведите решение к следующему виду:

Сотрудники (

идентификатор, первичный ключ, serial,
фамилия varchar(50),
...
идентификатор структурного подразделения, внешний ключ, integer).

### Ответ 1

![Название скриншота 1](https://github.com/mistermedved01/hw-12-01/blob/main/img/bd_red03.jpg)

База данных может состоять из следующих таблиц:

Сотрудники (

- Код сотрудника, первичный ключ, serial

- ФИО, varchar(50)

- Дата_трудоустройства, (date)

- Код_структур_подразд, smallint, внешний ключ Структурное подразделение (Код_структур_подразд)

- Код_должность, smallint, внешний ключ Должность (Код_должность)

- Код_филиала, smallint, внешний ключ Филиалы (Код_филиала)

- Код_текущего_проекта, smallint, внешний ключ Проекты (Код_проекта)

- Код_оклад, money, внешний ключ Должность (Оклад)

Структурное подразделение (

- Код_структур_подразд, первичный ключ, serial

- Название_тип_подразделения, varchar(50)

- Тип_подразделения, smallint, внешний ключ Тип структурного подразделения (Код_тип_структур_подразд) )

Тип структурного подразделения (

- Код_тип_структур_подразд, первичный ключ, serial

- Название_типа_структур_подрзад, varchar(20))

Должность (

- Код_должность, первичный ключ, serial

- Название_должности, varchar(50)

- Оклад, money

- Код_структур_подразд, varchar(50), внешний ключ Структурное подразделения (Код_структур_подзрад))

Филиалы (

- Код_филиала, первичный ключ, serial

- Адрес_id, smallint, внешний ключ Адреса (Код_адреса)

- Код_области, smallint, внешний ключ Адреса (Область))

Адреса (

- Код_адреса, первичный ключ, serial

- Область, varchar(50)

- Город, varchar(50)

- Улица, varchar(100)

- Номер_дома, varchar (30))

Проекты (

- Код_проекта, первичный ключ, serial

- Название_проекта, varchar(100))
