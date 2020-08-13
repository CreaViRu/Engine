cmake_minimum_required(VERSION 3.17 FATAL_ERROR)

project(Engine VERSION 0.1.0)

#SOURCE
add_executable(${CMAKE_PROJECT_NAME} src/main.cpp)

#GLFW
set(GLFW_BUILD_DOCS OFF CACHE BOOL "" FORCE)
set(GLFW_BUILD_TESTS OFF CACHE BOOL "" FORCE)
set(GLFW_BUILD_EXAMPLES OFF CACHE BOOL "" FORCE)
set(GLFW_INSTALL OFF CACHE BOOL "" FORCE)
add_subdirectory(external/glfw)
target_link_libraries(${CMAKE_PROJECT_NAME} glfw)