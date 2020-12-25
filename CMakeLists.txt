cmake_minimum_required(VERSION 3.17)
project(conan_cgal_example)

set(CMAKE_CXX_STANDARD 17)

set(CMAKE_MODULE_PATH ${CMAKE_BINARY_DIR} "${CMAKE_MODULE_PATH}")
message("Module path: ${CMAKE_MODULE_PATH}")

find_package(CGAL REQUIRED)

add_executable(conan_cgal_example
        main.cpp
)

target_link_libraries(conan_cgal_example PUBLIC CGAL::CGAL)