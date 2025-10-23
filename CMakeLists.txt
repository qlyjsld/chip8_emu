cmake_minimum_required(VERSION 3.20)
set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED True)
set(CMAKE_CXX_FLAGS "-Wall")
set(CMAKE_CXX_FLAGS_DEBUG "-g")
set(CMAKE_CXX_FLAGS_RELEASE "-g -Os -DNDEBUG")
set(CMAKE_EXPORT_COMPILE_COMMANDS ON)

project(chip8_emu)
add_executable(chip8_emu main.cpp)

add_subdirectory(SDL EXCLUDE_FROM_ALL)
include_directories(SDL/include)
target_link_libraries(chip8_emu PRIVATE SDL3::SDL3)