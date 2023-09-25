# 模型的实际渲染类
完成模型和动画的加载后，我们还需要实现一个接口来控制枪械模型的实际渲染
`IOverrideModel`  
我们主要需要实现里面的`render`方法  
关于`render`方法各个参数的意义，你可以参阅`IOverrideModel`中的注释  
```java
    /**
     * Renders the overridden model.
     *
     * @param partialTicks  the current partial ticks
     * @param transformType the camera transform type
     * @param stack         the itemstack of the item that has the overridden model
     * @param parent        if an attachment, the parent is the weapon this attachment is attached to otherwise it's an empty stack.
     * @param entity        the entity holding the item
     * @param matrixStack   the current matrix stack
     * @param buffer        a render type buffer get
     * @param light         the combined light for the item
     * @param overlay       the overlay texture for the item
     */
```

当然，TaC提供了一个方便渲染枪械的抽象类`SkinAnimationModel`，里面实现了一部分可以用来偷懒的方法，比如快速根据配件决定要渲染哪个部件模型（前提是你使用了推荐的部件命名）

## 基本流程
我们要做的工作很简单：为所有模型部件指定他应该跟着什么动

简单来说，在渲染枪械的时候，基本流程如下：
- 获取动画控制器以及模型（GunSkin）
- 找到每一个会独立运动的部件组
  - push
  - 调用动画控制器的`applySpecialModelTransform`，其中第二个参数是前一章中这个部件组对应的node
  - 渲染模型
  - pop
-  调用`PlayerHandAnimation`的`render`方法渲染手

还是以hcar为例：
```java
    @Override
    public void render(float v, ItemCameraTransforms.TransformType transformType, ItemStack stack, ItemStack parent, LivingEntity entity, MatrixStack matrices, IRenderTypeBuffer renderBuffer, int light, int overlay) {
        //获取模型控制器和皮肤（也就是模型）
        HCARAnimationController controller = HCARAnimationController.getInstance();
        GunSkin skin = SkinManager.getSkin(stack);
        
        matrices.pushPose();//push！
        {
            //通过动画控制器调整模型的位置等等
            controller.applySpecialModelTransform(getModelComponent(skin, BODY), HCARAnimationController.INDEX_BODY, transformType, matrices);
            //渲染主要模型
            RenderUtil.renderModel(getModelComponent(skin, BODY), stack, matrices, renderBuffer, light, overlay);
            //你可以直接使用RenderUtil里的方法，也可以使用SkinAnimationModel里的方法
        }
        matrices.popPose();//pop！
        //弹匣在动画中会独立运动，push一个新的
        matrices.pushPose();
        {
            controller.applySpecialModelTransform(getModelComponent(skin, BODY), HCARAnimationController.INDEX_MAG, transformType, matrices);
            renderMag(stack, matrices, renderBuffer, light, overlay, skin);
        }
        matrices.popPose();

        matrices.pushPose();
        {
            controller.applySpecialModelTransform(getModelComponent(skin, BODY), HCARAnimationController.INDEX_PULL, transformType, matrices);
            RenderUtil.renderModel(getModelComponent(skin, PULL), stack, matrices, renderBuffer, light, overlay);
        }
        matrices.popPose();

        PlayerHandAnimation.render(controller, transformType, matrices, renderBuffer, light);
    }
```

## 额外偏移
有些时候，枪械模型的部分部件会过长以至于超出了mc模型的坐标上限（表现为在bb里拖不出去），比如部分枪具有的超长枪管，或者消音器，那么这时候你需要在代码层面对其进行调整  
如果你继承的是`SkinAnimationModel`，那么只要在你的类构造器中的 
```java
   protected Map<ModelComponent, Vector3d> extraOffset = new HashMap<>();
```
里`put`部件的额外偏移就可以了  
（其实这玩意本来准备放到`GunSkin`里面作为皮肤功能的一部分的... 但是，我偷懒了，欸嘿）  

当你调用`renderComponent`及其相关方法时，这些偏移会自动应用  
如果你使用的是`RenderUtil`里的方法，那么你需要自行调用`MatrixStack`里的方法调整模型的输出位置