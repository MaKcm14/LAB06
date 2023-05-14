cmake_minimum_required(VERSION 3.25.1 FATAL_ERROR)

project(new_ex_formatter)

add_library(formatter_lib STATIC ../formatter_lib/formatter.cpp)
target_include_directories(formatter_lib PUBLIC ../formatter_lib)

add_library(formatter_ex STATIC ./formatter_ex.cpp)

target_link_libraries(formatter_ex formatter_lib)
