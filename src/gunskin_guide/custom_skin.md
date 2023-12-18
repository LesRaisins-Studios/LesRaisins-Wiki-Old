# 自定义皮肤
当皮肤类型为`custom`时，代表该皮肤将尝试加载用户提供的自定义模型，此时会尝试使用`custom`内的模型列表覆盖模型的`模型部件`

如果一个皮肤没有指定某个`模型部件`，那么他会使用枪械对应的默认`模型部件`

对于某把武器具体的`模型部件`，可以参阅[章节：模型部件列表](./gunskin_guide/model.md)，或是参照TaC的默认模型（全部位于`assets/tac/models/special`下，请确保TaC版本 >=0.3.9，不然你会看到地狱一般的命名X_X）  
模型文件名中去掉枪械`注册名`的部分即为该模型文件对应的部件名

## 覆盖模型列表
如果你希望你的皮肤覆盖默认皮肤的某个模型，那么你只需要在`models`内添加对应的键值对即可`"<部件名>":"<部件模型路径>"`

特别的，我们提供了一种快速导入的方式，如果`models`内提供了`auto`键，那么会自动尝试按照默认的模型文件命名格式加载所有存在的模型`<主模型路径>_<部件名>`  
大多数情况下，使用这种方式就完全够用了  

一个完整的例子看起来像这样：
```json
{
  "ak47": {
    "silver": {
      "type": "custom",
      "models": {
        "auto": "tac:gunskin/ak47/ak47_silver"
      },
      "icon": "tac:textures/gunskin/icon/ak47_silver.png",
      "mini_icon": "tac:textures/gunskin/mini_icon/ak47_silver.png"
    }
  }
}
```

### Tips：
1. `<主模型路径>`是枪械/皮肤主要模型的位置(即`body`部件，不含部件名后缀)
比如上例中，该皮肤的主模型路径是`tac:gunskin/ak47/ak47_silver`(对应的文件是`assets/tac/models/special/ak47_silver.json`)，那么他的`blot`这一部件如果放到和主模型相同的目录里，并命名为`ak47_silver_blot.json`，那么这个模型也会一起自动加载并覆盖`blot`


# Custom skins
When the skin type is `custom`, it means that the skin will try to load a user-supplied custom model, and will try to override the model's `model parts` with the list of models in `custom`.

If a skin does not specify a `model part`, then it will use the default `model part` for the weapon.

For a weapon-specific `model part`, see [section: Model part lists](. /gunskin_guide/model.md), or refer to TaC's default models (all located under `assets/tac/models/special`, make sure that TaC version >= 0.3.9, otherwise you'll see the hellishly named X_X)  
The part of the model file name that removes the `registered name` of the gun is the corresponding part name of that model file

## Override the model list
If you want your skin to override one of the default skin's models, then you just need to add the corresponding key-value pairs inside `models` `"<part name>":"<part model path>"`

Specifically, we provide a quick import method that automatically tries to load all existing models in the default model file naming format `<main model path>_<part name>` if the `auto` key is provided in `models`.  
In most cases, using this approach will be perfectly adequate  

A complete example looks like this:
```json
{
  "ak47": {
    "silver": {
      "type": "custom",
      "models": {
        "auto": "tac:gunskin/ak47/ak47_silver"
      },
      "icon": "tac:textures/gunskin/icon/ak47_silver.png",
      "mini_icon": "tac:textures/gunskin/mini_icon/ak47_silver.png"
    }
  }
}
```

### Tips：
1. The `<main model path>` is the location of the main model of the gun/skin (i.e. the `body` part, without the part name suffix)
For example, in the above example, the skin's main model path is `tac:gunskin/ak47/ak47_silver` (the corresponding file is `assets/tac/models/special/ak47_silver.json`), so if his `blot` widget is put in the same directory as the main model and named `ak47_silver_blot.json`, then this model will be automatically loaded and overwrite the `blot` as well.


