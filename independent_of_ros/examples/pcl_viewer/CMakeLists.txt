cmake_minimum_required(VERSION 2.6 FATAL_ERROR)

project(pclViewer)

find_package(PCL 1.2 REQUIRED)

include_directories(${PCL_INCLUDE_DIRS})
link_directories(${PCL_LIBRARY_DIRS})
add_definitions(${PCL_DEFINITIONS})

add_executable (pclViewer src/pclViewer.cpp)
target_link_libraries (pclViewer ${PCL_LIBRARIES})