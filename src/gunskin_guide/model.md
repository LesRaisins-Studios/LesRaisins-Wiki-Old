<style>
    table {
        margin-left: 0.1%
    }
</style>
# 枪械模型部件说明

## 总表
本表为参考命名表，仅作为今后加入的模型部件命名的参考规范，实际枪械的各部件名以各枪械具体的部件表为准。  
特别的，主要枪体的部件名为`main`，即枪在游戏中的注册名去掉`<命名空间>`的部分。


### 特殊
| 部件名        | 一般意义               |
|------------|--------------------|
| clumsyyy   | Timeless_50 中的特殊装饰 |
| nekooo     | Timeless_50 中的特殊装饰 |
| body_light | vector45 中的前端标志    |


### 主要部分
| 部件名  | 一般意义           |
|------|----------------|
| main | 一个模型中不会改变的恒定部分 |


### 枪管
| 部件名             | 一般意义                   |
|-----------------|------------------------|
| barrel          | 默认枪管（一般在枪管超长的时候用于调整位置） |
| barrel_extended | 延长枪管（几乎不会出现）           |
| barrel_short    | 短枪管（几乎不会出现）            |
| barrel_standard | 标准枪管（几乎不会出现）           |


### 脚架
| 部件名   | 一般意义                 |
|-------|----------------------|
| bipod | 脚架（一般在脚架超长的时候用于调整位置） |


### 枪栓
| 部件名         | 一般意义                    |
|-------------|-------------------------|
| bolt        | 枪栓（一般是抛壳窗上的那个挡板）        |
| bolt_extra  | 枪栓（仅栓动式步枪有，一般是枪栓后的阻铁部分） |
| bolt_handle | 部分武器上枪栓外侧的拉柄部分          |


### 子弹
| 部件名                | 一般意义              |
|--------------------|-------------------|
| bullet             | 子弹                |
| bullet1            | 子弹（编号 1）          |
| bullet2            | 子弹（编号 2）          |
| bullet_chain       | 弹链                |
| bullet_chain_cover | 弹链衬底（m249 的那块金属板） |
| bullet_head        | 子弹头               |
| bullet_shell       | 子弹壳               |


### 机匣盖
| 部件名 | 一般意义           |
|-----|----------------|
| cap | 一般是机枪的那块机匣上的盖板 |


### 提把
| 部件名   | 一般意义         |
|-------|--------------|
| carry | m4 枪族的可拆卸式提把 |


### 握把
| 部件名           | 一般意义 |
|---------------|------|
| grip_light    | 轻型握把 |
| grip_tactical | 战术握把 |


### 击锤
| 部件名    | 一般意义 |
|--------|------|
| hammer | 枪械击锤 |


### 护木
| 部件名                 | 一般意义              |
|---------------------|-------------------|
| hand_guard_default  | 默认护木（几乎不会出现）      |
| hand_guard_extended | 延长护木（几乎不会出现）      |
| hand_guard_short    | 短护木（几乎不会出现）       |
| hand_guard_standard | 标准护木（一般无法安装配件或导轨） |
| hand_guard_tactical | 战术护木（用于安装配件或导轨）   |


### 拉机柄
| 部件名          | 一般意义            |
|--------------|-----------------|
| handle       | 拉机柄             |
| handle_extra | sig_mcx 独有的双拉机柄 |


### 镭射配件
| 部件名                | 一般意义    |
|--------------------|---------|
| laser_basic        | 小型镭射光线  |
| laser_basic_device | 小型镭射装置  |
| laser_ir           | ir 镭射光线 |
| laser_ir_device    | ir 镭射装置 |


### 弹匣
| 部件名          | 一般意义           |
|--------------|----------------|
| mag          | 无弹匣配件改模效果的默认弹匣 |
| mag_drum     | 弹鼓             |
| mag_extended | 扩容弹匣           |
| mag_standard | 标准弹匣           |


### 枪口
| 部件名                | 一般意义 |
|--------------------|------|
| muzzle_default     | 默认枪口 |
| muzzle_brake       | 制退器  |
| muzzle_compensator | 补偿器  |
| muzzle_silencer    | 消声器  |


### 滑动块
| 部件名  | 一般意义                |
|------|---------------------|
| pull | 在枪管内滑动，链接枪栓和枪栓拉柄的部分 |


### 套筒
| 部件名  | 一般意义      |
|------|-----------|
| pump | 泵动式霰弹枪的套筒 |


