### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1


# Куриный Переворот

## Этап 1
Агенту необходимо поставить сверху **2** слоя из **9** блоков **Железной Решётки**. Всего **4** стены, которые необходимо построить из **Железной Решётки**. Не забудьте использовать ``||agent:агент переместиться вверх||`` чтобы поставить второй слой.

#### ~ tutorialhint
В конце у вас должно получить **3** вложенных друк в друга блока ``||loops:повторить|``. Перед запуском проверь что у агента достаточно блоков.

```ghost
player.onChat("курицы", function () {
    for (let index = 0; index < 2; index++) {
        agent.setItem(IRON_BARS, 1, 1)
        for (let index = 0; index < 4; index++) {
            for (let index = 0; index < 9; index++) {
                agent.place(DOWN)
                agent.move(FORWARD, 1)
            }
            agent.turn(RIGHT_TURN)
        }
        agent.move(UP, 1)
    }
})

``` 
