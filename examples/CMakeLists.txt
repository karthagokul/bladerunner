project(examples)
cmake_minimum_required(VERSION 2.8)
INCLUDE_DIRECTORIES(../common)
add_executable(${PROJECT_NAME}-common common.cpp)
target_link_libraries(${PROJECT_NAME}-common saho::common)

INCLUDE_DIRECTORIES(../dipc)

add_executable(${PROJECT_NAME}-watchdog-1 watchdog-example-1.cpp)
target_link_libraries(${PROJECT_NAME}-watchdog-1 saho::common)
target_link_libraries(${PROJECT_NAME}-watchdog-1 saho::dipc)
