cmake_minimum_required(VERSION 3.28)
project(my-project)
add_executable(my-app main.c)
message("Hello world!")
message(WARNING "Using fallback data...")
message(FATAL_ERROR "Oh no! Not enough cat images!")
