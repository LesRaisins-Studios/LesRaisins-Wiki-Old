# 皮肤描述文件

要让模组读取资源包里的枪械皮肤，你需要在资源包里添加一个json文件以描述皮肤  
具体的路径为
`assets/<命名空间>/models/gunskin/skin.json`  
你可以这个文件放到任意一个命名空间的对应路径下，这会决定你接下来皮肤的命名空间。（其中，TaC 的`<命名空间>`为`tac`）

## 描述文件格式
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

其中，`枪械id`对应枪械的注册名中去掉命名空间的部分（比如`ak47`）  
`皮肤id`是你为皮肤起的id，他会和描述文件的命名空间组成皮肤的`注册名`  
（比如描述文件放在了`example`命名空间下，`皮肤id`是`ruaaa`，那么这个皮肤的`注册名`就是`example:ruaaa`）  
对于同一把枪，两个不同皮肤的`注册名`不应该相同，如果出现了相同的情况，则后加载的会覆盖先加载的

`皮肤内容`是对于某个具体皮肤的描述，具体格式如下：
```json
    "<皮肤id>": {                    
      "type": "<texture/custom/common_texture>",   //必须,决定皮肤类型
      "textures": {                     //当且仅当类型为 texture/common_texture
        "<名称>": "<路径>"
      },
      "models": {                       //当且仅当类型为 custom
        "<部件名>": "<路径>"
      },
      "icon": "<路径>",                 //可选,皮肤对应的武器图标,在右下角状态栏展示
      "mini_icon": "<路径>"             //目前仅LesRaisinsGui使用到了,用于右上角的击杀播报展示
    }
```

关于每一种`皮肤类型`的详细说明，请参阅他们各自的页面  

> `common_texture` [章节：通用皮肤](./common_skin.md)  
> `texture` [章节：材质皮肤](./texture_skin.md)   
> `custom` [章节：自定义皮肤](./custom_skin.md)  

# Skin Description File(skin.json)

To allow the module to read the gun skins in the resource pack, you need to add a json file to the resource pack to describe the skins  
The specific path is
`assets/<namespace>/models/gunskin/skin.json`.  
You can put this file in any namespace, which will determine the namespace of your next skin. (where `<namespace>` for TaC is `tac`)

## Description file format
The exact contents of the description file should look something like this:
```json
{
  "<GUNid>": {
    "<SKINid>": {
      <Skin content>
    },
    "<SKINid>": {
      ...
    },
    ...
  },
  "<GUNid>": {
    ...
  },
  ...
}
```

The `gun id` corresponds to the part of the gun's registered name where the namespace is removed (e.g. `ak47`).  
The `skin id` is the id you give to the skin, and it will be combined with the namespace of the description file to form the `registered name` of the skin.  
(For example, if the description file is in the `example` namespace, and the `skin id` is `ruaaa`, then the `registered name` of the skin would be `example:ruaaa`)  
For the same gun, the `registered name` of two different skins should not be the same, if it is, the later loaded skin will overwrite the first loaded skin.

The `skin content` is the description of a specific skin, in the following format:
```json
    "<SKINid>": {                    
      "type": "<texture/custom/common_texture>",   //Must, determine skin type
      "textures": {                     //if and only if the type is texture/common_texture
        "<NAME>": "<Path>"
      },
      "models": {                       //If and only if the type is custom
        "<part name>": "<Path>"
      },
      "icon": "<Path>",                 //Optional, skinned weapon icons are displayed in the lower right status bar.
      "mini_icon": "<Path>"             //Currently only used by LesRaisinsGui for the kill announcement in the upper right corner.
    }
```

For a detailed description of each `skin type`, see their respective pages  

> `common_texture` [section: Common skins](. /common_skin.md)  
> `texture` [Section: Texture Skins](. /texture_skin.md)   
> `custom` [Section: Customizing Skins](. /custom_skin.md) 