# 自定义皮肤
当皮肤类型为`custom`时，代表该皮肤将尝试加载用户提供的自定义模型，此时会尝试使用`custom`内的模型列表覆盖模型的`模型部件`

如果一个皮肤没有指定某个`模型部件`，那么他会使用枪械对应的默认`模型部件`

对于某把武器具体的`模型部件`，可以参阅[章节：模型部件列表](./gunskin_guide/model.md)，或是参照TaC的默认模型（全部位于`assets/tac/models/special`下）  
模型文件名中去掉枪械`注册名`的部分即为该模型文件对应的部件名

## 覆盖模型列表
未完成的页面

*如果`models`内提供了`auto`键,那么会自动尝试按照默认的模型文件命名格式加载所有模型`<主模型路径>_<部件名>`

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
