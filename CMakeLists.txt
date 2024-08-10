cmake_minimum_required(VERSION 3.10)
project(lua)

include(../../../functions.cmake)

# Call the functions to collect files
collect_cpp_files("${CMAKE_CURRENT_SOURCE_DIR}")
collect_h_files("${CMAKE_CURRENT_SOURCE_DIR}")


include_directories("${CMAKE_CURRENT_SOURCE_DIR}")

# Include Conan dependencies
include_directories("${CMAKE_INCLUDE_PATH}")

link_directories(${CMAKE_LIBRARY_PATH})

add_library(${PROJECT_NAME} STATIC ${SRC_FILES} ${INCLUDE_FILES})