# 武器数据修改教学
## 一、提取数据
### 1.解压mod
解压mod，并在**"data/lesraisinsadd/guns"**或**"data/tac/guns"**路径下复制所有文件放入数据包
## 二、修改数据
根据需求修改完数据后，使用reload重载
# 数据包模板：
```
{  
  "general": {
  //武器是否能以全自动模式射击
  "auto": true,
  //射速，单位发每分钟
  "rate": 850,
  //武器射击模式，1半自动 2全自动 3三连发 0保险
  "rateSelector": [2, 1],
  //第三人称持枪类型
  "gripType": "tac:two_handed_ak47",
  //开火时枪口上台角度
  "recoilAngle": 2.135,
  //武器开火时枪口左右晃动的角度
  "horizontalRecoilAngle": 1.35,
  //武器向后后退的强度
  "recoilKick": 1.65,
  //当开镜时，后坐力减少的程度（按x%计算）
  "recoilAdsReduction": 0.205,
  //武器在后退过程所需时间，计算方式为1-x，该项数值越大，武器后座越快，视觉上的后坐力冲击越大
  "weaponRecoilOffset": 0.805,
  //视觉效果削弱
  "cameraRecoilModifier": 1.35,
  //玩家视角上抬所需的时间，越小的数值上抬越快。太小的数值可能看起来很晕。
  "recoilDuration": 0.225,
  //武器重量
  "weightKilo": 2.95,

//基础扩散参数。配件的增加精准度功能将在此参数上减少对应数值的百分比
  "spread": 1.565,
  //首发精准度
  "firstShotSpread": 0.15,
  //腰射散步惩罚，乘算
  "hipFireInaccuracy": 5.725,
  //连射散步惩罚所需子弹数
  "projToMinAccuracy": 8,
  //联社散步惩罚重置秒数
  "msToAccuracyReset": 320,
//移动射击散步惩罚，秒数
  "movementInaccuracy": 0.55
  },
  //弹射物
  "projectile": {
  //武器使用的弹药类型
    "item": "tac:nato_556_bullet",
	//是否能够看见射出的子弹模型
    "visible": false,
	//每次射击造成的总伤害
    "damage": 7,
	//伤害衰减起始点距离，x*射程
    "decayStart": 0.1,
	//最小伤害留存
    "minDecayMultiplier": 0.2,
	//结束距离
    "decayEnd": 0.85,
	//子弹的碰撞箱模型大小
    "size": 0.075,
	//子弹飞行速度，每方块/游戏刻
    "speed": 25,
	//子弹存在时间，tick
    "life": 9,
	//子弹尾迹长度
    "trailLengthMultiplier": 2.5
  },
  "reloads": {
  //是否通过弹匣装填。若否则单发装填。
    "magFed": true,
	// 默认最大弹容量
    "maxAmmo": 30,
	//装弹所需时间，以tick为单位
    "reloadMagTimer": 63,
	//空弹夹换弹额外所需时间
    "additionalReloadEmptyMagTimer": 27,
	//当拥有弹匣扩容附魔时，每一级增加的弹容量。生存模式可用的附魔等级仅为三级。
    "maxAdditionalAmmoPerOC": [10, 20, 30],
	//当换弹指令开始，x tick时间后无法通过射击终止武器的装填。该项是为了换弹动画准备的
    "preReloadPauseTicks": 8
  },
  #音效需要在SoundRegistry.Java中注册且通过sound.json文件引用
  "sounds": {
    "fire": "lesraisinsadd:item.hk433_fire",
    "reloadNormal": "lesraisinsadd:item.hk433_reload_norm",
    "reloadEmpty": "lesraisinsadd:item.hk433_reload_empty",
    "draw": "lesraisinsadd:item.hk433_draw",
    "inspect": "lesraisinsadd:item.hk433_inspect",
    "cock": "lesraisinsadd:item.pistol.cock",
    "silencedFire": "tac:item.ak47_fire_s"
  },
  "display": {
  //枪口火焰位置
    "flash": {
	//y轴（上下）
      "yOffset": 6.0,
	  //z轴(前后)
      "zOffset": -20.75,
      "trailAdjust": 1.325,
      "size": 0.8
    },
	//抛壳
    "shellCasing": {
      "tickLife":10,
      "yOffset": 1,
	  //左右
      "xOffset": 0,
      "zOffset": -6,
	  //大小
      "scale": 1,
      "velocityX": 8,
      "velocityY": 1,
      "velocityZ": -0.5,
      "rVelocityX": 0,
      "rVelocityY": 1.25,
      "rVelocityZ": 0.0,
      "aVelocityX": 45.0,
      "aVelocityY": -90.0,
      "aVelocityZ": 15.0,
	  //枪壳类型，shell_steel黑色的弹壳, shell_small铜色的手枪弹壳, shell_silver银色的手枪弹壳, shell_shotgun霰弹弹壳, shell_large铜色步枪弹壳, shell_huge狙击枪弹壳
      "casingModel": "tac:special/shell_large"
    },
    "hipfireScale": 1.25,
    "hipfireMoveScale": 0.5,
    "hipfireRecoilScale": 1.0,
    "showDynamicHipfire":true,
	//武器类型：0步枪, 1 机枪, 2手枪, 3 霰弹枪, 4冲锋枪, 5 狙击枪, 6RPG
    "weaponType": 0
  },
  "modules": {
  //机瞄位置
    "zoom": {
	//机瞄时fov放大(1-x)%
      "fovModifier": 0.8,
	  //高度，下加上减
      "yOffset": 14.40,
	  //远近，近加远减
      "zOffset": -1.8,
	  //左右
	  "xOffset": 0
    },
	//配件，删除相应部分即可禁用该配件
    "attachments": {
	//枪口配件(无需修改参数)
      "barrel": {
        "yOffset": -100829.84,
        "zOffset": -11.55,
        "scale": 1.00
      },
	  //枪托配件(无需修改参数)
      "stock": {
        "yOffset": 7.75,
        "zOffset": -22.05,
        "scale": 0.00
      },
	  //瞄具配件(需要修改参数将瞄具渲染到正确位置)
      "scope": {
        "yOffset": 12.2,
        "zOffset": 2.0,
        "scale": 1.0
      },
	  //扩容弹匣(无需修改参数)
      "extendedMag": {
        "yOffset": 1000.89,
        "zOffset": 5.35,
        "scale": 0.0
      },
	  //手枪瞄具(需要修改参数将瞄具渲染到正确位置)
      "pistolScope": {
        "yOffset": 7.35,
        "zOffset": 10.2,
        "scale": 1.0,
        "doRenderMount": true,
        "doOnSlideMovement": false
      },
	  //握把(无需修改参数)
      "underBarrel": {
        "yOffset": 7.799,
        "zOffset": -2.35,
        "scale": 0.00
      },
	  //镭射装置
      "irDevice": {
        "yOffset": 7.799,
        "zOffset": -2.35,
        "scale": 0.00
      }
    }
  }
}
```

