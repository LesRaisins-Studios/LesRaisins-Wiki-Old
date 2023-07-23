# 皮肤制作指南
## 开始之前

## 制作一个枪械皮肤

## 描述文件格式
要让模组读取资源包里的枪械皮肤，需要在资源包里添加一个json文件以描述皮肤  
具体的路径为
`assets/tac/models/gunskin/skin.json`  
请注意，描述文件的路径是固定的，你可以把皮肤所需的模型和纹理放置到其他命名空间里，但是描述文件的位置不能更改。对于加载多个资源包的场合，后加载的资源包里同一把枪械的使用相同标识符的皮肤会覆盖先加载的。

当前版本的描述文件格式如下:
```json
{
  "<枪械标识符>": {
    "<皮肤标识符>": {
      "<部件名>": "<模型路径>",
      "<部件名>": "<模型路径>",
      ...
    },
    "<皮肤标识符>": {
      ...
    },
    ...
  },
  "<枪械标识符>": {
    ...
  },
  ...
}
```

其中，`标识符`相当于枪和皮肤的名字，对于`同一把枪`，任意两个皮肤的`标识符`不应该相同  
`部件名`是每一把枪械对于的一系列模型部件的代号  
具体每一把枪的`标识符`和`部件名`可以在下方的[枪械模型部件说明](#枪械模型部件说明)中找到  
如果你的皮肤只有其中一部分的部件模型，那么只需要添加你需要替换的键值对即可，未作说明的其余部件将会自动使用枪械的默认皮肤

以下是一个示例
```json
{
  "ak47": {
    "golden": {
      "main": "tac:gunskin/ak47/ak47_golden",
      "mount": "tac:gunskin/ak47/ak47_golden_mount"
    },
    "silver": {
      "main": "tac:gunskin/ak47/ak47_silver"
    },
    "asiimov": {
      "main": "tac:gunskin/ak47/ak47_asiimov"
    },
    "vulcan": {
      "main": "tac:gunskin/ak47/ak47_vulcan"
    }
  },
  "qbz95": {
    "anubis": {
      "main": "tac:gunskin/qbz95/qbz95_anubis",
      "blot": "tac:gunskin/qbz95/qbz95_anubis_blot",
      "brake": "tac:gunskin/qbz95/qbz95_anubis_brake",
      "compensator": "tac:gunskin/qbz95/qbz95_anubis_compensator",
      "default_muzzle": "tac:gunskin/qbz95/qbz95_anubis_default_muzzle",
      "drum_mag": "tac:gunskin/qbz95/qbz95_anubis_drum_mag",
      "silencer": "tac:gunskin/qbz95/qbz95_anubis_silencer",
      "standard_mag": "tac:gunskin/qbz95/qbz95_anubis_standard_mag"
    }
  }
}
```

## 枪械模型部件说明
### ak47
枪械标识符: `ak47`
|部件名|说明|
|---|---|
|main|主要枪体|
|mount|附件(安装瞄具)
|bolt||
|light_stock||
|tactical_stock||
|heavy_stock||
|brake||
|compensator||
|silencer||
|standard_mag||
|extended_mag||