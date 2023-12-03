cmake_minimum_required(VERSION 3.8)
project(avatar_visualizer)

if(CMAKE_COMPILER_IS_GNUCXX OR CMAKE_CXX_COMPILER_ID MATCHES "Clang")
  add_compile_options(-Wall -Wextra -Wpedantic)
endif()

# find dependencies
find_package(ament_cmake REQUIRED)
find_package(rclcpp REQUIRED)

install(DIRECTORY robots/
   DESTINATION ${CMAKE_INSTALL_PREFIX}/share/${PROJECT_NAME}/robots)

ament_package()
