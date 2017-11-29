cmake_minimum_required(VERSION 3.3)
project(FlowGraph)

list(APPEND CMAKE_MODULE_PATH "/Users/Stepan/Desktop/FindTBB-master")

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11")

find_package(tbb REQUIRED)

set(SOURCE_FILES main.cpp)
add_executable(FlowGraph ${SOURCE_FILES})
target_link_libraries(FlowGraph tbb)