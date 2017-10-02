cmake_minimum_required(VERSION 3.8)
project(project_1)

set(CMAKE_CXX_STANDARD 11)

set(SOURCE_FILES
        lisod.c)

add_executable(project_1 ${SOURCE_FILES})