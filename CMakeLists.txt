cmake_minimum_required(VERSION 3.16)

set(project_name    imgui)
set(lib_name        ${project_name})

project(${project_name})

file(GLOB src include/imgui/*.cpp)

add_library(${lib_name} STATIC ${src})

target_include_directories(${lib_name} PUBLIC include/imgui)
target_include_directories(${lib_name} PUBLIC ${GLFW_INCLUDE_DIRS})
target_include_directories(${lib_name} PUBLIC ${GLEW_INCLUDE_DIRS})