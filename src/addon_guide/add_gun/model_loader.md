# 加载模型
为枪械加载模型非常简单。由于一把枪可能有一大堆模型（加之此前灾难级别的模型命名），同时为了加入了新的皮肤系统，TaC从`0.3.9`开始更改了枪械模型的加载方式，你只需要实现`com.tac.guns.client.gunskin`下的`SkinLoader`类并按正确的格式命名你的部件文件即可  

当然，如果你没有什么特别的需求，你也可以直接为你的新枪创建一个新的`SkinLoader`对象，这个类中提供了一些基础的加载默认模型及其皮肤的方法  

以下是一个简单的例子
```java
    public static SkinLoader HCAR = new SkinLoader(ModItems.HCAR.getId(),
            BODY,MAG_STANDARD,MAG_EXTENDED,PULL);
```

不要忘了在你的主类构造器中为枪械注册模型加载器
```java
    SkinLoader.register(ModItems.HCAR.getId(),HCAR);
```

## 模型部件
`SkinLoader`接受两个参数，即枪械的注册名`ResourceLocation`和它的部件列表`ModelComponent`  

`ModelComponent`是一个枚举类，他决定了默认情况下模型文件名的后缀  
其中唯一的属性`key`即为对应的模型文件名后缀  

关于模型部件的推荐命名规范，请参见[章节：模型部件列表](./gunskin_guide/model.md)

你只需将对应的模型文件放置到默认的模型路径`<your_namespace>:special/`下，TaC就会自动尝试加载这些模型  

比如上例中，`hcar`具有`BODY`, `MAG_STANDARD`, `MAG_EXTENDED`, `PULL` 四个模型部件，那么它们对应的文件名应该是`hcar.json`, `hcar_mag_standard.json`, `hcar_mag_extended.json`, `hcar_pull.json`

## 什么情况下应该将部件从枪械中分离？
部件**当且仅当**其会在动画中**独立运动**（比如弹匣和枪机等）或是**存在状态变化**（安装配件时展示不同的枪托/枪口）时，才应该分离成独立模型文件，否则他应该跟随主模型或其他模型文件

对于会发生状态变化的部件，你需要将他的**每一个状态**分离为单独的模型