# mixamo-blender-babylon
Tutorial

From [Mixamo](www.mixamo.com), under Characters, select Y Bot. Download Y Bot with the following settings:  
<img src="/img/1.png" alt="alt text" width="500px">  
Rename this file to ybot.fbx  

In Mixamo, under Animations, I chose a punch and kick. Download animations with the following settings:  
<img src="/img/2.png" alt="alt text" width="500px">  
Rename these files to ybot@animation.fbx, e.g. ybot@punch.fbx and ybot@kick.fbx.  

Open a new Blender 2.8 scene, and delete all 3 default objects (cube, camera, and light).  

In Blender top menu, click File → Import → FBX (.fbx). In Operator Presets on the right, check Manual Orientation and Automatic Bone Orientation. Select ybot.fbx and then click Import FBX.  
<img src="/img/3.png" alt="alt text" width="500px">  

Import ybot@punch.fbx and ybot@kick.fbx into Blender the same way you did ybot.fbx.  
<img src="/img/4.png" alt="alt text" width="500px">  

Rename Armature to Character, and rename all animations, as shown in the image below (bordered red):  
<img src="/img/5.png" alt="alt text" width="500px">  

Delete Armature.001 and Armature.002.  

As shown in the image below (bordered red), select Character (top right), click in the center of the circle (bottom right) and drag up to create a new sub-window. Select Dope Sheet (bottom left) and Action Editor (next to it), and select an animation (middle), e.g. Kick. Click play (bottom middle) to play animation. If your character is not animating, maybe you didn't select Character (top right bordered in red).  
<img src="/img/6.png" alt="alt text" width="500px">  

Change animation back to TPose from Kick. In Blender, press N, which opens the Transform tab. Note that Rotation is not all 0° and Scale is all 0.010 instead of 1.  
<img src="/img/7a.png" alt="alt text" width="500px">  

As shown in the image below (bordered red), in Object Mode, press A to select all. Press S to scale. Type 100 to scale from 0.010 to 1.  
<img src="/img/8.png" alt="alt text" width="500px">  

As shown in the image below (bordered red), press Ctrl + A to apply. Click All Transforms. Location should all be set to 0, Rotation all to 0, and Scale all to 1.  
<img src="/img/9.png" alt="alt text" width="500px">  

We need to change the two materials, as shown in the image below. Something about them is incompatible with .babylon format.  
<img src="/img/10.png" alt="alt text" width="500px">  

Click Alpha_Joints_MAT. As shown in the image below (bordered red), click Material Properties (bottom most), Browse Materials (slightly above), and select Material (slightly above). Do the same for Alpha_Body_MAT.  
<img src="/img/11.png" alt="alt text" width="500px">  

In Blender top menu, click File → Export → Babylon.js ver 6.2.3. Click Export Babylon.js scene.  

Open your .babylon file in Notepad. Scroll to bottom, and paste the following text  
  
"autoAnimate": true,"autoAnimateFrom": 1,"autoAnimateTo": 152,"autoAnimateLoop": true,  
  
before "instances":[]. Save your .babylon file.  
<img src="/img/12.png" alt="alt text" width="500px">  

Go to [Babylon.js Sandbox](https://sandbox.babylonjs.com/). Drag your .babylon file into the browser.  

Click image to watch Youtube video:  
<p align="center">
  <a href="https://www.youtube.com/embed/_f4z--WKsU4" target="_blank"><img src="/img/13.png" alt="IMAGE ALT TEXT HERE" width="240" border="10" /></a>
</p>  