# readme.txt
# Created Time: 2016-04-23 14:15:51
# Last modified: 2016-12-15 21:07:27
#
cmake_minimum_required(VERSION 2.8)

project(program-train)

set(CMAKE_C_FLAGS "$ENV{CMAKE_C_FLAGS} -std=c99 -g -Wall")

add_subdirectory(src bin)

