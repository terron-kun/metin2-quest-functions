# loop_timer()
Функция **loop_timer** создает цикличный таймер, привязанный к персонажу.

## Параметры функции
### timer_name
Тип *string*. **Обязательный параметр**. Имя таймера. Должно начинаться с латинской буквы. Может содержать только латиницу, нижние прочерки и числа.

### time
Тип *number*. **Обязательный параметр**. Количество секунд, по прошествии которых сработает таймер.

## Примечания
Функция **не** может быть вызвана анонимно.

Обратите внимание на то, что после выхода из игры и после телепортации таймер будет обнулён.

В отличие от функции [timer](../global/timer.md)(), эта функция вызывает триггер [timer](../_triggers/timer.md) бесконечное количество раз. После того, как на таймере заканчивается время, он запускается по новой.