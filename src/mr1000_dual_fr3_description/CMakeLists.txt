cmake_minimum_required(VERSION 3.8)
project(mr1000_dual_fr3_description)

if(CMAKE_COMPILER_IS_GNUCXX OR CMAKE_CXX_COMPILER_ID MATCHES "Clang")
  add_compile_options(-Wall -Wextra -Wpedantic)
endif()

find_package(ament_cmake REQUIRED)

# 安装 meshes 和 urdf 文件夹到共享目录，这样 ROS 2 才能找到模型
install(DIRECTORY
  meshes
  urdf
  DESTINATION share/${PROJECT_NAME}
)

ament_package()