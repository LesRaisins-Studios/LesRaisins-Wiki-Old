# 添加第一把枪

## 注册物品
TaC的枪械物品都继承`TimelessGunItem`，除了物品所在的组，你还可以指定默认修饰器，详见`TimelessGunItem`的构造器    
修饰器的作用是在枪械原先的基础上额外进行一些属性的调整（实现`IGunModifier`接口），比如配件，具体用法在后面的章节会有详细说明

以下是一个简单的例子（比如，这里暂时借用了`ak47`的默认修饰器`GunModifiers.AK47_MOD`  ）  
```java
public class ModItems {
    public static final DeferredRegister<Item> REGISTER = DeferredRegister
        .create(ForgeRegistries.ITEMS, Reference.MOD_ID);
    public static final RegistryObject<GunItem> HCAR = REGISTER
        .register("hcar",
            () -> new TimelessGunItem(
                properties -> properties.tab(GunMod.RIFLE),
                GunModifiers.AK47_MOD
            )
        );
}
```

别忘了在你的主类里加入注册
```java
    //...
    IEventBus bus = FMLJavaModLoadingContext.get().getModEventBus();
    ModItems.REGISTER.register(bus);
```