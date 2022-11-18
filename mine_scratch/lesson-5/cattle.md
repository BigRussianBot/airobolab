### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1


# Скотоводство

## Step 1
Посмотри на код который уже написан и попробуй запустить его. Он позволяет управлять движением агента без подсчёта блоков. Посмотри какой путь должен пройти агент чтобы достичь **золотого блока** и правильно запрограммируй его повороты.

```template
player.onChat("овцы", function () {
    while (!(agent.detect(AgentDetection.Block, FORWARD))) {
        agent.move(FORWARD, 1)
    }
    agent.turn(LEFT_TURN)
})

``` 

