cmake_minimum_required(VERSION 3.30...4.0)
project(utf-cpp)


add_library(utf-cpp INTERFACE)
add_library(utf-cpp::utf-cpp ALIAS utf-cpp)
target_compile_features(utf-cpp INTERFACE cxx_std_17)
target_sources(incplot-lib
    PUBLIC
    FILE_SET pub_headers
    TYPE HEADERS
    BASE_DIRS
    include/)


option(UTFCPP_BUILD_TESTS "Build tests" FALSE)
if(UTFCPP_BUILD_TESTS)
    add_subdirectory(test)
endif()