# 物品消耗

## 配置

以默认物品配置为例

```
  options:
    consume:
      cooldown: 3000
      amount: 1
      left: true
      right: true
```

* cooldown 物品消耗的冷却时间，单位为ms\
  &#x20;                物品使用冷却不会持久化存储，关服即重置
* amount 每次消耗的物品数量，物品只有大于该数量才会被消耗
* left 左键行为是否会使物品被消耗
* right 右键行为是否会使物品被消耗
