cmake_minimum_required(VERSION 3.10)

# set the project name
project(IMVIS)

find_package( OpenCV REQUIRED )
include_directories( ${OpenCV_INCLUDE_DIRS} )

set (CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CMAKE_SOURCE_DIR}/bin)

# add the executable
add_executable(IMVIS 
  code/h-nse-imvis.cpp
  code/Histogram.cpp
  code/Mirror.cpp)

target_link_libraries( IMVIS ${OpenCV_LIBS} )
