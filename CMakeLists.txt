cmake_minimum_required(VERSION 3.21 FATAL_ERROR)

project(CPP_test LANGUAGES CXX)

include(config/CPM.cmake)

CPMAddPackage("gh:fmtlib/fmt#9.1.0")

add_executable(app src/main.cpp)
target_compile_features(app PUBLIC cxx_std_20)
target_link_libraries(app PUBLIC fmt::fmt)
target_include_directories(app PUBLIC include)
