# CMake and project set up
cmake_minimum_required(VERSION 3.21)
project(NeuTRANS2D)

# Require C++20
set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

# Sources
set(NeuTRANS_SRC
        )

# Main code
add_executable(NeuTRANS2D.x ${CMAKE_CURRENT_SOURCE_DIR}/main.cpp)
target_include_directories(NeuTRANS2D.x PUBLIC ${CMAKE_CURRENT_SOURCE_DIR}/include)


#### FOR TESTING PURPOSES ###
# Testing binary
#set(NeuTRANS_TEST_SRC ${CMAKE_CURRENT_SOURCE_DIR}/src/testFun.cpp)
#add_executable(cpp_test ${CMAKE_CURRENT_SOURCE_DIR}/test/test.cpp ${NeuTRANS_TEST_SRC})
#target_include_directories(cpp_test PUBLIC ${CMAKE_CURRENT_SOURCE_DIR}/include)
## enable testing functionality
#enable_testing()
## define tests
#add_test(NAME cpp_test COMMAND $<TARGET_FILE:cpp_test>)