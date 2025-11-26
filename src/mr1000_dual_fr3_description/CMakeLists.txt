cmake_minimum_required(VERSION 2.8.3)
project(mr1000_dual_fr3_description)

find_package(catkin REQUIRED)

catkin_package()

install(
  DIRECTORY launch meshes urdf
  DESTINATION share/${PROJECT_NAME}
)

