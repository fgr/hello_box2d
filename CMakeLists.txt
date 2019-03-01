cmake_minimum_required(VERSION 3.13)
project(hello_box2d)

set(CMAKE_CXX_STANDARD 17)

if(EXISTS ${CMAKE_BINARY_DIR}/conanbuildinfo.cmake)
    include(${CMAKE_BINARY_DIR}/conanbuildinfo.cmake)

    conan_basic_setup()
else()
    message(WARNING "The file conanbuildinfo.cmake doesn't exist, you have to run conan install first")
endif()

add_executable(hello_box2d main.cpp)
target_link_libraries(hello_box2d ${CONAN_LIBS})
