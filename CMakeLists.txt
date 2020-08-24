cmake_minimum_required(VERSION 2.8 FATAL_ERROR)

project(voxel_grid)

find_package(PCL 1.2 REQUIRED)

include_directories(${PCL_INCLUDE_DIRS})
link_directories(${PCL_LIBRARY_DIRS})
add_definitions(${PCL_DEFINITIONS})

add_executable (voxel_grid voxel_grid.cpp)
add_executable (separate_object_ground separate_object_ground.cpp)
target_link_libraries (voxel_grid ${PCL_LIBRARIES})
target_link_libraries (separate_object_ground ${PCL_LIBRARIES})

