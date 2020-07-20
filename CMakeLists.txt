cmake_minimum_required(VERSION 3.14)
project(detect_potato C)

set(CMAKE_VERBOSE_MAKEFILE on)
set(CMAKE_BUILD_TYPE "Debug")
set(CMAKE_C_COMPILER "aarch64-linux-gnu-gcc")
set(CMAKE_C_FLAGS_DEBUG "-g -O0")
set(CMAKE_C_FLAGS "-fsanitize=thread -lpthread -pie -fPIE")

set(CMAKE_C_STANDARD 99)

include_directories(demo)

add_executable(detect_potato main.c)
add_executable(general-demo demo/general.c)