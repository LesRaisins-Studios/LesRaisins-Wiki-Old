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


