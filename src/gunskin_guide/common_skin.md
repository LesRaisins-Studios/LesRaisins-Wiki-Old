<style>
  table:{
    margin-left: 0.1%
  }
</style>
# 通用皮肤
在 TaC 0.3.9 的开发版本中，加入了注册好的「皮肤插件」，其中提供了 16 种（当前）通用皮肤。

对于新增在这 16 种皮肤下的内容，可以遵循在`skin.json`中已有的注册形式进行注册，成功加载后当即可以在游戏内通过「皮肤插件」调用。

为了避免大量重复劳动，我们提供了一种批量加载染色皮肤的方式，即`common_texture`类型  
通过这种方式，我们可以批量加载符合命名格式的染色皮肤。

注意，对于皮肤文件名称，请按照已有的皮肤进行设置（当前可以参考`tec_9`），否则会出现无法读取皮肤的情况。  
如果你是为了自己制作皮肤，请勿使用这种方式    
## 默认列表
以下是16种通用皮肤具体的皮肤id，以及其对应的皮肤插件的中文译名  
### todo： 完善中文译名
|皮肤id     |中文译名|皮肤id    |中文译名|  
|-----------|-------|----------|--------|  
|black      |1      |blue      |1       |  
|brown      |1      |dark_blue |1       |  
|dark_green |1      |gray      |1       |  
|green      |1      |jade      |1       |  
|light_gray |1      |magenta   |1       |  
|orange     |1      |pink      |1       |  
|purple     |1      |red       |1       |  
|sand       |1      |white     |1       |  

这里的命名空间全部是`tac`，你可以用对应的皮肤注册名通过`texture`或是`custom`类型单独覆盖某个皮肤
## 描述文件格式
通用皮肤的`皮肤内容`部分应该看起来像这样：
```json
  "<id>": {
    "common": {
      "type": "common_texture",
      "textures": {
        "<覆盖目标>": "<主要路径>"
      },
      "icon": "<主要路径>"
    }
```
此时，`textures`和`icon`等提供的是材质文件的`<主要路径>`  
也就是说，加载器会遍历上述默认列表中所有皮肤id，并把它拼接到主要路径之后尝试加载材质`<主要路径>_<皮肤id>`  

以awp为例，比如你提供了`tac:gunskin/ai_awp/ai_awp`
那么加载器就会尝试寻找所有名为`assets/tac/textures/gunskin/ai_awp/ai_awp_<皮肤id>.png`的材质文件并加载为对应`皮肤id`的皮肤  
如果材质列表含有多个项目，请确保每一项都填写正确并具有正确的文件名

以下是当前版本的描述文件，供参考：
```json
{
  "ai_awp": {
    "common": {
      "type": "common_texture",
      "textures": {
        "4": "tac:gunskin/ai_awp/ai_awp"
      },
      "icon": "tac:gunskin/icon/ai_awp"
    }
  },

  "deagle_357": {
    "common": {
      "type": "common_texture",
      "textures": {
        "5": "tac:gunskin/deagle_357/deagle_357",
        "6": "tac:gunskin/deagle_357/attachments"
      },
      "icon": "tac:gunskin/icon/deagle_357"
    }
  },

  "scar_l": {
    "common": {
      "type": "common_texture",
      "textures": {
        "5": "tac:gunskin/scar_l/scar_l"
      },
      "icon": "tac:gunskin/icon/scar_l"
    }
  },

  "udp_9": {
    "common": {
      "type": "common_texture",
      "textures": {
        "4": "tac:gunskin/udp_9/udp_9"
      },
      "icon": "tac:gunskin/icon/udp_9"
    }
  },

  "tec_9": {
    "common": {
      "type": "common_texture",
      "textures": {
        "4": "tac:gunskin/tec_9/tec_9"
      },
      "icon": "tac:gunskin/icon/tec_9"
    }
  }
}
```

# Common Skin
In the development version of TaC 0.3.9, a registered "Skin Plugin" has been added, which provides 16 (current) generic skins.

For the content added under these 16 skins, you can follow the registration form in `skin.json`, and after successful loading, you can immediately call it in-game through the `skin plugin`.

In order to avoid a lot of duplication of efforts, we provide a way to load coloring skins in bulk, namely the `common_texture` type.  
In this way, we can batch load color skins that match the naming format.

Note that for the skin file name, please set it according to the existing skin (currently you can refer to `tec_9`), otherwise you will not be able to read the skin.  
Do not use this method if you are making skins for yourself    
## Default list
Here are the specific skin ids for the 16 generic skins, and the English translations of their corresponding skin plugins  
### todo: Refine the English translations.
|skin id    |english|skin id   |english| 
|-----------|-------|----------|--------|  
|black      |1      |blue      |1       |  
|brown      |1      |dark_blue |1       |  
|dark_green |1      |gray      |1       |  
|green      |1      |jade      |1       |  
|light_gray |1      |magenta   |1       |  
|orange     |1      |pink      |1       |  
|purple     |1      |red       |1       |  
|sand       |1      |white     |1       |  

The namespaces here are all `tac`, and you can override a skin individually with the corresponding skin registry name by using the `texture` or `custom` type.
## Describe the file（skin.json） format
The `Skin Content` section of a generic skin should look something like this:
```json
  "<id>": {
    "common": {
      "type": "common_texture",
      "textures": {
        "<coverage target>": "<Main paths>"
      },
      "icon": "<Main paths>"
    }
```
In this case, `textures` and `icon` etc. provide the `<primary path>` of the material file.  
That is, the loader iterates through all the skin ids in the default list above and tries to load the material `<primary path>_<skin id>` after stitching it into the primary path

Using awp as an example, say you provide `tac:gunskin/ai_awp/ai_awp`
then the loader will try to find all material files named `assets/tac/textures/gunskin/ai_awp/ai_awp_<skin id>.png` and load them as the skin corresponding to the `skin id`.  
If the material list contains multiple items, make sure each item is filled out correctly and has the correct filename!

For reference, here is the description file for the current version:
```json
{
  "ai_awp": {
    "common": {
      "type": "common_texture",
      "textures": {
        "4": "tac:gunskin/ai_awp/ai_awp"
      },
      "icon": "tac:gunskin/icon/ai_awp"
    }
  },

  "deagle_357": {
    "common": {
      "type": "common_texture",
      "textures": {
        "5": "tac:gunskin/deagle_357/deagle_357",
        "6": "tac:gunskin/deagle_357/attachments"
      },
      "icon": "tac:gunskin/icon/deagle_357"
    }
  },

  "scar_l": {
    "common": {
      "type": "common_texture",
      "textures": {
        "5": "tac:gunskin/scar_l/scar_l"
      },
      "icon": "tac:gunskin/icon/scar_l"
    }
  },

  "udp_9": {
    "common": {
      "type": "common_texture",
      "textures": {
        "4": "tac:gunskin/udp_9/udp_9"
      },
      "icon": "tac:gunskin/icon/udp_9"
    }
  },

  "tec_9": {
    "common": {
      "type": "common_texture",
      "textures": {
        "4": "tac:gunskin/tec_9/tec_9"
      },
      "icon": "tac:gunskin/icon/tec_9"
    }
  }
}
```