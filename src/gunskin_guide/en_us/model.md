<style>
    table {
        margin-left: 0.1%
    }
</style>
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
