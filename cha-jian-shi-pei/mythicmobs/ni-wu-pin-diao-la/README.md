---
description: 相关配置支持解析即时声明变量
---

# NI物品掉落

在MM怪物的配置中添加

```
NeigeItems:
  Drops:
  - 物品ID 随机最低数量-随机最高数量 掉落概率 是否重复随机 指向数据 
```

物品ID可以是NI物品ID或者MM物品ID，优先检测NI物品

随机最低数量-随机最高数量 可以直接写数量

掉落概率 不写的话默认为1

是否重复随机 默认重复随机

指向数据 想写的话正常写就行

下面我写几个MM怪物示例配置

```
test1:
  Type: ZOMBIE
  Health: 1
  NeigeItems:
    Drops:
    # 50%掉落1-5个ID为"itemId"的NI物品(或MM物品)
    - itemId 1-5 0.5
test2:
  Type: ZOMBIE
  Health: 1
  NeigeItems:
    Drops:
    # 50%掉落1个ID为"itemId"的NI物品(或MM物品)
    - itemId 1 0.5
test3:
  Type: ZOMBIE
  Health: 1
  NeigeItems:
    Drops:
    # 掉落5个ID为"itemId"的NI物品(或MM物品)
    - itemId 5
```

顺带一提，因为整体支持调用即时声明节点，你可以通过节点自定义你的掉落概率（可根据权限、变量、等级、生命等一系列因素决定掉落概率）。下面我写一个最简单的例子

```
test4:
  Type: ZOMBIE
  Health: 1
  NeigeItems:
    Drops:
    # 掉落玩家等级数量的ID为"itemId"的NI物品(或MM物品)
    - itemId <papi::player_level>
```
