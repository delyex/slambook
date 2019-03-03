cmake_minimum_required( VERSION 2.8 )
project( geometry )

# Add GDB support
SET( CMAKE_BUILD_TYPE "Debug" )
SET( CMAKE_CXX_FLAGS_DEBUG "$ENV{CXXFLAGS} -O0 -Wall -g2 -ggdb" )

# 添加Eigen头文件
include_directories( "/usr/include/eigen3" )

add_executable( eigenGeometry eigenGeometry.cpp )
