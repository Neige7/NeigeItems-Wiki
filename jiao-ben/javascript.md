# JavaScript

## 对象与函数

NeigeItems 的 JavaScript 节点目前提供以下对象

* `player` 即 玩家本身

提供以下函数

* `vars(String id)` 根据ID解析节点
* `papi(String text)` 解析papi变量
* `papi(String itemID, Player player)` 获取对应ID的NI物品

## 路径

所有脚本文件应存放于plugins/NeigeItems/Scripts文件夹

## 运行前提

脚本文件被正常识别的前提条件是：它返回了该文件的全局对象

以默认脚本文件为例

```
function main() {
    return vars("strings-1") + player.getName()
}

load = function() {return this}
load()

```

每个待调用的NeigeItems脚本文件，都应该在最后返回该文件的全局对象，这样才能被正常调用。

在该文件中的体现便是最后的两行：

```
load = function() {return this}
load()
```

如果你无法理解我在说什么，请在你为NeigeItems编写的每个脚本文件最后加上这两行代码

