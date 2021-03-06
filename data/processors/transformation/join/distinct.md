# ![Разность](../../../images/icons/joindata/join-diff_default.svg) Разность

Результирующий набор данных содержит записи основного набора, для которых по ключевым полям не найдено соответствий в присоединяемом наборе. В результирующем наборе присутствуют поля только основного набора. SQL-операторов аналогов данной операции нет.

Пример:

Для примера возьмем две таблицы. Персона - главная таблица и присоединяемою Город.

Главная таблица:

|Имя|Id города|
|:-|-:|
|Андрей|1|
|Леонид|2|
|Сергей|1|
|Григорий|4|

Присоединяемая таблица:

|Id|Город|
|-:|:-|
|1|Москва|
|2|Санкт-Петербург|
|3|Казань|

![Связь](./merge.svg)

Результирующая таблица:

|Имя|Id города|
|:-|-:|
|Григорий|4|
