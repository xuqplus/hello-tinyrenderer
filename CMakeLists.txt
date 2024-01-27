cmake_minimum_required(VERSION 3.27)
project(clion-demo)

set(CMAKE_CXX_STANDARD 17)

add_executable(clion-demo main.cpp)
add_executable(test-cmake day00/test-cmake.cpp)
add_executable(test-tgaimage day00/test-tgaimage.cpp)

add_library(tagimagelib day00/tgaimage.cpp)
target_link_libraries(test-tgaimage tagimagelib)