---
# Weapon Data Modification
## I. Extract data
### 1. Unpack the mod
Unzip the mod and copy all the files under **"data/lesraisinsadd/guns "** or **"data/tac/guns "** and put them into the packet.
## II. Modifying Data
After modifying the data according to the requirements, use command /reload to enable all changes you have made.
# data example:
```
{  
  "general": {
  //Whether or not the weapon can fire in full auto mode
  "auto": true,
  //Rate of fire in Rounds Per Minute
  "rate": 850,
  //Weapon firing mode, 1 semi, 2 full auto, 3 burst, 0 safety.
  "rateSelector": [2, 1],
  //Third person grip type
  "gripType": "tac:two_handed_ak47",
  //Muzzle up angle when firing
  "recoilAngle": 2.135,
  //Angle at which the weapon's muzzle recoils when fired.
  "horizontalRecoilAngle": 1.35,
  //The strength of the weapon's backward recoil
  "recoilKick": 1.65,
  //How much the recoil is reduced when the gun is opened (by x%)
  "recoilAdsReduction": 0.205,
  //The time it takes for the weapon to recoil, calculated as 1-x, the larger the value, the faster the weapon recoils and the greater the visual recoil impact.
  "weaponRecoilOffset": 0.805,
  //Visual weakening
  "cameraRecoilModifier": 1.35,
  //The time it takes for the player's viewpoint to go up, the smaller the value the faster it goes up. Too small a value may look dizzying.
  "recoilDuration": 0.225,
  //Weapon weight
  "weightKilo": 2.95,

  //Base diffusion parameter. Accessories that increase accuracy will reduce this parameter by a percentage of the corresponding value.
  "spread": 1.565,
  //First Shot Accuracy
  "firstShotSpread": 0.15,
  //Penalty for shooting without aiming, multiplied by
  "hipFireInaccuracy": 5.725,
  //Number of bullets required for the spreads penalty
  "projToMinAccuracy": 8,
  //The number of seconds to reset the spreads penalty
  "msToAccuracyReset": 320,
  //Movement shooting spread penalty in seconds
  "movementInaccuracy": 0.55
  },
  "projectile": {
  //Type of ammo the weapon uses
    "item": "tac:nato_556_bullet",
	//whether the model of the projectile is visible or not
    "visible": false,
	//Total damage per shot
    "damage": 7,
	//distance from the start of damage decay, x*range  
    "decayStart": 0.1,
	//Minimum damage retention
    "minDecayMultiplier": 0.2,
	//End distance
    "decayEnd": 0.85,
	//Size of the bullet's hitbox
    "size": 0.075,
	//Bullet speed block/tick
    "speed": 25,
	//Bullet's existence time, tick
    "life": 9,
	//Bullet trail length
    "trailLengthMultiplier": 2.5
  },
  "reloads": {
  // Whether or not to load through the magazine. If otherwise single shot load.
    "magFed": true,
	// Default max ammo capacity.
    "maxAmmo": 30,
	// Time to load, in ticks.
    "reloadMagTimer": 63,
	// Extra time to reload empty magazines.
    "additionalReloadEmptyMagTimer": 27,
	// Additional ammo capacity per level when having the Magazine Expansion Enchantment. Survival Mode available attachment levels are only three.
    "maxAdditionalAmmoPerOC": [10, 20, 30],
	// When the ammo change command starts, it is not possible to terminate the weapon's loading by firing after x tick time. This item is for the bullet change animation
    "preReloadPauseTicks": 8
  },
  #Sound effects need to be registered in SoundRegistry.Java and referenced via the sound.json file
  "sounds": {
    "fire": "lesraisinsadd:item.hk433_fire",
    "reloadNormal": "lesraisinsadd:item.hk433_reload_norm",
    "reloadEmpty": "lesraisinsadd:item.hk433_reload_empty",
    "draw": "lesraisinsadd:item.hk433_draw",
    "inspect": "lesraisinsadd:item.hk433_inspect",
    "cock": "lesraisinsadd:item.pistol.cock",
    "silencedFire": "tac:item.ak47_fire_s"
  },
  "display": {
  // Position of muzzle flame
    "flash": {
	// y-axis (up and down)
      "yOffset": 6.0,
	//z-axis (front to back)
      "zOffset": -20.75,
      "trailAdjust": 1.325,
      "size": 0.8
    },
	//shell casting
    "shellCasing": {
      "tickLife":10,
      "yOffset": 1,
	//left and right
      "xOffset": 0,
      "zOffset": -6,
	//size
      "scale": 1,
      "velocityX": 8,
      "velocityY": 1,
      "velocityZ": -0.5,
      "rVelocityX": 0,
      "rVelocityY": 1.25,
      "rVelocityZ": 0.0,
      "aVelocityX": 45.0,
      "aVelocityY": -90.0,
      "aVelocityZ": 15.0,
	//Shell type, "shell_steel" black rifle shell, "shell_small" bronze pistol shell, "shell_silver" silver pistol shell, "shell_shotgun" shotgun shell, "shell_large" bronze rifle shell, "shell_huge" sniper shell.
      "casingModel": "tac:special/shell_large"
    },
    "hipfireScale": 1.25,
    "hipfireMoveScale": 0.5,
    "hipfireRecoilScale": 1.0,
    "showDynamicHipfire":true,
	//WeaponType: 0Rifle, 1MachineGun, 2Pistol, 3Shotgun, 4SubmachineGun, 5SniperGun, 6RPG
    "weaponType": 0
  },
  "modules": {
  // Position for aiming 
    "zoom": {
	//fov zoom (1-x)% on aiming
      "fovModifier": 0.8,
	  //Height
      "yOffset": 14.40,
	  //distance, near plus or minus
      "zOffset": -1.8,
	  //Left and right
	  "xOffset": 0
    },
	//Attachments, delete the corresponding part to disable the attachments.
    "attachments": {
	//Muzzle attachments (no need to change parameters)
      "barrel": {
        "yOffset": -100829.84,
        "zOffset": -11.55,
        "scale": 1.00
      },
	  //Stock accessories (no need to change parameters)
      "stock": {
        "yOffset": 7.75,
        "zOffset": -22.05,
        "scale": 0.00
      },
	  //Scope attachments (parameters need to be changed to render the scope to the correct position)
      "scope": {
        "yOffset": 12.2,
        "zOffset": 2.0,
        "scale": 1.0
      },
	  //Extended Magazine (no need to change parameters)
      "extendedMag": {
        "yOffset": 1000.89,
        "zOffset": 5.35,
        "scale": 0.0
      },
	  //Pistol Sight (no need to modify parameters)
      "pistolScope": {
        "yOffset": 7.35,
        "zOffset": 10.2,
        "scale": 1.0,
        "doRenderMount": true,
        "doOnSlideMovement": false
      },
	  //grip (no need to change parameters)
      "underBarrel": {
        "yOffset": 7.799,
        "zOffset": -2.35,
        "scale": 0.00
      },
	  //laser device (no need to change parameters)
      "irDevice": {
        "yOffset": 7.799,
        "zOffset": -2.35,
        "scale": 0.00
      }
    }
  }
}
```