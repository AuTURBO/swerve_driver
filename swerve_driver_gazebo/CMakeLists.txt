cmake_minimum_required(VERSION 2.8.3)
project(swerve_driver_gazebo)

find_package(catkin REQUIRED COMPONENTS
  controller_manager
  joint_state_controller
  robot_state_publisher
)

catkin_package(
##  INCLUDE_DIRS include
##  LIBRARIES swerve_driver_gazebo
  CATKIN_DEPENDS controller_manager joint_state_controller robot_state_publisher
  DEPENDS system_lib
)

include_directories(
# include
  ${catkin_INCLUDE_DIRS}
)
