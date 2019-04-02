cmake_minimum_required( VERSION 2.8 )
project( useSophus )

SET( CMAKE_BUILD_TYPE "Debug" )
SET( CMAKE_CXX_FLAGS_DEBUG "$ENV{CXXFLAGS} -O0 -Wall -g2 -ggdb" )

# 为使用 sophus，您需要使用find_package命令找到它
find_package( Sophus REQUIRED )
include_directories( ${Sophus_INCLUDE_DIRS} )
#include_directories( "/usr/local/include/sophus" )
include_directories( "/usr/include/eigen3" )

add_executable( useSophus useSophus.cpp )
target_link_libraries( useSophus ${Sophus_LIBRARIES} )
