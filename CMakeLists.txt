cmake_minimum_required(VERSION 3.13)

project(GeomView VERSION 1.0 LANGUAGES CXX)

include(FetchContent)
FetchContent_Declare(glfw GIT_REPOSITORY https://github.com/glfw/glfw.git GIT_TAG master)

set(GLFW_BUILD_DOCS OFF CACHE BOOL "" FORCE)
set(GLFW_BUILD_TESTS OFF CACHE BOOL "" FORCE)
set(GLFW_BUILD_EXAMPLES OFF CACHE BOOL "" FORCE)

FetchContent_MakeAvailable(glfw)

set(SOURCE_DIR ${CMAKE_SOURCE_DIR}/src)
set(LIBRARY_DIR ${CMAKE_SOURCE_DIR}/libs)

set(SOURCES ${SOURCE_DIR}/main.cpp)

target_link_libraries(GeomView PRIVATE glfw)

add_executable(GeomView ${SOURCES})