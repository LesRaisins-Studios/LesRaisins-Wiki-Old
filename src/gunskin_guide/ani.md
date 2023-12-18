# 动画制作教学
## 动画制作
- 导入模型  
   打开Blockbench,创建自由模型，导入枪械及手部模型  
   ![图片](https://s1.3hov.com/lesraisins/i/2023/11/02/1.png)  
   > 要点注意：  
   >> 1.手部模型T为虎口，L为左手；  
   >> 2.枪口朝向北方；  
   >> 3.文件夹大纲路径：  
   >>> 枪所有不可动的部件分为一组，所有可动部分单独分为一组，如aug动画过程中需要移动弹匣和拉柄，则单独创建aug_magazine和aug_charge分组  
   >>> 左右手RightHand的枢轴点必须为8 8 8，为方便编辑，将其套入L R组，此后的动画编辑均在这两组上执行
   >> 4.尺寸：双手武器手臂父级（L，R）缩放为1 1.5 1，手枪类手臂父级缩放为1.75 2 1.75
- 动画制作  
   动画包括1.持枪:static_state；2.掏枪：draw；3.检视：inspect；4.换弹：reload_norm；5.空仓换弹：reload_empty  
   ![图片](https://s1.3hov.com/lesraisins/i/2023/11/02/2.png)  
   > 要点注意：  
   >> 1.所有动画结束状态(位置，旋转，大小)需和static_state一致，否则会导致模型播放动画后错位  
   >> 2.除static_state外，所有动画在第二帧开始制作（时间轴显示为1） 
## 动画导出
- 删除所有块，及无用组  
   进入编辑模式，删除所有模型块。其次删除所有不会动模型的分组，以P90为例，需要删除aug_default分组以及所有块.  
- 导出动画  
   进入动画模式，每次导出一个动画。即在左上方动画窗口处，删剩1个动画后，在文件-导出-导出glTF模型，模型命名为p90_static_state.gltf  
   并依次导出其他所有动画
# Animation tutorials
## Animation
- Import model  
   Open Blockbench, create a **Generic Model**, import the gun and hand model.  
   ! [Image](https://s1.3hov.com/lesraisins/i/2023/11/02/1.png)  
   > Import the gun and hand models:  
   >> 1. The hand model T is the purlicue(the space between the forefinger and thumb), L is the left hand;  
   >> 2. The muzzle of the gun is facing north;  
   >> 3. Folder outline path:  
   >>> All the immovable parts of the gun are divided into a group, and all the movable parts are divided into a group separately, such as aug animation process needs to move the magazine and pull handle, then create aug_magazine and aug_charge group separately.  
   >>> The **Pivot Point** of RightHand Lefthand must be 8 8 8, in order to facilitate the editing, it will be set into L R group, and the animation editing will be executed on these two groups after that.
   >> 4. Size: two-handed weapon arm parent (L, R) scaled to 1 1.5 1, pistol-like arm parent scaled to 1.75 2 1.75
- Animation  
   The animation includes 1. holding the gun: static_state; 2. pulling out the gun: draw; 3. inspecting: inspect; 4. changing the bullet: reload_norm; 5. changing the bullet empty: reload_empty  ;6. fire: fire
   ! [Image](https://s1.3hov.com/lesraisins/i/2023/11/02/2.png)  
   > Points to note:  
   >> 1. All animation end states (position, rotation, size) need to be the same as static_state, otherwise it will cause the model to be misaligned after the animation is played.  
   >> 2. Except static_state, all the animations are created in the second frame (timeline display as 1). 

## Animation Export
- Delete all blocks and useless groups.  
   Enter edit mode and delete all model blocks. Secondly, delete all the groups that won't move the model, take P90 for example, you need to delete aug_default group and all the blocks.  
- Export animation  
   Enter animation mode and export one animation at a time. That is, in the upper left animation window, after deleting 1 animation, in the file-export-export glTF model, model named p90_static_state.gltf  
   And export all other animations in turn