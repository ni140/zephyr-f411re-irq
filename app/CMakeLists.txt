cmake_minimum_required(VERSION 3.20.0)

set(BOARD nucleo_f411re)

find_package(Zephyr REQUIRED HINTS $ENV{ZEPHYR_BASE})

project(zephyr-app C CXX)

target_sources(app PRIVATE src/main.c)

target_include_directories(app PRIVATE ${ZEPHYR_BASE}/include/zephyr)
target_include_directories(app PRIVATE ${CMAKE_CURRENT_SOURCE_DIR})
