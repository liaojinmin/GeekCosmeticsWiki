---
sidebar_position: 1
---

# API应用

## 事件
```
package me.geek.cos.api.event
// 玩家进入区域事件
me.geek.cos.api.event.PlayerJoinRegionsEvent
// 玩家离开区域事件
me.geek.cos.api.event.PlayerLeaveRegionsEvent

```

## 给予与扣除
> 以下是一个简单的给予玩家、删除玩家时装的案例

```kotlin
import me.geek.cos.api.*
import org.bukkit.entity.Player

fun Player.add(node: String) {
    val cos = CosmeticManager.givePlayerCosmetic(this, node)
    sendMessage("时装给与结果: $cos.reason")
}
fun Player.del(node: String) {
    val cos = CosmeticManager.takePlayerCosmetic(this, node)
    sendMessage("时装扣除结果: $cos.reason")
}
```

## 自定义时装
:::warning  
暂未开放API，开放后允许扩展更多类型时装，定义载体的动作轨迹。
:::