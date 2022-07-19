# 自定义动作

自定义动作需要一定的 javascript 和 java 基础。

自定义动作文件存放于 NeigeItems/CustomSections 文件夹

下面是示例配置

```
// 文件名不重要, 写成啥都行
// main函数会自动执行
function main() {
    // 导入相应的类, 这两行看不懂的话直接抄就行
    const ActionManager = Packages.pers.neige.neigeitems.manager.ActionManager.INSTANCE

    // 插入新的自定义动作
    ActionManager.addAction(
        // 动作名称
        "test",
        // 动作内容(一般是异步调用的, 所以需要同步执行的内容需要自行同步)
        function(player, string) {
            player.sendMessage("1233211234567")
            // 每个动作都一定要返回一个布尔量(true或false)
            return true
        })
}

```
