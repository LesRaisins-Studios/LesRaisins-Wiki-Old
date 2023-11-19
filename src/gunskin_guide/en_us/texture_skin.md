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