cmake_minimum_required(VERSION 2.8.3)
project(simple_trajectory)

## Compile as C++11, supported in ROS Kinetic and newer
add_compile_options(-std=c++11)

 
find_package(catkin REQUIRED COMPONENTS
  roscpp
  actionlib
)
 
include_directories(
  include
  ${catkin_INCLUDE_DIRS}
)

add_executable(simple_trajectory src/main.cpp)
target_link_libraries (simple_trajectory ${catkin_LIBRARIES})

 
