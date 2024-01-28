cmake_minimum_required(VERSION 3.27)
project(clion-demo)

set(CMAKE_CXX_STANDARD 17)

add_executable(clion-demo main.cpp)
add_executable(test-cmake day00/test-cmake.cpp)
add_executable(test-tgaimage day00/test-tgaimage.cpp)
add_executable(test-tgaimage-01 day01/test-tgaimage-01.cpp)
add_executable(test-draw-head day01/test-draw-head.cpp)

add_library(tgaimagelib day00/tgaimage.cpp)
target_link_libraries(test-tgaimage tgaimagelib)

target_link_libraries(test-tgaimage-01 tgaimagelib)

configure_file(day01/african_head.obj african_head.obj COPYONLY)
add_library(tgamodellib day01/model.cpp)
target_link_libraries(test-draw-head tgaimagelib)
target_link_libraries(test-draw-head tgamodellib)
