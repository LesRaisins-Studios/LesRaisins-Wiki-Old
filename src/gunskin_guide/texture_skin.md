# 材质皮肤
当皮肤类型为`texture`时，代表该皮肤不会修改默认模型而仅替换材质，此时会尝试使用`textures`内的材质列表覆盖枪械所有模型内的默认材质。

其中，继承的父模型（TaC的默认模型）全部位于`assets/tac/models/special`下

## 覆盖材质列表
以`ak47`为例，这是它的主要模型`ak47.json`，
```json
{
	"credit": "Made with Blockbench",
	"texture_size": [256, 256],
	"textures": {
		"0": "tac:items/ak47_uv",
		"particle": "tac:items/ak47_uv"
	},
	"elements": [...]
    ...
}
```

其中，`textures`是父模型的材质列表  
如果我们想要皮肤覆盖其中的某些材质，则需要在皮肤的材质列表中指定相应的路径  
比如我们有一把黄金ak的材质，想要用一张名为`ak47_golden.png`的新贴图覆盖默认模型的`ak47_uv.png`  
那么我们只需要这样写：
```json
    "golden": {
      "type": "texture",
      "textures": {
        "0": "tac:gunskin/ak47/ak47_golden"
      },
      "icon": "tac:gunskin/icon/ak47_golden"
    }
```
该材质作也为例子包含在TaC的官方资源文件内，可以作为参考`assets/tac/models/gunskin/skin.json`  

tips：如果你发现皮肤好像没加载，请检查日志输出，这很可能是你的路径写错了

# Texture Skins
When the skin type is `texture`, it means that the skin will not modify the default model but only replace the textures, and will try to use the list of textures in `textures` to override the default textures in all models of the gun.

where the inherited parent models (TaC's default models) are all located under `assets/tac/models/special`

## Overlay Material List
Taking `ak47` as an example, this is its main model, `ak47.json`.
```json
{
	"credit": "Made with Blockbench",
	"texture_size": [256, 256],
	"textures": {
		"0": "tac:items/ak47_uv",
		"particle": "tac:items/ak47_uv"
	},
	"elements": [...]
    ...
}
```

Where `textures` is the parent model's texture list.  
If we want the skin to override some of these textures, we need to specify the corresponding paths in the skin's texture list.  
For example, if we have a golden ak and we want to override the default model's `ak47_uv.png` with a new texture called `ak47_golden.png`, then we just need to write this: `textures` is the parent model's texture list.  
Then we just need to write it like this:
```json
    "golden": {
      "type": "texture",
      "textures": {
        "0": "tac:gunskin/ak47/ak47_golden"
      },
      "icon": "tac:gunskin/icon/ak47_golden"
    }
```
This material is also included as an example in TaC's official resource file, which can be used as a reference `assets/tac/models/gunskin/skin.json`.  

Tips: If you find that the skin doesn't seem to be loading, please check the log output, it's probably because you've written the wrong path.