# item.get_limit()
Функция **item.get_limit** сообщает требования, необходимые для использования предмета.

## Параметры функции
### limit_index
Тип *number*. **Обязательный параметр**. В `player.item_proto` есть поля `limittype0`, `limitvalue0`, `limittype1` и `limitvalue1`. В качестве этого параметра надо указать число, идущее после названия необходимых полей, которые надо получить. Допустим, если вы хотите получить информацию о первой паре полей (`limittype0` и `limitvalue0`), то в качестве параметра надо указать `0`.

## Возвращаемые значения
### limits
Тип *mixed*. В случае, если предмет не был &laquo;выделен&raquo;, то ничего не возвращается, то бишь `nil`.

Если параметр не является числом или если параметр меньше `0` или больше `1`, то возвращается `0` <sup>number</sup>.

Если функция выполнилась без ошибок, то возвращается таблица, которая выглядит примерно так: `{limittype, limitvalue}`. `limittype` &mdash; это тип ограничения, а `limitvalue` &mdash; значение ограничения.

## Примечания
Функция **не** может быть вызвана анонимно.

Существуют следующие типы ограничений:

| limittype | Название | Назначение |
| --- | --- | --- |
| 0 | LIMIT_NONE | Нет ограничений |
| 1 | LIMIT_LEVEL | Ограничение по минимальному уровню |
| 2 | LIMIT_STR | Ограничение по минимальному количеству силы |
| 3 | LIMIT_DEX | Ограничение по минимальному количеству подвижности |
| 4 | LIMIT_INT | Ограничение по минимальному количеству интеллекта |
| 5 | LIMIT_CON | Ограничение по минимальному количеству здоровья (не путать с HP) |
| 6 | LIMIT_PCBANG | неизвестно |
| 7 | LIMIT_REAL_TIME | неизвестно |
| 8 | LIMIT_REAL_TIME_START_FIRST_USE | неизвестно |
| 9 | LIMIT_TIMER_BASED_ON_WEAR | неизвестно |
| 10 | LIMIT_MAX_NUM | неизвестно |Эта функция работает только с &laquo;выделенными&raquo; предметами. Подробнее тут: [item](../item).