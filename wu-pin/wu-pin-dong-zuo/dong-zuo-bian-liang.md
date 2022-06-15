# 动作变量

以默认配置为例

```
actionTest:
  material: STONE
  nbt:
    test1: "666"
    test2: 
      test3: "777"
    test4:
    - "888"
    - "999"
  sections:
    test: "000"
```

```
actionTest:
  all: 
  - "console: say 名为test1的NBT的值为: <nbt::test1>"
  - "console: say 名为test2.test3的NBT的值为: <nbt::test2.test3>"
  - "console: say 名为test4.0的NBT的值为: <nbt::test4.0>"
  - "console: say 名为test4.1的NBT的值为: <nbt::test4.1>"
  - "console: say 名为test的节点的值为: <data::test>"
```

后台返回值如下

```
[Server] 名为test1的NBT的值为: 666
[Server] 名为test2.test3的NBT的值为: 777
[Server] 名为test4.0的NBT的值为: 888
[Server] 名为test4.1的NBT的值为: 999
[Server] 名为test的节点的值为: 000
```

用法类似于即时声明节点，data表示调用节点，nbt表示调用物品nbt。

一层一层id以小数点"."分隔
