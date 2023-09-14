# 使用Blockbench绘制自定义TaC枪械纹理绘制
[blockbench使用教程](https://www.bilibili.com/video/BV1fk4y127qg/)

## 使用Blockbench绘制TaC枪械纹理绘制

### 一、教学概述
鉴于近日LesRaisins玩家社区有较多玩家希望绘制专属于自己的TaC枪械纹理皮肤却不知如何下手，以及有部分纹理艺术家在创作时使用了错误的模型文件。本着为方便纹理艺术家对TaC模组创作自定义纹理为目的，解决新人在创作时容易遇到的问题，下文是本人(LeComte)撰写的使用Blockbench绘制TaC纹理的教学。本教学主要针对零Blockbench基础的玩家，以及指出正确的模型文件，避免艺术家们使用错误的模型绘制。若有不足，请多谅解。

### 二、操作步骤
1.右键模组选择解压

2.打开模型目录\tac-r-0.3.5.1-1.16.5\assets\tac\models\special\注意，您需要使用special文件夹下的模型文件而非items！

3.选择你想制作的模型文件，将其导入blockbench。下文以**aa_12**为例可以看到**aa_12**是由多个零部件模型组成的，此处我们选择第一个模型"aa_12_body.json"将其导入Blockbench中

4.在Blockbench中导入其他零部件组装成一把完整的枪

> 文件-导入-添加Java版方块/物品模型
> 
> 选择所有未导入的零部件
> 
5.绘制纹理
> 右上角打开绘画模式开始绘制纹理

### 三、压缩资源包
**1.新建以下路径**

\mytexture\assets\tac\textures\items\aa_12纹理贴图存放路径需要和模组一致，

如aa_12的纹理贴图在模组中存放在**tac-r-0.3.5.1-1.16.5\assets\tac\textures\items\aa_12**文件夹中

则你需要将你的**贴图**存放在\mytexture\assets\tac\textures\items\aa_12文件夹内，且**文件名需一致**


**2.新建资源包识别文件**
在mytexture目录下新建一个pack.mcmeta文件
在里面粘贴以下代码：
~~~
"pack": {
    "pack_format":6,
    "description": "我的TaC模组纹理资源包"
  }
}
~~~
保存该文件后，将mytexture文件夹压缩为mytexture.zip，并将其放入.minecraft/resourcepacks文件夹内


### 四、加载资源包

1.打开游戏-选项-资源包-加载资源包

2.尚未完成的资源包不建议压缩，直接将文件夹放在resourcepacks文件夹下

3.游戏内按f3+t可以重载资源包