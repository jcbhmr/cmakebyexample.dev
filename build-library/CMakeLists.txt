cmake_minimum_required(VERSION 3.28)
project(my-project)
add_library(my-lib STATIC my-lib.c)
add_library(my-lib SHARED my-lib.c)
