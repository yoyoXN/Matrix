cmake_minimum_required(VERSION 3.23.0)
project(Matrix VERSION 0.1.0)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

set(MATRIX_ROOT_DIR ${CMAKE_CURRENT_SOURCE_DIR})
set(CMAKE_INSTALL_PREFIX ${MATRIX_ROOT_DIR}/bin)
set(BINARY_ROOT_DIR ${CMAKE_INSTALL_PREFIX}/)

set(EXECUTABLE_OUTPUT_PATH ${BINARY_ROOT_DIR})
set(LIBRARY_OUTPUT_PATH ${BINARY_ROOT_DIR})

add_subdirectory(engine)