# todo: downgrade cmake version
cmake_minimum_required(VERSION 3.0.0)

# Store your project namme here
set(PROJECT_NAME "single_target")

project(${PROJECT_NAME})

# Set your cpp standard
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11")

# todo: cannot remember right now what is it
# set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${PROJECT_SOURCE_DIR}/bin)

#---------------------------------------------------------

# Store your files here
set(SOURCES mock_main.cpp mock_dummy.cpp)
set(HEADERS mock_dummy.h)

#---------------------------------------------------------

set(ALL_FILES ${SOURCES}
              ${HEADERS}
              )

add_executable(${PROJECT_NAME} ${ALL_FILES})

# Filters
source_group("" FILES ${ALL_FILES})