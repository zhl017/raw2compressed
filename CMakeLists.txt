cmake_minimum_required(VERSION 3.0.2)
project(raw2compressed)

find_package(catkin REQUIRED COMPONENTS)

catkin_python_setup()

catkin_package(CATKIN_DEPENDS)

catkin_install_python(PROGRAMS
  nodes/raw2compressed
  DESTINATION $(CATKIN_PACKAGE_BIN_DESTINATION)
)

install(DIRECTORY launch
  DESTINATION $(CATKIN_PACKAGE_SHARE_DESTINATION)
)