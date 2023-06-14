cmake_minimum_required(VERSION 3.0.2)
project(hr4c_msgs)

find_package(catkin REQUIRED COMPONENTS
  rospy std_msgs geometry_msgs message_generation
)

add_service_files(
  DIRECTORY srv
  FILES
  GetInt8Array.srv
  SetInt8Array.srv
  SetInt8.srv
  SetJointTrajectory.srv
  SetPose.srv
  GetPose.srv
  SetForceMoment.srv
  GetForceMoment.srv
  GetMotorStatus.srv
  GetInterpolationStatus.srv
  SetFloat64.srv
  )

generate_messages(
  DEPENDENCIES
  std_msgs
  geometry_msgs
  )

catkin_package(
  CATKIN_DEPENDS std_msgs geometry_msgs message_runtime
)

include_directories(
  ${catkin_INCLUDE_DIRS}
)
