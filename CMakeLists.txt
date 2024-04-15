cmake_minimum_required(VERSION 3.16)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED True)

file (READ ${CMAKE_SOURCE_DIR}/VERSION VERSION)

string(STRIP ${VERSION} VERSION)

message("PROJECT_VERSION = ${VERSION}")

project(Hello LANGUAGES CXX VERSION ${VERSION})

set (SOURCE_DIR ${CMAKE_CURRENT_SOURCE_DIR}/src)
set (INCLUDE_DIR ${CMAKE_CURRENT_SOURCE_DIR}/include)

set(target_sources
    hello.cpp
    main.cpp
)
list(TRANSFORM target_sources PREPEND "src/")

include_directories("${INCLUDE_DIR}")

add_executable(Hello ${target_sources})