cmake_minimum_required(VERSION 3.10)
project(HelloWorld)
find_package(gRPC CONFIG REQUIRED)
add_executable(HelloWorld main.cpp)


