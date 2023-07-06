---
sidebar_position: 3
---

# 物品源
| **节点**     | 是否物品源 | 描述                     |
|------------|-------|------------------------|
| **Self** | 是     | 插件本身提供的物品展示源           |
| **ModelEngine** | 否     | 来着 ModelEngine 插件提供的模型 |
| **ItemsAdder** | 是     | 来着 ItemsAdder 插件提供的物品  |
> 你可以理解为获取时装模型的源物品，也可能是其他插件提供的物品、模型

## 理解源
如果使用 `Self` 设置时装物品源
以下案例将构建一个 `KELP` 材质的物品并设置 customModelData
作为背包时装，如果你的 ModelData 错误，未能与材质包上的 ModelData 同步
则会导致玩家的背包展示出 **海藻** 而不是你的模型
```yaml title="Self"
cosmetics:
  背包:
    type: PACK
    itemStack:
      itemSource: Self
      material: KELP
      customModelData: 20000
```

```yaml title="ItemsAdder"
cosmetics:
  背包2:
    type: PACK
    itemStack:
      itemSource: ItemsAdder
      itemID: "我是ItemsAdder的物品名称"
      name: "我是用于在GUI中覆盖原有物品名称"
```

> 如果要关闭气球的摇摆动画
> ```yaml title="如果要关闭气球的摇摆动画”
> cosmetics:
> 海马气球:
> type: BALLOON
> itemStack:
> itemSource: Self
> material: KELP
> name: '&b海马气球'
> lore:
> - ''
> customModelData: 20001
> # 关闭摇摆动画
> closeBalloonAction: true
> ```

:::warning 关于 ModelEngine 源
目前插件版本兼容仍然存在问题。
:::


 