### 导轨
| 部件名                 | 一般意义                        |
|---------------------|-----------------------------|
| rail_cover          | 导轨上的防滑垫（用于握持，不能和配件同时装）      |
| rail_cover_under    | 导轨底端的防滑垫                    |
| rail_cover_side     | 导轨侧边的防滑垫                    |
| rail_cover_top      | 导轨顶上的防滑垫（如果没有独立分开需求，就使用第一个） |
| rail_default        | 默认导轨（一般没有安装配件的地方）           |
| rail_extended       | 战术导轨（用于安装配件的导轨）             |
| rail_extended_under | 底部的战术导轨                     |
| rail_extended_side  | 侧边的战术导轨                     |
| rail_extended_top   | 上部的战术导轨（如果没有独立分开需求，就使用第一个）  |
| rail_scope          | 用于安装瞄具的导轨部分，以及镜桥            |


### 弹匣释放片/按钮
| 部件名     | 一般意义     |
|---------|----------|
| release | 弹匣释放片/按钮 |


### 火箭弹
| 部件名    | 一般意义      |
|--------|-----------|
| rocket | rpg7 的火箭弹 |


### 照门
| 部件名                | 一般意义             |
|--------------------|------------------|
| sight              | 默认照门             |
| sight_folded       | 折叠照门（一般在安装瞄具后折叠） |
| sight_folded_light | 折叠照门的荧光部分        |
| sight_light        | 默认照门的荧光部分        |


### 手枪套筒
| 部件名                  | 一般意义      |
|----------------------|-----------|
| slide                | 默认套筒      |
| slide_extended       | 延长套筒      |
| slide_extended_light | 延长套筒的荧光部分 |
| slide_light          | 默认套筒的荧光部分 |


### 枪托
| 部件名            | 一般意义 |
|----------------|------|
| stock_default  | 默认枪托 |
| stock_folded   | 折叠枪托 |
| stock_light    | 轻型枪托 |
| stock_tactical | 战术枪托 |
| stock_heavy    | 重型枪托 |


## 各枪械具体部件表  
各个枪械的详细模型部件表。其中，`默认模型路径`全部位于`tac:models/special`下


### ak47
枪械标识符: `ak47`  

| 部件名                | 说明         | 默认模型路径                  |
|--------------------|------------|-------------------------|
| main               | 主要枪体       | ak47                    |
| rail_scope         | 附件(安装瞄具)   | ak47_rail_scope         |
| bolt               | 枪机         | ak47_bolt               |
| stock_light        | 轻型枪托       | ak47_stock_light        |
| stock_tactical     | 战术枪托       | ak47_stock_tactical     |
| stock_heavy        | 重型枪托       | ak47_stock_heavy        |
| muzzle_brake       | 制退器        | ak47_muzzle_brake       |
| muzzle_compensator | 补偿器        | ak47_muzzle_compensator |
| muzzle_silencer    | 消音器        | ak47_muzzle_silencer    |
| mag_standard       | 弹匣(无拓展)    | ak47_mag_standard       |
| mag_extended       | 弹匣(安装任意拓展) | ak47_mag_extended       |


# Firearms Model Parts Description

## Summary Table
This table is a reference naming list, and is only used as a reference specification for naming model parts for future additions; the actual names of each part of a gun are based on the specific parts list for each gun.  
In particular, the part name of the main gun body is `main`, i.e. the gun's in-game registered name minus the `<namespace>` part.

### SPECIAL
| PartsName  | Meanings           |
|------------|--------------------|
| clumsyyy   | Timeless_50 's special decoration |
| nekooo     | Timeless_50 's special decoration |
| body_light | vector45 's front-end flags    |


### MAIN PART
| PartsName  | Meanings           |
|------|----------------|
| main | A constant part of a model that does not change |


### BARREL
| PartsName             | Meanings                   |
|-----------------|------------------------|
| barrel          | Default barrel (generally used to adjust position when the barrel is extra long) |
| barrel_extended | Extended barrel (hardly ever)          |
| barrel_short    | Short barrels (hardly ever)            |
| barrel_standard | Standard barrels (hardly ever)         |


### BIPOD
| PartsName   | Meanings                 |
|-------|----------------------|
| bipod | bipod (generally used to adjust the position when the bipod is extra long) |


### BOLT
| PartsName         | Meanings                    |
|-------------|-------------------------|
| bolt        | Bolt (usually the stopper on the case throwing window)        |
| bolt_extra  | Bolt (bolt-action rifles only, usually the iron blocking portion behind the bolt) |
| bolt_handle | The outer part of the pull handle on the bolt on some weapons          |


### BULLET
| PartsName                | Meanings              |
|--------------------|-------------------|
| bullet             | bullet                   |
| bullet1            | bullet (No. 1)           |
| bullet2            | bullet (No. 2)           |
| bullet_chain       | bullet_chain             |
| bullet_chain_cover | bullet_chain_cover（The metal plate from the m249） |
| bullet_head        | bullet_head              |
| bullet_shell       | bullet_shell             |


### CAP
| PartsName | Meanings           |
|-----|----------------|
| cap | It's usually the cover plate on the magazine of a machine gun. |


### CARRY
| PartsName   | Meanings         |
|-------|--------------|
| carry | Detachable carrying handle for the m4 gun family |


