
cmake_minimum_required(VERSION 3.28)

project(ExampleDependency)

set(PACKAGE_NAME ExampleDependency)
set(PACKAGE_VERSION 0.0.0)

add_library(sekrit-sos)
target_sources(sekrit-sos
  PRIVATE
    sekrit-sos.cpp
)
target_compile_features(sekrit-sos
  PUBLIC
    cxx_std_23
)
target_include_directories(sekrit-sos
  PUBLIC
    $<BUILD_INTERFACE:${CMAKE_CURRENT_SOURCE_DIR}/include>
)
