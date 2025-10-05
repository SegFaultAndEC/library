There are two types of maps primarily used in bump mapping: normal maps and height maps.
## types
### normal map
A normal map sets these values over an entire surface, which directs the shader to create the illusion that fragments (pixels) on the surface are facing different directions.
### height maps
Height maps indicate the relative height of each pixel from mesh.

Normal and height maps can add realistic physical details to your surfaces without using much computing power. Frequently, normal maps are used without height maps.
## Add surface details with normal maps
A normal map is similar to a base map, except that the red, green, and blue values indicate the direction of the normal relative to the mesh surface. Normal maps are mostly cyan and purple because the directions are expressed using higher values in the blue channel.
