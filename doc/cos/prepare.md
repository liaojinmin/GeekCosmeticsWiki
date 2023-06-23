---
sidebar_position: 1
---

# 准备

正式开始创建 新时装 前，你需要先了解的一些信息
你必须对 **YAML** 格式 有一点的了解
如果你不熟悉此配置结构的一些用法，建议参阅 [此处](https://www.runoob.com/w3cnote/yaml-intro.html) 
> 以下是一个时装配置案例
```yaml
cosmetics:
  # 这个时装的唯一识别ID
  '背包':
    # 这个时装的种类
    type: PACK
    # 这个时装的物品源
    itemStack:
      # 这个时装使用自有物品配置
      itemSource: Self
      # 这个时装的物品材质
      material: KELP
      # 这个时装的名称，理论上只在GUI中可见
      name: '&b背包'
      # 这个时装的lore，在gui中可见
      lore:
        - ''
      # 物品的 modelData
      customModelData: 20000
```
