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