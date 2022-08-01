cmake_minimum_required(VERSION 3.20)
set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED True)

project(chip8_emu)
add_executable(chip8_emu main.cpp)

include_directories(SDL2/include)
target_link_libraries(chip8_emu ${CMAKE_CURRENT_LIST_DIR}/SDL2/lib/x64/SDL2main.lib)
target_link_libraries(chip8_emu ${CMAKE_CURRENT_LIST_DIR}/SDL2/lib/x64/SDL2.lib)
