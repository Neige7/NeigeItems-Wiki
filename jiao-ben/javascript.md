# JavaScript

## 路径

所有脚本文件应存放于plugins/NeigeItems/Scripts文件夹

## 运行前提

脚本文件被正常识别的前提条件是：它返回了该文件的全局对象

以默认脚本文件为例

```
/**
 * @param sections json {节点键: 节点值}
 * @param player Player 待解析玩家
 */
function main(sections, player) {
    return sections["strings-1"]
}

load = () => {return this}
load()

```

每个待调用的NeigeItems脚本文件，都应该在最后返回该文件的全局对象，这样才能被正常调用。

在该文件中的体现便是最后的两行：

```
load = () => {return this}
load()
```

如果你无法理解我在说什么，请在你为NeigeItems编写的每个脚本文件最后加上这两行代码

## 函数参数

每个函数在被调用时都会被传入两个对象

* Sections 即当前物品的所有指向数据
* player 即作为该物品解析对象的玩家

以默认脚本文件为例

```
/**
 * @param sections json {节点键: 节点值}
 * @param player Player 待解析玩家
 */
function main(sections, player) {
    return sections["strings-1"]
}

load = () => {return this}
load()

```

你需要手动在参数位置写上这两个参数

或者通过arguments\[0]及arguments\[1]调用它们