### GRIP
| PartsName           | Meanings |
|---------------|------|
| grip_light    | light grip    |
| grip_tactical | tactical grip |


### HAMMER
| PartsName    | Meanings |
|--------|------|
| hammer | hammer |


### HAND GUARD
| PartsName                 | Meanings              |
|---------------------|-------------------|
| hand_guard_default  | Default wood guard (hardly ever occurs)      |
| hand_guard_extended | Extension of hand guards (hardly ever occurs)      |
| hand_guard_short    | Short hand guards (almost never occurs)       |
| hand_guard_standard | Standard hand guards (fittings or rails are generally not available) |
| hand_guard_tactical | Tactical hand guards (for mounting fittings or rails)   |


### HANDLE
| PartsName          | Meanings            |
|--------------|-----------------|
| handle       | handle             |
| handle_extra | sig_mcx unique double pull handle |


### LASER
| PartsName                | Meanings    |
|--------------------|---------|
| laser_basic        | Compact laser light  |
| laser_basic_device | Compact laser device  |
| laser_ir           | ir laser light |
| laser_ir_device    | ir Radium device |


### MAGAZINE
| PartsName          | Meanings           |
|--------------|----------------|
| mag          | Default magazines without magazine accessory remodeling effect |
| mag_drum     | magazine drum               |
| mag_extended | extended magazines          |
| mag_standard | standard magazines          |


### MUZZLE
| PartsName                | Meanings |
|--------------------|------|
| muzzle_default     | default muzzle |
| muzzle_brake       | brake  |
| muzzle_compensator | compensator  |
| muzzle_silencer    | silencer  |


### PULL
| PartsName  | Meanings                |
|------|---------------------|
| pull | The part that slides inside the barrel and links the bolt to the bolt handle. |


### PUMP
| PartsName  | Meanings      |
|------|-----------|
| pump | pump for pump-action shotguns |


### RAIL
| PartsName                 | Meanings                        |
|---------------------|-----------------------------|
| rail_cover          | Non-slip pads on guides (for grip, not to be fitted at the same time as accessories)      |
| rail_cover_under    | Anti-slip pads on the bottom of the guides                    |
| rail_cover_side     | Anti-slip pads on the side of the guides                   |
| rail_cover_top      | Non-slip pads on top of the guides (use the first one if there is no need for separate separation) |
| rail_default        | Default rail (generally no place to install accessories)           |
| rail_extended       | Tactical rails (rails for mounting accessories)             |
| rail_extended_under | Tactical rail at the bottom                     |
| rail_extended_side  | Side tactical rails                     |
| rail_extended_top   | Upper tactical rail (use the first one if there is no need for separate separation)  |
| rail_scope          | Rail section for mounting sights, and claw mounts            |


### RELEASE
| PartsName     | Meanings     |
|---------|----------|
| release | Magazine release tab/button |


### ROCKET
| PartsName    | Meanings      |
|--------|-----------|
| rocket | RPG7 rockets |


### SIGHTS
| PartsName                | Meanings             |
|--------------------|------------------|
| sight              | default sight             |
| sight_folded       | Folding sight (usually folded after scope are installed) |
| sight_folded_light | The fluorescent part of the sight        |
| sight_light        | The fluorescent part of the folding sight        |


### SLIDE
| PartsName                  | Meanings      |
|----------------------|-----------|
| slide                | default slide      |
| slide_extended       | extended slide      |
| slide_extended_light | The fluorescent part of the default slide |
| slide_light          | The fluorescent part of the extended slide |


### STOCK
| PartsName            | Meanings |
|----------------|------|
| stock_default  | defalut stock |
| stock_folded   | folded stock |
| stock_light    | light stock |
| stock_tactical | tactical stock |
| stock_heavy    | heavy stock |


## Detailed parts list for each firearm  
Detailed model parts lists for each firearm. The `default model paths` are all located under `tac:models/special`.


### ak47
Gun identifier: `ak47'  

| PartsName                | Meanings         | Default Model Path                  |
|--------------------|------------|-------------------------|
| main               | Main body       | ak47                    |
| rail_scope         | Attachment (mounting sights)   | ak47_rail_scope         |
| bolt               | bolt         | ak47_bolt               |
| stock_light        | light stock       | ak47_stock_light        |
| stock_tactical     | tactical stock       | ak47_stock_tactical     |
| stock_heavy        | heavy stock       | ak47_stock_heavy        |
| muzzle_brake       | brake        | ak47_muzzle_brake       |
| muzzle_compensator | compensator        | ak47_muzzle_compensator |
| muzzle_silencer    | silencer        | ak47_muzzle_silencer    |
| mag_standard       | Magazine (no expansion)    | ak47_mag_standard       |
| mag_extended       | Magazine (with any expansion installed) | ak47_mag_extended       |