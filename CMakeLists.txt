
cmake_minimum_required(VERSION 2.8)
add_compile_options(-std=c++11)
PROJECT(Graphs)

find_package(VTK REQUIRED)
include(${VTK_USE_FILE})

add_executable(Graphs main.cpp)

if(VTK_LIBRARIES)
  target_link_libraries(Graphs ${VTK_LIBRARIES})
else()
  target_link_libraries(Graphs vtkHybrid vtkWidgets)
endif()
