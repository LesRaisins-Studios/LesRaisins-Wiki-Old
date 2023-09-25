# 开始制作一个TaC附属包

## 导入依赖
在build.gradle中添加 
```gradle
repositories {
    maven {
        url = "https://www.cursemaven.com"
    }
}
dependencies {
    implementation fg.deobf('curse.maven:obfuscate-289380:3336021')
    implementation fg.deobf('curse.maven:tac-491264:<verison>')
}
```

请注意，从`0.3.9`开始，因为某些严重的问题，`curios`不再作为TaC的前置（防弹衣相关内容被暂时移除），所以你可以不必添加他  
介于截止至本指南撰写时，`0.3.9`尚未在curseforge上发布，你可能需要从本地导入TaC作为前置，具体请参考：  
[Forge Documentation](https://docs.minecraftforge.net/en/fg-5.x/dependencies/)  
当然，你也可以下载TaC的源码并建立本地仓库

## mods.toml
```toml
[[dependencies.${mod_id}]]  
   modId="tac"  
   mandatory=true  
   versionRange="[0.3.9.1,)"  
   ordering="AFTER"  
   side="BOTH"  
```

---
完成以上步骤后，点击`runClient`，你应该能在测试客户端中看到你的mod和tac正常加载