cmake_minimum_required(VERSION 3.1.0)

project(cs471_proj3)

# Use C++ 11 standard
set(CMAKE_CXX_STANDARD 11)

# Add threading lib
set(THREADS_PREFER_PTHREAD_FLAG ON)
find_package(Threads REQUIRED)

#Specify include dir
include_directories(include)

# Add all *.cpp files in ../src
file(GLOB SOURCES "src/*.cpp")

add_executable(cs471_proj3.out ${SOURCES})

# Link threading lib
target_link_libraries(cs471_proj3.out Threads::Threads)
