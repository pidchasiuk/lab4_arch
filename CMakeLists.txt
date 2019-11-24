cmake_minimum_required(VERSION 3.5)
project(lab4)

add_library(chucknorris
    include/ChuckNorris.hpp
    ChuckNorris.cpp
)


target_include_directories(
  chucknorris
  PUBLIC
    "include"
)

add_executable(cpp_demo
  main.cpp
)

target_link_libraries(cpp_demo chucknorris)
