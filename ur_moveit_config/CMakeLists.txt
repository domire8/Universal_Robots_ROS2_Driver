cmake_minimum_required(VERSION 3.22)
project(ur_moveit_config)

find_package(ament_cmake REQUIRED)

ament_package()

install(
  DIRECTORY config launch srdf
  DESTINATION share/${PROJECT_NAME}
)

# Install executables
install(PROGRAMS
  scripts/wait_for_robot_description
  DESTINATION lib/${PROJECT_NAME}
)