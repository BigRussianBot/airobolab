### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1


# Уберём заросли!

## Step 1
Агенту необходимо уничтожить **8** блоков зарослей продвигаясь **вперёд**. Тут всего **16** линий зарослей которые необходимо уничтожить. Для уничтожение одной линии агенту необходимо использовать ``||agent:агент уничтожить вперёд||`` и ``||agent:агент переместиться вперёд||`` **8** раз.
#### ~ tutorialhint 
```blocks
player.onChat("очистка", function () {
    for (let index = 0; index < 8; index++) {
        for (let index = 0; index < 8; index++) {
        	
        }
    }
})

```

```ghost
player.onChat("очистка", function () {
    for (let index = 0; index < 8; index++) {
        agent.destroy(FORWARD)
        agent.move(FORWARD, 1)
        for (let index = 0; index < 2; index++) {
            agent.move(FORWARD, 1)
            agent.turn(RIGHT_TURN)
        }
    }
})
``` 
