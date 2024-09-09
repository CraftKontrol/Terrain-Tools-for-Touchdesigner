# Tree GLSL Shader
# Version 1.004
This shader is used to deform a tree with a bending effect and noisy leafs deformations. 
it assumes that the tree is UV unwrapped in a way that the right part of the tree is the leafs part and the left part is the trunk part. 
it needs a second UV set to deform the tree with a gradient on the y axis. it render a tree with a bark texture and a leaf texture. 
its based on the PBR shader from TouchDesigner. 
just modified the ambient lighting part to avoid ambient on shadows. 
and added a fake transluency on backface culling.