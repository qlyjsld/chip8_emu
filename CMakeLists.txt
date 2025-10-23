cmake_minimum_required(VERSION 3.20)
set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED True)

project(chip8_emu)
add_executable(chip8_emu main.cpp)

add_subdirectory(SDL EXCLUDE_FROM_ALL)
include_directories(SDL/include)
target_link_libraries(chip8_emu PRIVATE SDL3::SDL3)