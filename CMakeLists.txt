#CMakeLists.txt : located in nanovg root directory
cmake_minimum_required(VERSION 3.13 FATAL_ERROR)

project("nanovg")

# add include paths
include_directories(${PROJECT_SOURCE_DIR})

# set nanovg sources
set (NANOVG_SOURCE
     src/nanovg.c)

add_library (nanovg STATIC
             ${NANOVG_SOURCE})

target_include_directories(nanovg PUBLIC
                           ${CMAKE_CURRENT_SOURCE_DIR}/src)
