# mixamo-blender-babylon
Tutorial

From [Mixamo](www.mixamo.com), under Characters, select Y Bot. Download Y Bot with the following settings:
<img src="/img/1.png" alt="alt text" width="400px">  
Rename this file to ybot.fbx

In Mixamo, under Animations, I chose a punch and kick. Download animations with the following settings:
<img src="/img/2.png" alt="alt text" width="400px">  
Rename these files to ybot@animation.fbx, e.g. ybot@punch.fbx and ybot@kick.fbx.

Open a new Blender 2.8 scene, and delete all 3 default objects (cube, camera, and light).

In Blender top menu, click File → Import → FBX (.fbx). In Operator Presets on the right, check Manual Orientation and Automatic Bone Orientation. Select ybot.fbx and then click Import FBX.
<img src="/img/3.png" alt="alt text" width="400px">  

Import ybot@punch.fbx and ybot@kick.fbx into Blender the same way you did ybot.fbx.
<img src="/img/4.png" alt="alt text" width="400px">  

Rename Armature to Character, and rename all animations, as shown in the image below (bordered red):
<img src="/img/5.png" alt="alt text" width="400px">  

Delete Armature.001 and Armature.002.

As shown in the image below (bordered red), select Character (top right), click in the center of the circle (bottom right) and drag up to create a new sub-window. Select Dope Sheet (bottom left) and Action Editor (next to it), and select an animation (middle). Click play (bottom middle) to play animation. If your character is not animating, maybe you didn't select Character (top right bordered in red).
<img src="/img/6.png" alt="alt text" width="400px">  
