cmake_minimum_required( VERSION 2.8 )
project(useSLAM)
#add_executable(use_eigen useGeometry.cpp)

add_executable(helloSLAM helloSLAM.cpp)

add_library(hello libHelloSLAM.cpp)
add_library(hello_shared SHARED libHelloSLAM.cpp)

target_link_libraries(helloSLAM hello_shared)