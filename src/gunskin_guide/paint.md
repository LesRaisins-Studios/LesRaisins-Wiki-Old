# 皮肤绘制帮助
## 开始之前
本章节的内容 **不是绘制纹理的美术或风格指南** ，仅仅是帮助读者正确获得制作皮肤所需素材（模型和纹理）的帮助文档，在阅读本章节的内容前，请确保你对mc的游戏资源文件结构/资源包制作有基本的认识  

阅读本章节的内容前，你需要掌握blockbench的基本使用方法  

[点击跳转到酒石酸菌的blockbench教程](https://www.bilibili.com/video/BV1fk4y127qg/)

## 使用Blockbench绘制TaC枪械纹理绘制

### 获取模组文件
1.右键模组并解压`tac-xxxx.jar`

2.打开解压后的文件夹，在资产中找到tac的模型`\assets\tac\models\special\`  
注意，您需要使用special文件夹下的模型文件而非items！

3.选择你想制作的模型文件，将其导入blockbench  
以`aa_12`为例，可以看到，`aa_12`是由多个零部件模型组成的，此处我们选择第一个模型`aa_12_body.json`并将其导入Blockbench中

4.在Blockbench中导入其他零部件拼合成一把完整的枪

> 文件-导入-添加Java版方块/物品模型
> 
> 选择所有未导入的零部件


5.绘制纹理
> 右上角打开`绘画模式`开始绘制纹理

## 导出资源包(legacy)
<font color="red">过时内容警告</font>  
<font color="red">本小节的内容适用于TaC 0.3.9（开发中）之前的版本</font>  
<font color="red">如果你正在为0.3.9及以上的TaC或者0.3.7及以上LesRaisins分支版本创作纹理，那么除非你想替换游戏内的默认皮肤，则以下内容不是必要的。请参阅</font> [章节：描述文件格式](./description_file.md) 
 
### 纹理存放位置
纹理贴图在材质包内的存放路径需要和模组一致，以覆盖原先的贴图  

如果你熟悉mc资源包的制作，则完全可以跳过这一节，方法与覆盖原版材质一致

以`aa12`为例，你需要把你的贴图放到如下位置：
`\assets\tac\textures\items\aa_12`且文件名需**完全一致**

然后打包即可作为普通的资源包使用

### Tips：

1. 将资源包完成后，打开游戏-选项-资源包-加载资源包
2. 尚未完成的资源包不建议压缩，你可以直接将文件夹放在resourcepacks文件夹下
3. 游戏内按`f3 + t`可以重载资源包


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