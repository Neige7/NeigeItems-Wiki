---
description: 全部动作支持papi变量
---

# 动作类型

## 发送文本

> 向玩家发送一条消息(可使用&作为颜色符号)

```yaml
- 'tell: &eHello'
```

## 发送文本

> 向玩家发送一条消息(不将&解析为颜色符号)

```yaml
- 'tellNoColor: §eHello, can you see "&"?'
```

## 强制聊天

> 强制玩家发送一条消息(不将&解析为颜色符号)

```yaml
- 'chat: see, I can send "&"!'
```

## 强制聊天

> 强制玩家发送一条消息(可使用&作为颜色符号)

```yaml
- 'chatWithColor: &eHello'
```

## 执行指令(玩家)

> 强制玩家执行一条指令(可使用&作为颜色符号)

```yaml
- 'command: say Hello'
- 'player: say Hello'
```

## 执行指令(玩家)

> 强制玩家执行一条指令(不将&解析为颜色符号)

```yaml
- 'commandNoColor: say Hello'
```

## 执行指令(后台)

> 后台执行一条指令(可使用&作为颜色符号)

```yaml
- 'console: say Hello'
```

## 执行指令(后台)

> 后台执行一条指令(不将&解析为颜色符号)

```yaml
- 'consoleNoColor: say Hello'
```

## 给予金币(Vault)

> 给予玩家一定数量金币

```yaml
- 'giveMoney: 100'
```

## 扣除金币(Vault)

> 扣除玩家一定数量金币

```yaml
- 'takeMoney: 100'
```

## 给予经验

> 给予玩家一定数量经验

```yaml
- 'giveExp: 100'
```

## 扣除经验

> 扣除玩家一定数量经验

```yaml
- 'takeExp: 100'
```

## 设置经验

> 设置玩家当前经验

```yaml
- 'setExp: 100'
```

## 给予经验等级

> 给予玩家一定数量经验等级

```yaml
- 'giveLevel: 100'
```

## 扣除经验等级

> 扣除玩家一定数量经验等级

```yaml
- 'takeLevel: 100'
```

## 设置经验等级

> 设置玩家当前经验等级

```yaml
- 'setLevel: 100'
```

## 延时

> 延迟动作执行(单位是tick)

```yaml
- 'delay: 10'
```

## 终止

> 终止动作执行

```yaml
- 'return'
```
