cmake_minimum_required(VERSION 3.19)

project(HelloWorld)
include(cmake/StandardProjectSettings.cmake)

if (MSVC)
  add_compile_options(/W4)
else()
  add_compile_options(-Wall -Wextra -Wpedantic)
endif()

add_executable(hello src/main.cpp)
target_compile_features(hello PRIVATE cxx_lambda_init_captures)

