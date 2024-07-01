cmake_minimum_required(VERSION 3.5)

# Set the path to the compiler
set(CMAKE_C_COMPILER "D:/Environment/mingw64/bin/gcc.exe")
set(CMAKE_CXX_COMPILER "D:/Environment/mingw64/bin/g++.exe")

project(learnopengl)

# 依赖环境
# ------------------------------------------------------------------------------
set(CMAKE_MODULE_PATH ${CMAKE_MODULE_PATH} "${CMAKE_SOURCE_DIR}/cmake/modules/")
add_library(glad include/glad.c)
add_library(stb_image include/stb_image_wrap.cpp)
find_package(GLFW3 REQUIRED)
# find_package(ASSIMP REQUIRED)
# find_package(FREETYPE2 REQUIRED)
include_directories(${GLFW3_INCLUDE_DIR})
# include_directories(${ASSIMP_INCLUDE_DIR})
# include_directories(${FREETYPE2_INCLUDE_DIR})
# ------------------------------------------------------------------------------

include_directories(./include)

# 子目录cd 
add_subdirectory(src/start)
# add_subdirectory(src/lighting)
# add_subdirectory(src/model)
# add_subdirectory(src/advance)
# add_subdirectory(src/breakout)

# add_subdirectory(test)
