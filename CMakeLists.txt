cmake_minimum_required(VERSION 3.5)
project(dummy_lib)

set(CMAKE_CXX_STANDARD 17)

add_library(${PROJECT_NAME} dummy.cpp)

target_include_directories(${PROJECT_NAME} PUBLIC include)

set_target_properties(${PROJECT_NAME} PROPERTIES PUBLIC_HEADER "include/dummy.hpp")

install(TARGETS ${PROJECT_NAME} PUBLIC_HEADER DESTINATION ${CMAKE_INSTALL_INCLUDEDIR})
