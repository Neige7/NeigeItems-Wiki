# 物品配置

## 路径

物品配置文件可以存放于plugins/NeigeItems/Items文件夹

重复 ID 的物品仍然会被加载，但可能互相覆盖

最后哪个物品活下来。。。随缘了属于是

## 配置

详见默认配置

{% content-ref url="../kai-shi/mo-ren-pei-zhi.md" %}
[mo-ren-pei-zhi.md](../kai-shi/mo-ren-pei-zhi.md)
{% endcontent-ref %}

## 结构

* 物品ID
  * 物品材质
  * CustomModelData
  * 子ID/损伤值
  * 物品名
  * 物品Lore（物品描述）\
    \- 第一行Lore\
    \- 第二行Lore
  * 附魔
    * 附魔ID: 附魔等级
  * 隐藏标识\
    \- 隐藏标识1\
    \- 隐藏标识2
  * 颜色（0-65535）
  * 物品NBT
    * NBT键: NBT值
  * 引用的全局节点\
    \- 全局节点1\
    \- 全局节点2
  * 私有节点
    * 私有节点ID
      * 私有节点类型
      * 私有节点配置
      * 私有节点配置
      * 私有节点配置
