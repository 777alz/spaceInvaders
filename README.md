# space.exe 🛸

space invaders demake written in c++ with opengl and glfw. based on the excellent [tutorial](https://nicktasios.nl/posts/space-invaders-from-scratch-part-1.html) by Nick Tasios.


## what's in the box 📦

```
spaceInvaders/
├── include/        # headers (GL/, GLFW/, KHR/) - all the good stuff
├── lib/            # static libs (glew32.lib, glew32s.lib, libglfw3dll.a)
├── src/            # source code (main.cpp) + runtime dlls
├── .vscode/        # vs code config (tasks.json, c_cpp_properties.json)
├── glew32.dll      # runtime dependency 1
├── glfw3.dll       # runtime dependency 2
├── space.exe       # the final boss (appears after build)
└── README.md       # you are here
```

## build instructions 🛠

### prerequisites
- g++ compiler with c++11 support
- vs code with c++ extension (recommended but not mandatory)
- windows (sorry linux users)
- support for openGL 3.3+

### vs code build (easy mode)
1. open folder in vs code
2. hit `ctrl+shift+b`to build
3. run `space.exe`

### manual build
```sh
g++ -g -std=c++11 -Iinclude -Llib src/*.cpp -lglfw3dll -lopengl32 -lglew32 -o space.exe
```

## controls 🎮
- `←` `→` : move (left/right, obviously)
- `space` : pew pew
- `esc` : quit (easier than alt+f4)

## notes 📝
- sprites are literally just byte arrays in the code
- framerate independent? we don't do that here