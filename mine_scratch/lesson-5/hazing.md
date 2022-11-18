### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1


# Ловушка 

## Step 1
Агенту необходимо установить **Натяжной датчик** чтобы волки не смогли про так пройти. Установи в ``||agent:агент ставит блок||`` **Натяжной датчик**. Используй цикл ``||loops:пока||`` поставив правильное условие внутри.

#### ~ tutorialhint
Не забудь использовать **не** в своём условии!

```blocks
player.onChat("ловушка", function () {
    agent.setItem(TRIPWIRE, 64, 1)
    while (!(agent.detect(AgentDetection.Block, FORWARD))) {
    	
    }
})

``` 
```ghost
player.onChat("ловушка", function () {
    agent.setItem(TRIPWIRE, 64, 1)
    while (!(agent.detect(AgentDetection.Block, FORWARD))) {
        agent.place(DOWN)
        agent.move(FORWARD, 1)
    }
})
```
