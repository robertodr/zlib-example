cmake_minimum_required(VERSION 3.1 FATAL_ERROR)

project(zlib-example CXX)

find_package(ZLIB REQUIRED)

add_executable(zlib-example zlib-example.cpp)
target_include_directories(zlib-example
  PUBLIC
    ZLIB::ZLIB
  )
target_link_libraries(zlib-example
  PUBLIC
    ZLIB::ZLIB
  )

add_executable(cnpy-example cnpy-example.cpp cnpy.cpp)
target_include_directories(cnpy-example
  PUBLIC
    ZLIB::ZLIB
    ${PROJECT_SOURCE_DIR}
  )
target_link_libraries(cnpy-example
  PUBLIC
    ZLIB::ZLIB
  )
