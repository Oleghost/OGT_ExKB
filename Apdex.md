
https://its.1c.ru/db/metod8dev/content/5807/hdoc

**Apdex** - **Application Performance Index**

APDEX = (NS + NT/2)/N
N - общее количество выполнений
NS - количество выполнений с временем отклика от 0 до T
NT - количество выполнений с временем отклика от T до 4T

## Шкала APDEX:

| от   | до   | Оценка            |
| ---- | ---- | ----------------- |
| 0.00 | 0.50 | неприемлемо       |
| 0.50 | 0.70 | очень плохо       |
| 0.70 | 0.85 | удовлетворительно |
| 0.85 | 0.94 | хорошо            |
| 0.94 | 1.00 | отлично           |

## Методика APDEX 

Оценка производительности системы по методике APDEX состоит из следующих основных этапов:

- [Получить список ключевых операций](https://its.1c.ru/db/content/metod8dev/src/developers/scalability/methods/i8105807.htm#apdex_1)
- [Определить приоритет каждой операции](https://its.1c.ru/db/content/metod8dev/src/developers/scalability/methods/i8105807.htm#apdex_2)
- [Определить целевое время для каждой операции](https://its.1c.ru/db/content/metod8dev/src/developers/scalability/methods/i8105807.htm#apdex_4)
- [Собрать информацию о времени выполнения каждой ключевой операции](https://its.1c.ru/db/content/metod8dev/src/developers/scalability/methods/i8105807.htm#apdex_4)
- [На основании собранных данных получить оценку APDEX](https://its.1c.ru/db/content/metod8dev/src/developers/scalability/methods/i8105807.htm#apdex_5)

1. Опросить пользователей / заказчиков, выяснить какие операции для них самые важные
2. Адекватный вариант, если конфигурация приближена к типовым 5-3-8 (проведение - открытие форм - оперативный отчет)
3. С помощью ТЖ события CALL. Собрать контекстные вызовы.