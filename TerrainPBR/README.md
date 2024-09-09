# Terrain PBR Shader
# Version 1.003
This shader use a height map to displace the terrain and a splat map to blend between different textures.
it blends the color, normal and roughness of the textures using the 3 channels of the splat map.
Normal mappping blending is done using the PartialNormalDerivatives function or OverlayNormals function.

This shader is based on the PBR shader from TouchDesigner.
just modified the ambient lighting part to avoid ambient on shadows
