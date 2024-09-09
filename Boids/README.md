# Boids
# Version 1.07

Original by David Braun
https://github.com/DBraun/TouchDesigner_Shared/tree/master/Starters/boids

The shader uses a combination of rules such as separation, alignment, and cohesion
to simulate the flocking behavior of birds or fish. It also includes collision avoidance
and target seeking behaviors.

The shader takes input data for each boid, including its position, direction, flocking information,
and information about nearby targets and enemies. It uses this data to calculate the desired
acceleration for each boid, which is then used to update its position and direction.

The shader also includes utility functions for generating random numbers, manipulating vectors,
and applying forces based on distance and direction.

Modified the shader to include multiples Targets and Ennemies to the boid system. 
Modified the input geometry to parse an alembic file. 
Added an animation factor using velocity to speed up or slow down the animation. 
Modified the material to be PBR.