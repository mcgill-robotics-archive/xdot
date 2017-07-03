cmake_minimum_required(VERSION 2.8.3)
project(xdot)

# Load catkin and all dependencies required for this package
find_package(catkin REQUIRED)

catkin_package()

catkin_python_setup()

catkin_install_python(
  PROGRAMS
    scripts/dot_viewer.py
    src/xdot/${PROJECT_NAME}_qt.py
    src/xdot/${PROJECT_NAME}.py
  DESTINATION
    ${CATKIN_PACKAGE_BIN_DESTINATION}
)

