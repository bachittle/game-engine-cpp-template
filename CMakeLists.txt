cmake_minimum_required(VERSION 3.10.0)

# NOTE: change your project name here. 
project(Game-Engine-Cpp-Template)

# this has to be included for conan 1.0
# i know its deprecated, but I like it better than the new one.
# TODO: check for version, and select version 2.0
include(${CMAKE_BINARY_DIR}/conan_paths.cmake)

find_package(glfw3 REQUIRED)
find_package(spdlog REQUIRED)
find_package(glm REQUIRED)


add_subdirectory(external/glad)
add_subdirectory(external/imgui)
add_subdirectory(external/stb)

add_executable(example example.cpp)
target_link_libraries(example glfw imgui)