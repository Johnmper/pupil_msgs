cmake_minimum_required(VERSION 3.1)
project(pupil_msgs)

## Find catkin macros and libraries
## if COMPONENTS list like find_package(catkin REQUIRED COMPONENTS xyz)
## is used, also find other catkin packages
find_package(catkin REQUIRED COMPONENTS
  std_msgs
  sensor_msgs
  message_generation
)

add_message_files(FILES point2d.msg point3d.msg ellipse2d.msg circle3d.msg sphere3d.msg stamped_point3d_array.msg pupil_datum.msg gaze_datum.msg frame.msg eye_status.msg)

generate_messages(DEPENDENCIES std_msgs sensor_msgs)

catkin_package(
  CATKIN_DEPENDS std_msgs sensor_msgs message_runtime
)
