cmake_minimum_required(VERSION 2.8.3)
project(aisaac)

find_package(catkin REQUIRED COMPONENTS
  geometry_msgs
  roscpp
  rospy
  sensor_msgs
  consai_msgs
  std_msgs
  message_generation 
)



add_service_files(
  FILES
  pid.srv
  Kick.srv
)

add_message_files(
  FILES
  Status.msg
)

generate_messages(
DEPENDENCIES
 std_msgs)




catkin_package(
CATKIN_DEPENDS roscpp rospy std_msgs message_runtime)

include_directories(
  ${catkin_INCLUDE_DIRS}
)
