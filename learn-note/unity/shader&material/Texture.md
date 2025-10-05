## Tiling and Offset
- Tiling is the number of tiles per unit on the surface of the mesh. A higher number makes the pattern smaller.
- Offset begins the tiling at a different point. For example, an X Offset of 0.5 offsets the tiling by half the width of the texture.
## UV mapping
Meshes made by modeling applications generate their own sets of 2D coordinates called UV coordinates. UV coordinates are like the XY coordinates in regular 2D spaces, but they are called UV to differentiate them from the coordinate system of the environment (XYZ). UV coordinates are relative to the mesh, not the 3D space in your scene.
UV mapping is the process of unwrapping the surface of a 3D model to create a flat surface, then applying a 2D texture map to it. In the process, the modeling application generates the UV coordinates that allow the texture to be wrapped back onto the model.
