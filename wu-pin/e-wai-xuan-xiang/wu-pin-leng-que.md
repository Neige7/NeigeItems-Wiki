# 物品冷却

## 配置

以默认物品配置为例

```
ExampleItem3:
  material: STONE
  options:
    cooldown: 3000
```

* cooldown 物品使用的冷却时间，单位为ms\
  &#x20;                物品使用冷却不会持久化存储，关服即重置

{% hint style="info" %}
options.cosume.cooldown优先级高于options.cooldown

如果你同时配置了两者

则仅有options.cosume.cooldown可以正常工作
{% endhint %}
