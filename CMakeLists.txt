cmake_minimum_required(VERSION 3.16)
project(mosek_example)

set(CMAKE_CXX_STANDARD 14)

set(MOSEK_INCLUDE_DIR "/home/yutaka/mosek/9.2/tools/platform/linux64x86/h")
set(MOSEK_LIB_DIR "/home/yutaka/mosek/9.2/tools/platform/linux64x86/bin")

include_directories(${MOSEK_INCLUDE_DIR})
link_directories(${MOSEK_LIB_DIR})

add_executable(mosek_main main.cpp)
target_link_libraries(mosek_main mosek64 fusion64)