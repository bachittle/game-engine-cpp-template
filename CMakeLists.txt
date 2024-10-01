cmake_minimum_required(VERSION 3.10.0)

# NOTE: change your project name here. 
project(Game-Engine-Cpp-Template)

# Detect Conan version
find_program(CONAN_CMD conan)
if(CONAN_CMD)
    execute_process(
        COMMAND ${CONAN_CMD} --version
        OUTPUT_VARIABLE CONAN_VERSION_OUTPUT
        OUTPUT_STRIP_TRAILING_WHITESPACE
    )
    if(CONAN_VERSION_OUTPUT MATCHES "Conan version ([0-9]+\\.[0-9]+\\.[0-9]+)")
        set(CONAN_VERSION ${CMAKE_MATCH_1})
    endif()
endif()

# Choose between Conan 1 and Conan 2
if(CONAN_VERSION VERSION_LESS "2.0.0")
    # Conan 1.x
    message(STATUS "Using Conan 1.x configuration")
    include(${CMAKE_BINARY_DIR}/conan_paths.cmake)
else()
    # Conan 2.x
    message(STATUS "Using Conan 2.x configuration")
    # Include Conan 2.x specific configuration here
    # For example:
    # include(${CMAKE_BINARY_DIR}/conan/conan_toolchain.cmake)
endif()


find_package(glfw3 REQUIRED)
find_package(spdlog REQUIRED)
find_package(glm REQUIRED)


add_subdirectory(external/glad)
add_subdirectory(external/imgui)
add_subdirectory(external/stb)

add_executable(example example.cpp)
target_link_libraries(example glfw imgui)