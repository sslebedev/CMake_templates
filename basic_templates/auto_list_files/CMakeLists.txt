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

# Store yor sources root here
set(SRC_ROOT_PATH "${CMAKE_SOURCE_DIR}")
file(
    GLOB_RECURSE ALL_FILES 
    LIST_DIRECTORIES false
    "${SRC_ROOT_PATH}/*.c*"
    "${SRC_ROOT_PATH}/*.h*"
)

add_executable(${PROJECT_NAME} ${ALL_FILES})

#Filters
foreach(SOURCE IN ITEMS ${ALL_FILES})
    get_filename_component(SOURCE_PATH "${SOURCE}" PATH)
    file(RELATIVE_PATH SOURCE_PATH_REL "${SRC_ROOT_PATH}" "${SOURCE_PATH}")
    string(REPLACE "/" "\\" GROUP_PATH "${SOURCE_PATH_REL}")
    source_group("${GROUP_PATH}" FILES "${SOURCE}")
endforeach()
