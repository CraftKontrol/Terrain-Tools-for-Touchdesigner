# Water PBR Shader
#Version 1.001
This shader uses a height map to displace the water surface and a normal map to create the water's surface normal. 
It uses a depth map to fade the alpha based on the depth map distance, and to create foam on the water's surface using simplex noises. 
it also uses the depth map to blend between two colors based on the deepness of the water. 
As outuputs, it returns the color, the camera space normals, the normal map, and the distance to the depth map.