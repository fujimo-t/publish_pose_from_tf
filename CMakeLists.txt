cmake_minimum_required(VERSION 2.8.3)
project(publish_pose_from_tf)

find_package(catkin REQUIRED)
catkin_package()

catkin_install_python(
  PROGRAMS nodes/publish_pose_from_tf
  DESTINATION ${CATKIN_PACKAGE_BIN_DESTINATION}
)
