<style>
  table:{
    margin-left: 0.1%
  }
</style>
# 皮肤资源包制作指南

## 开始之前
欢迎来到LesRaisins提供的tac皮肤资源包制作指南

### 请注意：  
1. 本指南不是皮肤本身的纹理绘制或模型制作的美术教程，而仅仅是帮助读者正确创作枪械模型/纹理、以及将已经制作好的皮肤纹理与模型实装进游戏的说明文档，同时，为了避免阅读障碍，也请确保在阅读本章节的内容掌握基础的资源包制作知识和相关概念； 
2. 本指南的部分页面与小节可能带有`legacy`标识，这代表这部分内容可能不适用于最新版的TaC，详情请参阅对应页面的说明  
3. 本指南中许多示例内容的具体文件都包含在TaC本体的资产文件夹中，如果你觉得本指南描述的不够直观，不妨直接打开源文件看看，也许有助于理解

## 一些说明
### 关于模型
在游戏中tac最终呈现的枪械的`完整的模型`是由一系列来自不同文件的模型组合而来的；  

对于这一系列模型，我们在本指南中其称之为`模型部件`或者`部件`；  


## 制作一个枪械皮肤
关于如何正确获取原始素材和开始绘制皮肤，请参阅 [章节：皮肤绘制帮助](./gunskin_guide/paint.md)

## 描述文件格式
要让模组读取资源包里的枪械皮肤，你需要在资源包里添加一个json文件以描述皮肤  
具体的路径为
`assets/<命名空间>/models/gunskin/skin.json`  
你可以这个文件放到任意一个命名空间的对应路径下，这会决定你接下来皮肤的命名空间。（其中，TaC 的`<命名空间>`为`tac`）

关于`描述文件`的详细内容，请参阅 [章节：描述文件格式](./gunskin_guide/description_file.md)


## 调用皮肤
贼简单,`/give @s tac:ak47{Skin:"<皮肤命名空间>:<皮肤标识符>"}`,可以不加命名空间,默认是`tac`,
比如有一把ak的皮肤,`skin.json`放在`tac`的命名空间里,比如上例中的黄金和白银ak,
就是`/give @s tac:ak47{Skin:"golden"}` `/give @s tac:ak47{Skin:"tac:silver"}`  

---
## Skin Resource Pack Creation Guide

## Before You Begin ##
Welcome to the tac skin resource pack creation guide from LesRaisins.

### Please note:  
1. This guide is not an art tutorial for texturing or modelling the skins themselves, but simply a document to help the reader to properly create gun models/textures, and to actualise the skins textures and models that have already been created into the game, and to avoid any dyslexia, please make sure that you have a good understanding of the basics of Resource Pack creation and the concepts involved in it when reading through the contents of this section; 
2. some pages and sections of this guide may be marked with a `legacy` symbol, which means that the content may not be applicable to the latest version of TaC, please refer to the corresponding page for details.  
3. Many of the example files in this guide are contained in the assets folder of TaC itself, so if you feel that this guide is not intuitive enough for you, you may want to open the source files directly to see them, which may help you understand them.

## Some notes
### About the model
The `complete model` of the gun that tac eventually presents in the game is a combination of a series of models from different files;  

For the purposes of this guide, we will refer to these models as `model parts` or `components`;  


## Making a gun skin
For information on how to get the source material right and start skinning, see [Section: Skinning Help](. /gunskin_guide/paint.md)

## Describe file format
To allow the module to read the gun skins in the resource pack, you need to add a json file to the resource pack to describe the skins.  
The specific path is
`assets/<namespace>/models/gunskin/skin.json`.  
You can put this file in any namespace you want, which will determine the namespace of your next skin. (where `<namespace>` for TaC is `tac`)

For details on `description files`, see [section: Description file format](. /gunskin_guide/description_file.md)


## Getting a skined gun
It's easy, `/give @s tac:ak47{Skin:"<skin namespace>:<skin identifier>"}`, you can leave out the namespace, it defaults to `tac`.
For example, if there is a skin for an ak, `skin.json` is placed in the `tac` namespace, such as the gold and silver ak in the above example.
is `/give @s tac:ak47{Skin: "golden"}` `/give @s tac:ak47{Skin: "tac:silver"}`
