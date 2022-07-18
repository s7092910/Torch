# Torch

Torch is a 7 Days to Die mod which works to optimize one of the game's most inefficient areas -- the lighting engine. It is designed to improve frame rates and in situtations where there are many lights in an area in game, it does so without compromising on how the game looks.

## Installation Guide

Torch is a client only mod. All that is needed is to download the Mod and simply drop the mod into your Mods folder where 7 Days to Die is installed. Then launch the game with Easy Anti Cheat disabled. Check to see if Occlusion is on in the main menu Video Settings, if it is off, turn it on. No other work is required in order to take advanatage of the mod.

Not sure if you installed the mod correctly? Try checking the console in game by pressing F1 and scroll up to the part where the mods are loading. If the mod is installed correctly, these following lines should be shown.

```Text
[MODS] Trying to load from folder: Torch
[MODS] Found ModAPI in Torch.dll, creating instance
[MODS] Loaded Mod: Torch (mod version)

[Torch] Loading Patch
[Torch] [LightOcclusionManager] Light Occlusion: Awake
[Torch] Loaded Patch
```

## Compatibility

Torch uses the built in Occlusion Culling System in 7 Days to Die. As such, a GPU that supports DirectX 11.0 or OpenGL 4.3 is required, which covers most graphics cards released after 2010. If you have one of the following GPUs you likely do have a GPU that will support Torch

* INTEL HD Graphics 2500/4000 (Ivy Bridge) or newer
* NVIDIA GeForce 400 Series (Fermi) or newer
* AMD Radeon HD 5000 Series (TeraScale 2) or newer

If you encounter issues with Torch, make sure that your graphics drivers are up to date.

If your GPU doesn't support some features required by Torch, an error message will appear in the console in game. You will see one of two error messages.

```Text
[Torch] [LightOcclusionManager] Light Occlusion: GPU doesn't supports Async GPU Readback
[Torch] [LightOcclusionManager] Light Occlusion: GPU doesn't supports Compute Shaders
```

## Technical details

Of course, it isn't possible to say that the game is magically faster without providing some kinda of explanation. This section will cover some of the changes and additons that are responsible for performance improvements. Not all changes and additions will be listed.

* With Unity's built in render pipeline, if the camera is facing a direction, it will create shadow maps and do other related rendering for any lights within the Camera's frustum even if the light source is behind a wall and any part of the light's bounding volume is not visible to the camera. This process can be fairly intenstive while haven't no affect on the final frame. Torch does a check to see if the light's bounding volume is visible and culls the light if it's bounding volume is not visible early on in the rendering process. 

## Contact
There is a hosted channel in Guppy's Unofficial 7DtD Modding Server Discord. The channel is `#laydors-toolshed`

* [Guppy's Unofficial 7DtD Modding Server Discord](https://discord.gg/mQpvj95rvW)
