cmake_minimum_required(VERSION 3.0.0)
project(FastCGIServer VERSION 0.1.0)

include(CTest)
enable_testing()

set(CPACK_PROJECT_NAME ${PROJECT_NAME})
set(CPACK_PROJECT_VERSION ${PROJECT_VERSION})
include(CPack)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED on)
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS}")

add_executable(FastCGIServer main.cpp)
target_link_libraries(FastCGIServer -lfcgi++ -lfcgi -lpthread)