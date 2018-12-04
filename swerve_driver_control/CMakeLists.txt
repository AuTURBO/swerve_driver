cmake_minimum_required(VERSION 2.8.3)
project(swerve_driver_control)


find_package(catkin REQUIRED COMPONENTS
  gazebo_ros
  swerve_driver_description
  geometry_msgs
  roscpp
  std_msgs
  tf
)

catkin_package(
  INCLUDE_DIRS include
  LIBRARIES swerve_driver_control
  CATKIN_DEPENDS gazebo_ros geometry_msgs roscpp std_msgs tf swerve_driver_description
  DEPENDS system_lib
)

###########
## Build ##
###########

## Specify additional locations of header files
## Your package locations should be listed before other locations
include_directories(
# include
  ${catkin_INCLUDE_DIRS}
)

add_executable(swerve_driver_control src/test.cpp)
target_link_libraries(swerve_driver_control ${catkin_LIBRARIES})
add_dependencies(swerve_driver_control test.cpp)
