# Build Documentation

## Build System Essentials

This project uses:
- CMake as the build system
- Build artifacts are generated in the `build/` folder
- Conan for dependency management
  - Currently using Conan 1.x
  - Future migration to Conan 2.x planned as 1.x becomes deprecated

## Build Configurations

You can build in Debug or Release mode:

Command line:
```powershell
# Debug build
cmake --build . --config Debug

# Release build
cmake --build . --config Release
```

VSCode: Use the CMake extension's dropdown menu to switch between Debug and Release configurations. Look for the "Configure" button in the CMake extension's toolbar.

## Build Tools

By default on Windows, MSBuild is used as the build system. You can optionally use Ninja for faster builds:
- Configure via VSCode: 
  Preferences > Settings > Extensions > CMake Tools > Generator > Set to "Ninja"

## IDE Setup

### VSCode (Recommended)
VSCode provides an excellent balance between features and simplicity:
- Essential extensions: CMake Tools, C/C++
- Integrated debugging capabilities
- Git visualization
- AI code assistance
- Clean, minimal interface

Search online for "VSCode C++ setup tutorial" for detailed setup guides.

### Visual Studio
Consider Visual Studio if you need:
- Advanced performance profiling
- Complex debugging features
- Visual memory analysis

However, for most development needs, VSCode provides the perfect balance of functionality while maintaining our project's minimal approach.