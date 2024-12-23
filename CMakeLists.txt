cmake_minimum_required(VERSION 3.16)
project(tutorial VERSION 0.0.1)

set(SOURCES main.cpp)

set(CMAKE_BUILD_TYPE Debug)
set(CMAKE_CXX_STANDARD 20)

find_package(glfw3 3.4 REQUIRED)
find_package(OpenGL REQUIRED)
find_package(GLEW REQUIRED)
add_executable(tutorial ${SOURCES})
include_directories(${GLEW_INCLUDE_DIRS})
target_link_libraries(tutorial glfw)
target_link_libraries(tutorial OpenGL::GL)
target_link_libraries(tutorial ${GLEW_LIBRARIES})

