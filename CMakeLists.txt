cmake_minimum_required (VERSION 2.8)
project (MyProgram)

#version number
set (MyProgram_VERSION_MAJOR 1)
set (MyProgram_VERSION_MINOR 0)

#include the subdirectory containing our libs
add_subdirectory (Project)
include_directories(Project)
#indicate the entry point for the executable
add_executable (MyProgram Project main.cpp)

# Indicate which libraries to include during the link process.
target_link_libraries (MyProgram Project)

install (TARGETS MyProgram DESTINATION bin)
