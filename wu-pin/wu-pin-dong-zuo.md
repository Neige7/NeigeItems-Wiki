# 物品动作

## 简介

通过左键/右键使用物品，触发一系列指令组（支持papi变量）

可自定义每次是否消耗物品、消耗的物品数量、物品冷却、左键/右键触发

## 路径

所有物品动作配置文件应存放于plugins/NeigeItems/ItemActions文件夹

重复配置同一 ID 的物品不会导致报错，但可能互相覆盖

最后哪套动作活下来。。。随缘了属于是

## 配置

以默认指令配置为例

```
ExampleItem:
  consume:
    cooldown: 3000
    amount: 1
    left: true
    right: true
  left:
  - "console: say He's name is %player_name%"
  - "command: say My name is %player_name%"
  right: 
  - "console: say He's name is %player_name%"
  - "command: say My name is %player_name%"
  all: 
  - "console: say He's name is %player_name%"
  - "command: say My name is %player_name%"
ExampleItem3:
  cooldown: 3000
  all: 
  - "console: say He's name is %player_name%"
  - "command: say My name is %player_name%"
```

* ExampleItem 即物品ID，对应ID的物品交互后将触发下列指令组
  * consume 代表物品使用后将消耗
    * cooldown 物品消耗冷却时间
    * amount 每次消耗几个物品（大于这个数量才可以消耗并触发动作）
    * left 左键点击物品是否消耗
    * right 右键点击物品是否消耗
  * left 左键行为将触发下方指令组
    * 物品动作
  * right 右键行为将触发下方指令组
  * all 左/右键行为都将触发下方指令组
* ExampleItem3 物品ID
  * cooldown 代表物品使用冷却（不消耗）

{% hint style="info" %}
如果同时配置消耗冷却（consume.cooldown）和使用冷却（cooldown）

后者将被前者覆盖
{% endhint %}
