project(PackageTest CXX)
cmake_minimum_required(VERSION 2.8.12)

include(${CMAKE_BINARY_DIR}/conanbuildinfo.cmake)
conan_basic_setup()

find_package(hayai CONFIG REQUIRED)

add_executable(example example.cpp)
target_link_libraries(example ${CONAN_LIBS})
