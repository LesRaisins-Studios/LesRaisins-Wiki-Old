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


