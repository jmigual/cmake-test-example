cmake_minimum_required(VERSION 3.21 FATAL_ERROR)

project(CPP_test LANGUAGES CXX)

add_executable(app src/main.cpp)
target_compile_features(app PUBLIC cxx_std_20)
target_include_directories(app PUBLIC include)

include(CTest)

add_test(NAME test COMMAND app)
add_test(NAME test2 COMMAND app)
