cmake_minimum_required(VERSION 3.10)

# set the project name
project(cpluspalette VERSION 1.0)



set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED True)

add_executable(cpluspalette src/main.cpp src/colors.cpp src/kmean.cpp)

find_package(X11 REQUIRED)
include_directories(${X11_INCLUDE_DIR})
target_link_libraries(cpluspalette ${X11_LIBRARIES})


install(TARGETS cpluspalette )
