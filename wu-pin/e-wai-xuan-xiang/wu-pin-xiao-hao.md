---
description: 物品消耗的同时会触发物品指令
---

# 物品消耗

## 配置

以默认物品配置为例

```
ExampleItem2:
  material: STONE
  options:
    consume:
      cooldown: 3000
      amount: 10
      left: true
      right: true
```

* consume 物品消耗相关配置
  * cooldown 物品消耗的冷却时间，单位为ms\
    &#x20;                物品使用冷却不会持久化存储，关服即重置
  * amount 每次消耗的物品数量，物品只有大于该数量才会被消耗，默认为1
  * left 左键行为是否会使物品被消耗
  * right 右键行为是否会使物品被消耗

{% hint style="info" %}
options.cosume.cooldown优先级高于options.cooldown

如果你同时配置了两者

则仅有options.cosume.cooldown可以正常工作
{% endhint %}
