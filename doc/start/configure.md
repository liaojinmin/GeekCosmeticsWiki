---
sidebar_position: 3
---
# 配置

若插件成功安装，你将会在服务端插件目录下看到一个名为 GeekCosmetics 的目录，其结构如下

```
GeekCosmetics
│  settings.yml ················ 插件配置文件
│  menu.yml ············ 菜单配置文件
│  kether.yml ················ Kether 配置文件
│  
├─data.db ······················· 插件本地数据
│      
├─lang ······················· 语言文件
│      zh_CN.yml
│
├─cos ······················· 时装文件
│      def.yml
│      
└─regions ·················· 区域文件
       def.yml
```

### 配置文件
```yaml title=settings.yml
debug: false
#
# 数据库设置，选择你需要使用的数据储存方式，sqlite,mysql
# 默认: sqlite
data_storage:
  use_type: sqlite
  mysql:
    host: '127.0.0.1'
    port: 3306
    database: 'server_cos'
    username: 'root'
    password: '123456'
    params: '?autoReconnect=true&useSSL=false'
  hikari_settings:
    maximum_pool_size: 10
    minimum_idle: 10
    maximum_lifetime: 1800000
    keepalive_time: 0
    connection_timeout: 5000
Redis: # 该功能未实在
  use: false
  host: 127.0.0.1
  port: 6379
  password: ''
  ssl: false
set:
  # 显示视距
  visibleByDistance: 32
  # 玩家进入NPC展示区时，NPC是否解析玩家身上的装备，设置为 FALSE 以节省带宽使用
  parsePlayerArmor: true
```