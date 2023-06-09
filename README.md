
# TLabVihiclePhysics
An open source wheel collider sample project  
More controllable and more natural cornering drift than Unity built-in WheelCollider  
Support for course mods using AssetBundles  
Supports URP only

[You can play the demo here](https://tlab.itch.io/tlabvihiclephysics-mod)
## Screenshot
![output](https://github.com/TLabAltoh/TLabVihiclePhysics/assets/121733943/27fbf2d4-aa59-4005-a771-081d57d9f71d)
![output_1](https://github.com/TLabAltoh/TLabVihiclePhysics/assets/121733943/45939db4-7e75-4e38-a9ed-1a1602e8113d)

## Getting Started
### Prerequisites
- Unity 2022.3.3f1
- UniversalRenderingPipeline
- ProBuilder
- [TLabVKeyborad](https://github.com/TLabAltoh/TLabVKeyborad)
- node (v16.15.0)
### Installing
Clone the repository to any directory with the following command  
```
git clone https://github.com/TLabAltoh/TLabVihiclePhysics.git
```
Execute the following commands in the cloned project (install necessary submodules)

```
git submodule init
git submodule update
```

### WheelColiderSource
#### Check it works
- After opening the cloned project, create any scene and add the collider attached ground and ```Assets/TLab/TLabVihiclePhysics/Resource/TLabCarRoot.prefab```. You can check the operation of WheelCollider by executing
#### How to play
##### Car Operation
- Left / Right Arrow: Handle
- Up Arrow: Accelerator
- Down Arrow: Brake
- Q: Shift Up
- E: Shift Down
- C: Clutch
##### Camera Operation
- ASDW: Camera Rotation
- Z: Switch Camera (FPS / TPS)

#### Build
- Uncheck ```Strip Engine Code``` from Project Settings when building.Since this is a mechanism to remove unnecessary code at build time, it may cause unintended behavior in downloaded AssetBundles

### Mod
AssetBundles can be used to import your own mods built as scenes. Since we are developing with the goal of modding with WebGL, the only way to download AssetBundle is from a web server
#### Build Asset Bundle
1. Name the scene you want to build as an AssetBundle from the inspector as AssetBundle (Create only one named AssetBundle per project)
2. execute Assets/Build AssetBundle {target platform} from the menu item to build the AssetBundle. The built AssetBundle is placed in ```AssetBundle/{target platform}
#### CreateServer
1. Place any AssetBundle in ```AssetBundle/Server/```
2. Start WebServer with ```npm start```
#### PlayMod
After starting the server, play ```Assets/GCC/BuiltIn/Scenes/Title.unity``` and go to ```https://localhost:5000/{Your own pass}/{asset bundle name}.assetbundl``` to get the mod

## Reference
- https://github.com/JustInvoke/Randomation-Vehicle-Physics
- https://github.com/unity-car-tutorials/Unity5-WheelColliderSource

