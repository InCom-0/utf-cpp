cmake_minimum_required(VERSION 3.30...4.0)
project(utf-cpp)


add_library(utf-cpp INTERFACE)
add_library(utf-cpp::utf-cpp ALIAS utf-cpp)
target_include_directories(utf-cpp INTERFACE ${CMAKE_CURRENT_SOURCE_DIR}/include)
target_compile_features(utf-cpp INTERFACE cxx_std_23)