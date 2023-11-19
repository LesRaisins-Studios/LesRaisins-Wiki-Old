## Skinning Tutorial
## Before You Begin
The content of this section **is not an art or style guide for drawing textures**, it is just a help document to help readers get the materials (models and textures) needed to make skins correctly. Before reading this section, please make sure you have a basic understanding of mc's game resource file structure/resource pack creation.  

Before reading this chapter, please make sure you have a basic understanding of mc's game resource file structure/resource pack creation.  

[Click to jump to blockbench tutorial for tartaric acid bacteria](https://www.bilibili.com/video/BV1fk4y127qg/)

## Using Blockbench to draw TaC gun texture drawing

### Get the module file
1. Right click on the module and extract `tac-xxxx.jar`.

2. Open the extracted folder and find the tac's models in the assets `\assets\tac\models\special\`.  
Note that you need to use the model files in the folder **special** instead of **items**!

3. Select the model file you want to make and import it into blockbench  
Take `aa_12` as an example, you can see that `aa_12` is composed of several parts models, here we select the first model `aa_12_body.json` and import it into Blockbench.

4. Import other parts into Blockbench to build a complete gun.

> File-Import-Add Java version of the block/item model.
> 
> Select all unimported parts


5. Painting Texture
> Turn on `Paint Mode` in the upper right corner and start painting the texture.

## Exporting Resourcepacks(legacy)
<font color="red">Outdated content warning</font>  
<font color="red">The content of this subsection applies to versions of TaC prior to TaC 0.3.9 (in development)</font>  
<font color="red">If you are creating textures for TaC 0.3.9 and above or LesRaisins branch versions 0.3.7 and above, then the following is not necessary unless you want to replace the default in-game skins. See also.</font> [Chapter: Describing File Formats](./description_file.md) 
 
### Texture file storage location
The texture file need to be stored in the same path in the material pack as the module in order to overwrite the original mapping 

If you are familiar with the creation of mc resource packs, then you can skip this section entirely, in the same way as overriding the original texture

Using `aa12` as an example, you need to put your textures in the following location:
`\assets\tac\textures\items\aa_12` and the filenames need to be **exactly** the same

Then you can package it up and use it as a normal resource package

### Tips：

1. After finishing the resourcepacks, open the game - Options - Resourcepacks - Load Resourcepacks
2. It is not recommended to compress unfinished resource packs, you can just put the folder in the resourcepacks folder
3. Press `f3 + t` to reload the resource packs in-game.