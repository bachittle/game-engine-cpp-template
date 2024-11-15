# Game Engine C++ Template

Minimal C++ OpenGL game engine template that gives you a window and ImGui with just a few lines of code.

## What's Included
- GLFW window setup
- Dear ImGui integration
- OpenGL context
- Conan package management
- Example showing window creation and ImGui demo

## Quick Start
Using PowerShell:
```powershell
mkdir build
cd build
conan install .. -s build_type=Release --build missing
cmake ..
cmake --build . --config Release

# Run the example
.\Release\example.exe
```

You can also use the VSCode CMake extension to configure and build the project. Make sure to select the Release configuration for optimal performance.

## Documentation
- `docs/design_philosophy.md` - Learn about the template's minimalist approach and design decisions
- `docs/build.md` - Advanced build configurations (Ninja, Conan versions, IDE setup, etc.)