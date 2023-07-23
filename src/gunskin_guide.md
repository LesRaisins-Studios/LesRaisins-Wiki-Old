# 皮肤制作指南

## 开始之前
欢迎来到TaC-LesRaisins
本项目使用了一个非常简单粗暴的方式使tac可以通过加载资源包里的皮肤  

请注意：  
1. 本指南不是资源包制作或者皮肤本身的绘制教程，而仅仅是将已经制作好的皮肤纹理与贴图实装进游戏的说明文档，请确保你在阅读本章节的内容掌握基础的资源包制作知识和相关概念;  
2. 本项目仅仅是个人为了好玩而进行的，且基本没有被TaC主分支合并的可能，一切修改与产生的问题TaC制作组无关(也不要因为皮肤相关的事情去催他们，他们有自己的开发计划);
3. 介于个人能力有限，你应当知晓使用本分支可能造成的风险，比如某天不再维护，或者出现奇妙的bug(我很可能也没有能力修);
4. 由于本项目最初是为服务器服务的，更换皮肤需要修改枪械本身的nbt，目前还没有不开启作弊切换皮肤的途径。

## 制作一个枪械皮肤
未完成
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

其中，`标识符`相当于枪和皮肤的名字，对于同一把枪，任意两个皮肤的`标识符`不应该相同  
`部件名`是每一把枪械对于的一系列模型部件的代号。  

具体每一把枪的`标识符`和`部件名`可以在[章节：模型部件列表](#模型部件说明)中找到。

如果你的皮肤只有其中一部分的部件模型，那么只需要添加你需要替换的键值对即可，未作说明的其余部件将会自动使用枪械的默认皮肤。

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
