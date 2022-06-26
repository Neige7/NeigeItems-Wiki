# NI物品掉落

在MM怪物的配置中添加

```
NeigeItems:
  Drops:
  - 物品ID 随机最低数量-随机最高数量 掉落概率 是否重复随机 指向数据 
```

随机最低数量-随机最高数量 可以直接写数量

掉落概率 不写的话默认为1

是否重复随机 默认重复随机

指向数据 想写的话正常写就行

下面我写几个示例配置

```
test1:
  Type: ZOMBIE
  Health: 1
  NeigeItems:
    Drops:
    # 50%掉落1-5个ID为"itemId"的NI物品
    - itemId 1-5 0.5
test2:
  Type: ZOMBIE
  Health: 1
  NeigeItems:
    Drops:
    # 50%掉落1个ID为"itemId"的NI物品
    - itemId 1 0.5
test3:
  Type: ZOMBIE
  Health: 1
  NeigeItems:
    Drops:
    # 掉落5个ID为"itemId"的NI物品
    - itemId 5
```
