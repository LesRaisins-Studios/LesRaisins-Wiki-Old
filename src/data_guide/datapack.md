# 数据包制作
数据包可以在游戏中使用/reload指令快速重载，为便于使用及测试推荐各位玩家使用数据包管理数据。
## 一、准备工作
### 1. 创建数据包：
在文件夹"saves/存档名/datapack"(单机)或"world/datapack"(服务器)下创建一个文件夹，文件夹名称随意。
在该文件夹下创建**文件夹data**和**文件pack.mcmeta**
并将一下代码复制进pack.mcmeta内
```
{
    "pack": {
        "pack_format": 6,
        "description": "介绍"
    }
}
```
进入data文件夹创建以下路径：**"data/lesraisinsadd/guns"**或**"data/tac/guns"**

### 2.加载数据包：
单机游戏使用/reload指令重载数据包
服务器推荐重启重载

---
# Datapack Creation
Datapack can be quickly reloaded in the game using the **/reload** command, for ease of use and testing it is recommended that you use datapack to manage your data.
## I. Preparation
### 1. Create the datapack:
Create a folder under "saves/NAME/datapack" **(single world)** or "world/datapack" **(server)**.
In this folder, create the folder **data** and the file **pack.mcmeta**.
And copy the following code into **pack.mcmeta**
```
{
    "pack": {
        "pack_format": 6,
        "description": "Introduction"
    }
}
```
Go to the data folder and create the following path: **"data/lesraisinsadd/guns "** or **"data/tac/guns "**

### 2. Load the packet:
Standalone games use the /reload command to reload packets
Server recommended reboot reload