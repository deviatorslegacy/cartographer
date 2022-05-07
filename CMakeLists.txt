cmake_minimum_required(VERSION 3.10)

project(cartographer VERSION 0.1.0)

file(GLOB SOURCE_FILES "${PROJECT_SOURCE_DIR}/src/*.c")
set(INCLUDE_DIR "${PROJECT_SOURCE_DIR}/src/include/")

configure_file("${INCLUDE_DIR}/config.h.in" "${INCLUDE_DIR}/config.h")

add_executable(cartographer ${SOURCE_FILES})

target_include_directories(cartographer PUBLIC ${INCLUDE_DIR})
