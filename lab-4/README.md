# Лабораторная работа 4

> Нагрузочное тестирование БД

Задачи:
- Написать скрипт, заполняющий БД большим количеством тестовых данных, рекомендуется использовать [faker.js](https://github.com/faker-js/faker).
- Измерить время выполнения запросов, написанных в ЛР3.
  - Проверить для числа записей:
     - 100 записей в каждой табличке
     - 1.000 записей
     - 1.0000 записей
     - 1.000.000 записей
     - можно больше.
  - Все запросы выполнять с фиксированным ограничением на вывод (LIMIT), т.к. запросы без LIMIT всегда будет выполняться O(n) от кол-ва записей
  - Проверить влияние сортировки на скорость выполнения запросов.
  - Для измерения использовать фактическое (не процессорное и т.п.) время. Для node.js есть [console.time и console.timeEnd](https://nodejs.org/api/console.html#console_console_time_label).
- Добавить в БД индексы (хотя бы 5 штук). Измерить влияние (или его отсутствие) индексов на скорость выполнения запросов. Обратите внимание на:
  - Скорость сортировки больших табличек
  - Скорость JOIN