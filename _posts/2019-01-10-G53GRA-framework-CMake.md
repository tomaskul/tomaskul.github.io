---
layout: post
title: "Blog Entry #26 – G53GRA Framework set up"
comments: false
description: "Setting up graphics framework on Linux/CLion."
keywords: "university, uni, g53gra, graphics, linux, clion, cmake, freeglut, opengl, c++, computer science"
--- 

**[Updatetd 8/March/2019]** - Fixing `#include`'s to maintain existing compatibility when extending compatibility to GNU/Linux.

As one of my final year modules I picked G53GRA - Graphics. This module aims to teach the fundamental of 3D computer graphics with strong emphasis on practical work which is to be done using FreeGLUT implementation of OpenGL API. Upon getting ready to set up my working environment for the upcoming coursework, I noticed that all of the set up instructions were outlined for Windows/Visual Studio and MacOS/XCode, which weren't particularly useful to someone running Linux/CLion combination and when attempting to open & run the solution I encountered numerous errors.

Below I outlined the solution that got this working on my machine, however couple things worth noting:
- This is a very case-specific solution
- I'm inexperienced with CMake, so this might not be the *best* solution

## Solution
### Step 1 - Install FreeGLUT
Ensure you have the necessary [freeglut](http://freeglut.sourceforge.net/) library installed on your machine. For debian based distributions, use:
```TERMINAL
sudo apt-get install freeglut3-dev
```

### Step 2 - Import the project
Use CLion's "Import Project from Sources" option to import the project and to auto-generate the CMake file for you.

### Step 3 - Update #include's
In `Engine.h` & `Camera.h` add 

```
#elif __linux__
#include <GL/glut.h> 
```

And in `Texture.cpp`, within `#else` add:

```
#ifdef __linux__
#include <GL/gl.h>
#include <GL/glut.h>
#else
#include <OpenGL/OpenGL.h>
#include <GLUT/glut.h>
#endif
```

- ~~In `Engine.h`, `Camera.h` & `Texture.cpp` change `#include <GLUT/glut.h>` to `#include <GL/glut.h>`~~
- ~~In `Texture.cpp` change `#include <OpenGL/OpenGL.h>` to `#include <GL/gl.h>`~~

### Step 4 - Update CMakeLists.txt
Now, at this point I had numerous "'undefined reference to 'gl____'" errors, which are caused by the linker, to fix these you simply need to provide correct file paths and here is where CMake file mentioned in an earlier step comes in.

At the top of the CMake, after CMake version and project name are set add the following commands:
```CMAKE
find_package(OpenGL REQUIRED)
find_package(GLUT REQUIRED)
```

These (`find_package()`) commands will locate and load into memory the locations of the necessary libraries. Lastly, at the very end of the CMake add the following command, don't forget to replace `<project_name>` with the name of your project:

```CMAKE
target_link_libraries(<project_name> ${OPENGL_LIBRARIES} ${GLUT_LIBRARY})
```