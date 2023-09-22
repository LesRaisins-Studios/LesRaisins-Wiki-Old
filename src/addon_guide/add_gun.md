# 添加第一把枪

## 注册物品
TaC的枪械物品都继承`TimelessGunItem`，除了物品所在的组，你还可以指定默认修饰器，详见`TimelessGunItem`的构造器    
修饰器的作用是在枪械原先的基础上额外进行一些属性的调整（实现`IGunModifier`接口），比如配件，具体用法在后面的章节会有详细说明

以下是一个简单的例子（比如，这里暂时借用了`ak47`的默认修饰器`GunModifiers.AK47_MOD` ）  
```java
    //...
    public static final DeferredRegister<Item> REGISTER = DeferredRegister
        .create(ForgeRegistries.ITEMS, Reference.MOD_ID);
    public static final RegistryObject<GunItem> HCAR = REGISTER
        .register("hcar",
            () -> new TimelessGunItem(
                properties -> properties.tab(GunMod.RIFLE),
                GunModifiers.AK47_MOD
            )
        );
```
（本章节之后的内容里，都将以这把`hcar`作为例子）

别忘了在你的主类里加入注册
```java
    //...
    IEventBus bus = FMLJavaModLoadingContext.get().getModEventBus();
    ModItems.REGISTER.register(bus);
```

现在，打开游戏，你应该能看见在创造模式物品栏中`突击步枪`一栏中多出了一个紫黑块（而且拿出来应该游戏还会崩溃）
