cmake_minimum_required(VERSION 3.22)
project(vex-glad)

set(CMAKE_CXX_STANDARD 17)

include_directories(glad/include/)

file(GLOB_RECURSE CPP_SOURCE_FILES ${CMAKE_CURRENT_SOURCE_DIR}/glad/src/*.c ${CMAKE_CURRENT_SOURCE_DIR}/glad/include/*.h)

add_library(glad ${CPP_SOURCE_FILES})

add_definitions(-fPIE)

