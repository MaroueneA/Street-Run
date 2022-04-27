# How to build

First, we initialize the SDL video system with SDL_Init().
Next, we set the title for our application window.
Then we create the window and get a pointer to the surface with SDL_SetVideoMode().
The background image is loaded on to a temporary surface.
SDL_DisplayFormat() creates a copy of the temporary surface using the same bit-depth as the screen surface. This will speed up rendering.
The memory for the temporary surface is freed with a call to SDL_FreeSurface().
Now we enter the "main loop" of the program. Here we check for events and then update the screen.
When the user presses ESC or 'q', we end the "main loop"
Before the program ends we free the memory for the background surface with SDL_FreeSurface, and cleanup SDL with SDL_Quit().


In Visual C++ you'll need to follow these steps:

Create a new empty Windows Application Project.
Add the "sdltest.cpp" file to your project.
On the menu click Project, then Properties.
Double-click "Configuration Properties".
Double-click "C/C++".
Click "Code Generation".
Change "Runtime Library" to "Multi-threaded DLL".
Double-click "Linker".
Click "Input".
Beside "Additional Dependencies", type "sdl.lib sdlmain.lib".
