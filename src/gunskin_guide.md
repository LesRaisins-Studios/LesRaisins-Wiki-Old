<style>
  table:{
    margin-left: 0.1%
  }
</style>
# 皮肤资源包制作指南

## 开始之前
欢迎来到LesRaisins提供的tac皮肤资源包制作指南

请注意：  
1. 本指南不是皮肤本身的纹理绘制或模型制作的美术教程，而仅仅是将已经制作好的皮肤纹理与模型实装进游戏的说明文档，同时，为了避免阅读障碍，也请确保在阅读本章节的内容掌握基础的资源包制作知识和相关概念； 
2. 待补充


## 制作一个枪械皮肤
未完成


## 一些说明
在游戏中tac最终呈现的枪械的`完整的模型`是由一系列来自不同文件的模型组合而来的；  
对于这一系列模型，我们在本指南中其称之为`模型部件`或者`部件`；


## 描述文件格式
要让模组读取资源包里的枪械皮肤，你需要在资源包里添加一个json文件以描述皮肤  
具体的路径为
`assets/<命名空间>/models/gunskin/skin.json`  
你可以这个文件放到任意一个命名空间的对应路径下，这会决定你接下来皮肤的命名空间。（其中，TaC 的`<命名空间>`为`tac`）

描述文件的具体内容应该看起来像这样：
```json
{
  "<枪械id>": {
    "<皮肤id>": {
      <皮肤内容>
    },
    "<皮肤id>": {
      ...
    },
    ...
  },
  "<枪械id>": {
    ...
  },
  ...
}
```

其中，`枪械id`对应枪械的注册名中去掉命名空间的部分(比如`ak47`)  
`皮肤id`是你为皮肤起的id，他会和描述文件的命名空间组成皮肤的`注册名`(比如描述文件放在了`example`命名空间下，`皮肤id`是`ruaaa`，那么这个皮肤的`注册名`就是`example:ruaaa`)  
对于同一把枪，两个不同皮肤的`注册名`不应该相同，如果出现了相同的情况，则后加载的会覆盖先加载的

`皮肤内容`是对于某个具体皮肤的描述，具体格式如下：
```json
    "<皮肤id>": {
      "type": "<texture/custom>",   //必须,为 texture/custom 二者之一,决定该皮肤是否需要修改模型
      "textures": {                 //当且仅当类型为 texture
        "<名称>": "<路径>"
      },
      "models": {                   //当且仅当类型为 custom
        "<部件名>": "<路径>"
      },
      "icon": "<路径>"              //可选,皮肤对应的武器图标,在右下角状态栏展示
    }
```
当皮肤类型为`texture`时,代表该皮肤不会修改默认模型而仅替换材质,此时会尝试使用`textures`内的材质列表覆盖枪械所有模型内的默认材质。

当皮肤类型为`custom`时,代表该皮肤将会加载自定义模型,此时会尝试使用`models`里的模型覆盖默认模型;
特别的,如果`models`内提供了`auto`键,那么会自动尝试按照默认的模型文件命名格式加载所有模型`<主模型路径>_<部件名>`

如果你想为某一把枪制作皮肤,那么它各个模型部件的具体命名可以参照官方模型的命名格式(全部位于`assets/tac/models/special`下)

比如`ak47`的主模型路径是`tac:special/ak47`(对应的文件是`assets/tac/models/special/ak47.json`),那么他的`blot`这一部件就应该放到和主模型一样的文件夹里,并命名为`ak47_blot.json`

如果你的皮肤只有其中一部分的部件模型,那么你也可以只添加你需要替换的键值对,其余的部分会使用默认皮肤的模型。

一个完整的例子看起来像这样：
```json
{
  "ak47": {
    "golden": {
      "type": "texture",
      "textures": {
        "0": "tac:gunskin/ak47/ak47_golden"
      },
      "icon": "tac:textures/gunskin/icon/ak47_golden.png"
    },
    "silver": {
      "type": "custom",
      "models": {
        "auto": "tac:gunskin/ak47/ak47_silver"
      },
      "icon": "tac:textures/gunskin/icon/ak47_silver.png"
    }
  },
  "其他的什么枪":{

  }
}
```

## 调用皮肤
贼简单,`/give @s tac:ak47{Skin:"<皮肤命名空间>:<皮肤标识符>"}`,可以不加命名空间,默认是`tac`,
比如有一把ak的皮肤,`skin.json`放在`tac`的命名空间里,比如上例中的黄金和白银ak,
就是`/give @s tac:ak47{Skin:"golden"}` `/give @s tac:ak47{Skin:"tac:silver"}`  


## 通用皮肤
在 TaC 0.3.9 的开发版本中，加入了注册好的「皮肤插件」，其中提供了 9 种（当前）通用皮肤。

对于新增在这 9 种皮肤下的内容，可以遵循在`skin.json`中已有的注册形式进行注册，成功加载后当即可以在游戏内通过「皮肤插件」调用。

以`ai_awp`的通用皮肤举例：
```json
{
  "ai_awp": {
    "ai_awp_beige": {
      "type": "texture",
      "textures": {
        "4": "tac:gunskin/ai_awp/ai_awp_beige"
      },
      "icon": "tac:textures/gunskin/icon/ai_awp_beige.png"
    },
    "ai_awp_black": {
      "type": "texture",
      "textures": {
        "4": "tac:gunskin/ai_awp/ai_awp_black"
      },
      "icon": "tac:textures/gunskin/icon/ai_awp_black.png"
    },
    "ai_awp_blue": {
      "type": "texture",
      "textures": {
        "4": "tac:gunskin/ai_awp/ai_awp_blue"
      },
      "icon": "tac:textures/gunskin/icon/ai_awp_blue.png"
    },
    "ai_awp_green": {
      "type": "texture",
      "textures": {
        "4": "tac:gunskin/ai_awp/ai_awp_green"
      },
      "icon": "tac:textures/gunskin/icon/ai_awp_green.png"
    },
    "ai_awp_jade": {
      "type": "texture",
      "textures": {
        "4": "tac:gunskin/ai_awp/ai_awp_jade"
      },
      "icon": "tac:textures/gunskin/icon/ai_awp_jade.png"
    },
    "ai_awp_orange": {
      "type": "texture",
      "textures": {
        "4": "tac:gunskin/ai_awp/ai_awp_orange"
      },
      "icon": "tac:textures/gunskin/icon/ai_awp_orange.png"
    },
    "ai_awp_pink": {
      "type": "texture",
      "textures": {
        "4": "tac:gunskin/ai_awp/ai_awp_pink"
      },
      "icon": "tac:textures/gunskin/icon/ai_awp_pink.png"
    },
    "ai_awp_sand": {
      "type": "texture",
      "textures": {
        "4": "tac:gunskin/ai_awp/ai_awp_sand"
      },
      "icon": "tac:textures/gunskin/icon/ai_awp_sand.png"
    },
    "ai_awp_white": {
      "type": "texture",
      "textures": {
        "4": "tac:gunskin/ai_awp/ai_awp_white"
      },
      "icon": "tac:textures/gunskin/icon/ai_awp_white.png"
    }
  }
}
```