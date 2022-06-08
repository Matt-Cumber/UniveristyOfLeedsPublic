# University of Leeds Coursework Demos

Due to plagiarism concerns, instead of uploading pure code, find some demos of courseworks here.

## Group Project - Game Engine
I have been developing a C++, OpenGl, GLSL game engine as part of a group project module in my final year of my masters degree in Computer Science with High Performance Games Engineering. A more in depth video of the engine will be available soon which will include features added by my team members. However, the repository is public and the code can be found at https://github.com/kablouser/PlatinumEngine. 

Here I will demo the particle system which I implemented. To implement this feature, I had to write a new shader in GLSL and a renderer which makes use of instancing in OpenGl. I use a texture atlas to texture particles and can index into the atlas using different parameters. 

### Particle Effect No Texture - Pixel Fire

https://user-images.githubusercontent.com/46685490/167919133-dd6af308-eacb-4e9f-9811-62e649888f6f.mov

### Particle Effect With Texture Atlas - Explosion

https://user-images.githubusercontent.com/46685490/167919159-d2dd953c-d150-4a56-9103-d2c47d74a8bd.mov

### Normal Mapping
The objects on the left use a default phong shader where the normal is the normal of the plane. The objects on the right (separated using the bin object) are using a normal texture to sample a normal instead of one normal for the whole plane. This allows lighting to take into consideration the texture of the object, resulting in more depth to the images.

https://user-images.githubusercontent.com/46685490/168167300-22c6274c-7439-432e-bb9c-6e78074325c0.mp4

## High Performance Graphics - Vulkan Application with Bloom Post Processing

The application I wrote was built in 3 stages over 3 courseworks submitted to the University of Leeds and was written in C++ and runs on Windows. The first coursework involved rendering obj files with a mtl file which contained both colours and textures. Next, the second coursework expanded on this by implenenting two lighting models: Blinn Phong and a PBR model. In the final coursework I decided to implement two post processing effects: Pixelation and Bloom. The bloom I implemented is a simple gaussian blur which uses the 1D formula from https://en.wikipedia.org/wiki/Gaussian_blur. I also make use of linear filtering to reduce the number of taps required to blur the image based on the explanation from the blog post here https://www.rastergrid.com/blog/2010/09/efficient-gaussian-blur-with-linear-sampling/. The weights and offsets are calculated once on the CPU when required and sent to the GPU for rendering, rather than computing the blur in the shader itself.

Here are some results from the bloom post processing effect:

Using a threshold of 1.0 to extract bright lights, blurring the thresholded image 1 time, using sigma as 9 and a kernel footprint size of 22 for blurring, the below image is produced.

![image](https://user-images.githubusercontent.com/46685490/172678910-37a3e890-5b98-476e-82ec-298af83b4ce1.png)

Using the same settings as above but blurring the image 10 times results in this image.

![image](https://user-images.githubusercontent.com/46685490/172680370-a57600f2-0f83-4be2-8398-afb27e3326bd.png)

## Animation and Simulation - Cloth Simulator 
Using a mass-spring model, a simple cloth can simulated using some basic equations. Code was written in C++. *Note cloth self intersections were not dealt with*. 

### A cloth fixed at two corners with wind blowing

https://user-images.githubusercontent.com/46685490/168165014-2ed102b3-2289-44bf-90dc-57e7788335fd.mp4

## A cloth falling onto a ball on the ground

https://user-images.githubusercontent.com/46685490/168166456-435e1a1a-6356-449b-9810-3ab7c9dd6b15.mp4

### A cloth falling onto a spinning ball

https://user-images.githubusercontent.com/46685490/168165030-2e2e2f60-6290-4497-96bd-f24a30bc8afc.mp4

## Animation and Simulation - 2D Fluid Simulation

https://user-images.githubusercontent.com/46685490/168178564-949b93b5-dd7b-452f-92b9-1726eeade167.mp4

## Geometric Processing - Loop Subdivision
Each triangle of the mesh is split into 4 triangles on each sub divide call. Code was written in C++

https://user-images.githubusercontent.com/46685490/168170557-9e387b15-240d-4d93-af16-34d296da09b9.mp4
