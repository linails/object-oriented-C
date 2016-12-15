# readme.txt
# Created Time: 2016-04-23 14:20:56
# Last modified: 2016-12-15 21:07:52
#
cmake_minimum_required(VERSION 2.8)

include_directories(
    ${PROJECT_SOURCE_DIR}/src
    ${PROJECT_SOURCE_DIR}/src/libs
    ${PROJECT_SOURCE_DIR}/src/srcs
)

#aux_source_directory(. SRC_LIST)
#aux_source_directory(./libs/ SRC_LIST)
#aux_source_directory(./srcs/ SRC_LIST)

set(SRC_LIST
   main.c 
#   srcs/xx.c
#####################################################################
#   srcs/xx.c
)

add_executable(ooc ${SRC_LIST})

if ("${SYSTEM_TYPE}" STREQUAL "i686")
set(libs_path ${PROJECT_SOURCE_DIR}/src/libs/i686)
endif()

if ("${SYSTEM_TYPE}" STREQUAL "x86_64")
set(libs_path ${PROJECT_SOURCE_DIR}/src/libs/x86_64)
endif()

set(link_lib
    #${libs_path}/libsqlite3.a
    pthread
    dl
)

target_link_libraries(ooc ${link_lib})

