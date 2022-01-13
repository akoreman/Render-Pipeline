**WORK IN PROGRESS**
# Custom shader pipeline using Unity3D SRP and HLSL

In order to gain more intuition for Unity3D's render pipelines I implemented a custom render
pipeline in Unity3D by using its scriptable render pipeline and HLSL for the shaders. For some parts following the
tutorial by CatLikeCoding.

Currently supports:
- Unlit and Lit shaders
  - Opaque and transparant
  - Texture sampling
- Illumination by multiple colored directional lights
  - BRDF controlled by metallic and smoothness parameters
  - Casted shadows using shadow maps
    - Support for cascaded shadow maps
    - Support for varying shadow map resolution
    - Clipped shadows for transparent objects
  - Support for soft shadows using percentage closer filtering
  - Support for normal maps
- Global illumination
  - Support for sampling from the lightmaps generated by Unity for static objects
  - Support for using light probes and LPPVs to approximate GI for dynamic objects
  - Meta pass for colored GI
 
 To do:
 - Support for spot lights + shadows
 - Support for point lights + shadows
 - Support for emmisive surfaces
 - Support for baked shadows
 - Support for reflections
 - Support for light cookies
 
 ## Screenshots:  
 
<img src="https://raw.github.com/tkoreman/WIP-ShaderDemo/master/images/sampleRender.PNG" width="400">  

**Cascaded shadow maps**   

<img src="https://raw.github.com/tkoreman/WIP-ShaderDemo/master/images/CascShadowMaps.PNG" width="400">  

**Cascaded shadow maps culling spheres visualisation**  

<img src="https://raw.github.com/tkoreman/WIP-ShaderDemo/master/images/CascCullingSpheres.PNG" width="400"> 

**Effect of varying shadow map sizes on shadow details**  

<img src="https://raw.github.com/tkoreman/WIP-ShaderDemo/master/images/shadowLevels.png" width="400">  

**Colored global illumination**
  
