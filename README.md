# University of Leeds Coursework Demos

Due to plagiarism concerns, instead of uploading pure code, find some demos of courseworks here.

## Group Project - Game Engine
I have been developing a C++, OpenGl, GLSL game engine as part of a group project module in my final year of my masters degree in Computer Science with High Performance Games Engineering. A more in depth video of the engine will be availabale soon which will include features added by my team members. However, the repository is public and the code can be found at https://github.com/kablouser/PlatinumEngine. 

Here I will demo the particle system which I implemented. To implement this feature, I had to write a new shader in GLSL and a renderer which makes use of instancing in OpenGl. I use a texture atlas to texture particles and can index into the atlas using different parameters. 

### Particle Effect No Texture - Pixel Fire

https://user-images.githubusercontent.com/46685490/167919133-dd6af308-eacb-4e9f-9811-62e649888f6f.mov

### Particle Effect With Texture Atlas - Explosion

https://user-images.githubusercontent.com/46685490/167919159-d2dd953c-d150-4a56-9103-d2c47d74a8bd.mov

## Animation and Simulation - Cloth Simulator 
Using a mass-spring model, a simple cloth can simulated using some basic equations. *Note cloth self intersections were not dealt with*. 

### A cloth fixed at two corners with wind blowing

### A cloth falling onto a spinning ball rested on the floor
