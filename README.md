![Glotch image](https://github.com/CraftKontrol/Terrain-Tools-for-Touchdesigner/blob/main/TerrainExample/TerrainToolsExample.jpg?raw=true)
# Terrain Tools for Touchdesigner 
Terrain Tools is a set of externals for touchdesigner designed to help create environments.
All based on game engines techniques, this set of tools is designed to be used in real-time applications.
It use as input a height map and a splat map to blend between different textures.
It uses also the height map to instance trees and grass on the terrain.
It uses a LOD system to optimize the rendering of the scene.
There is also a volumetric fog system, a lens flare system, 
and a boids system to animate birds or fishes.

## Content
1. Terrain shader
2. Water shader
3. Tree shader
4. Grass shader
5. PBR shader
6. LOD instancer
7. Animated boids system
8. Volumetric fog
9. Lens flare shader
10. Terrain Example Scene                   


### TODO
Some transparency artifacts on grass and tree shaders to fix.


## 1. Terrain shader
This shader use a height map to displace the terrain and a splat map to blend between different textures.
it blends the color, normal and roughness of the textures using the 3 channels of the splat map.
Normal mappping blending is done using the PartialNormalDerivatives function or OverlayNormals function.
This shader is based on the PBR shader from TouchDesigner.
just modified the ambient lighting part to avoid ambient on shadows.

## 2. Water shader
This shader uses a height map to displace the water surface and a normal map to create the water's surface normal. 
It uses a depth map to fade the alpha based on the depth map distance, and to create foam on the water's surface using simplex noises.
it also uses the depth map to blend between two colors based on the deepness of the water.
As outuputs, it returns the color, the camera space normals, the normal map, and the distance to the depth map.

## 3. Tree shader
This shader is used to deform a tree with a bending effect and noisy leafs deformations.
it assumes that the tree is UV unwrapped in a way that the right part of the tree is the leafs part and the left part is the trunk part.
it needs a second UV set to deform the tree with a gradient on the y axis.
it render a tree with a bark texture and a leaf texture.
its based on the PBR shader from TouchDesigner.
just modified the ambient lighting part to avoid ambient on shadows. 
and added a fake transluency on backface culling.

## 4. Grass shader
This shader is used to deform a grass with a bending effect.
it render a grass with fake transluency.
It fades the grass with a fresnel effect when side facing the camera.
its based on the PBR shader from TouchDesigner.
just modified the ambient lighting part to avoid ambient on shadows

## 5. PBR shader
its based on the PBR shader from TouchDesigner.
just modified the ambient lighting part to avoid ambient on shadows.

## 6. LOD instancer
It Generate instances position from a heightmap and a distribution map.
It uses a LOD system to optimize the rendering, and a cone view frustum to cull the instances that are not in the camera view.

## 7. Animated boids system
This one is originally by David Braun
https://github.com/DBraun/TouchDesigner_Shared/tree/master/Starters/boids

Modified the shader to include multiples Targets and Ennemies to the boid system.
Modified the input geometry to parse an alembic file.
Added an animation factor using velocity to speed up or slow down the animation.
Modified the material to be PBR.

## 8. Volumetric fog
This one is originally by Tim Gerritsen
https://forum.derivative.ca/t/volumetric-fog-shader/9823

Just removed multiple light based positions and colors to simplify the shader. I added a fade factor to the fog to make it fade out a different color at a certain distance.

## 9. Lens flare shader
A Combination of GLSL and TD operators that use screen space postions to create a lens flare effect. it also use the depth map to fade the lens on obstructed areas.

## 10. Terrain Example Scene
An example scene to show how to use the terrain tools.


##	Installation process
Just drag and drop TOXs on your scene. 
See the example scene for more details.

##	Software dependencies
Touchdesigner 2022.11880
