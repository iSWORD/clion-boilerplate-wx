cmake_minimum_required(VERSION 2.8.4)
project(ProjectName)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11")

set(SOURCE_FILES main.cpp)
add_executable(BinaryName ${SOURCE_FILES})

# wxWidgets
find_package(wxWidgets REQUIRED COMPONENTS core base)
include("${wxWidgets_USE_FILE}")
target_link_libraries(BinaryName ${wxWidgets_LIBRARIES})