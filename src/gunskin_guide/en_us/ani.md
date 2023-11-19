# Animation tutorials
## Animation
1. Import model  
   Open Blockbench, create a **Generic Model**, import the gun and hand model.  
   ! [Image](https://s1.3hov.com/lesraisins/i/2023/11/02/1.png)  
   > Import the gun and hand models:  
   >> 1. The hand model T is the purlicue(the space between the forefinger and thumb), L is the left hand;  
   >> 2. The muzzle of the gun is facing north;  
   >> 3. Folder outline path:  
   >>> All the immovable parts of the gun are divided into a group, and all the movable parts are divided into a group separately, such as aug animation process needs to move the magazine and pull handle, then create aug_magazine and aug_charge group separately.  
   >>> The **Pivot Point** of RightHand Lefthand must be 8 8 8, in order to facilitate the editing, it will be set into L R group, and the animation editing will be executed on these two groups after that.
   >> 4. Size: two-handed weapon arm parent (L, R) scaled to 1 1.5 1, pistol-like arm parent scaled to 1.75 2 1.75
2. Animation  
   The animation includes 1. holding the gun: static_state; 2. pulling out the gun: draw; 3. inspecting: inspect; 4. changing the bullet: reload_norm; 5. changing the bullet empty: reload_empty  ;6. fire: fire
   ! [Image](https://s1.3hov.com/lesraisins/i/2023/11/02/2.png)  
   > Points to note:  
   >> 1. All animation end states (position, rotation, size) need to be the same as static_state, otherwise it will cause the model to be misaligned after the animation is played.  
   >> 2. Except static_state, all the animations are created in the second frame (timeline display as 1). 
## Animation Export
1. Delete all blocks and useless groups.  
   Enter edit mode and delete all model blocks. Secondly, delete all the groups that won't move the model, take P90 for example, you need to delete aug_default group and all the blocks.  
2. Export animation  
   Enter animation mode and export one animation at a time. That is, in the upper left animation window, after deleting 1 animation, in the file-export-export glTF model, model named p90_static_state.gltf  
   And export all other animations in turn