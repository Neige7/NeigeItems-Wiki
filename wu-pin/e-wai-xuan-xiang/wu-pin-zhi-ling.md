# 物品指令

## 路径

所有物品指令配置文件应存放于plugins/NeigeItems/Items文件夹

重复配置同一 ID 的物品不会导致报错，但可能互相覆盖

最后哪套指令活下来。。。随缘了属于是

## 配置

以默认指令配置为例

```
ExampleItem:
  left:
    console:
    - "say He's name is %player_name%"
    player:
    - "say My name is %player_name%"
  right: 
    console:
    - "say He's name is %player_name%"
    player:
    - "say My name is %player_name%"
  all: 
    console:
    - "say He's name is %player_name%"
    player:
    - "say My name is %player_name%"
```

* ExampleItem 即物品ID，对应ID的物品交互后将触发下列指令组
* left 左键行为将触发下方指令组
  * console 下列指令将由后台执行
  * player 下列指令将由玩家本人执行
* right 右键行为将触发下方指令组
* all 左/右键行为都将触发下方指令组
