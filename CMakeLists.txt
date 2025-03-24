cmake_minimum_required(VERSION 3.13)

project(GeomView VERSION 1.0 LANGUAGES CXX)

set(GLFW_BUILD_DOCS OFF CACHE BOOL "" FORCE)
set(GLFW_BUILD_TESTS OFF CACHE BOOL "" FORCE)
set(GLFW_BUILD_EXAMPLES OFF CACHE BOOL "" FORCE)

set(SOURCE_DIR ${CMAKE_SOURCE_DIR}/src)
set(LIBRARY_DIR ${CMAKE_SOURCE_DIR}/libs)

set(SOURCES ${SOURCE_DIR}/main.cpp)

add_subdirectory(${LIBRARY_DIR}/glfw)

target_link_libraries(GeomView glfw)

add_executable(GeomView ${SOURCES})