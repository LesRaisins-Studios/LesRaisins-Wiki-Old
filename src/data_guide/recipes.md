# 合成表
## 一、合成表路径
**合成表存放于\data\lesraisinsadd\recipes或\data\tac\recipes路径下**
## 二、修改合成表
以黑桃A为例

**本文不介绍原版合成表的相关教学，如有需求请[点击查看](https://minecraft.fandom.com/zh/wiki/%E9%85%8D%E6%96%B9 "点击查看")**

**[点击查看所有forge tags](https://forge.gemwire.uk/wiki/Tags "点击查看所有forge tags")**

武器在合成台的分类由data中的"weaponType"决定，武器类型：0步枪, 1 机枪, 2手枪, 3 霰弹枪, 4冲锋枪, 5 狙击枪, 6RPG
```
{
//type tac:workbench为使用枪械制造台合成，如需使用原版工作台则为minecraft:crafting_shaped。
  "type": "tac:workbench",
  //材料
  "materials": [
    {
      "item": {
	  //tag表示某一类物品，。
        "tag": "forge:ingots/iron"
      },
	  //所需数量
      "count": 26
    },
    {
      "item": {
        "tag": "forge:gems/quartz"
      },
      "count": 28
    },
    {
	//如使用的物品并非某一类物品，则使用"item"
      "item": {
        "item": "minecraft:obsidian"
      },
      "count": 12
    },
    {
      "item": {
        "item": "minecraft:diamond"
      },
      "count": 7
    },
    {
      "item": {
        "tag": "forge:rods/blaze"
      },
      "count": 6
    },
    {
      "item": {
        "item": "minecraft:nether_star"
      },
      "count": 1
    }
  ],
  //合成结果
  "result": {
    "item": "lesraisinsadd:ace_of_spades"
  }
}
```

---

## Recipes
## I. Recipes path
**Synthesis tables are stored in the \data\lesraisinsadd\recipes or \data\tac\recipes paths.
## II. Modifying the recipes
Take the Ace of Spades as an example

**This article does not introduce the vanilla recipes, [click to view](https://minecraft.fandom.com/zh/wiki/%E9%85%8D%E6%96%B9 "click to view") if you need**

**[Click to view all forge tags](https://forge.gemwire.uk/wiki/Tags "Click to view all forge tags")**

The classification of the weapon in the workbench is determined by the "weaponType" in the data, weapon type: 0 Rifle, 1 Machine gun, 2 Pistol, 3 Shotgun, 4 Submachine gun, 5 Sniper gun, 6 RPG.
```
{
//type "tac:workbench" for synthesising using the gunsmithing bench, or "minecraft:crafting_shaped" if you need to use the Crafting Table.
  "type": "tac:workbench".
  "materials": [
    {
      "item": {
	  //tag indicates a certain type of item.
        "tag": "forge:ingots/iron"
      },
	  //所需数量
      "count": 26
    },
    {
      "item": {
        "tag": "forge:gems/quartz"
      },
      "count": 28
    },
    {
	//If the item being used is not an item of a certain type, use "item"
      "item": {
        "item": "minecraft:obsidian"
      },
      "count": 12
    },
    {
      "item": {
        "item": "minecraft:diamond"
      },
      "count": 7
    },
    {
      "item": {
        "tag": "forge:rods/blaze"
      },
      "count": 6
    },
    {
      "item": {
        "item": "minecraft:nether_star"
      },
      "count": 1
    }
  ]
  //Synthesis result
  "result": {
    "item": "lesraisinsadd:ace_of_spades"
  }
}
``