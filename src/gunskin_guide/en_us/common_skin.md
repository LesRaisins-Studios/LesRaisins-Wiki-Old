<style>
  table:{
    margin-left: 0.1%
  }
</style>
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