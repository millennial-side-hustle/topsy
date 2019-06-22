cmake_minimum_required(VERSION 3.13)
project(topsy)

set(CMAKE_CXX_STANDARD 17)

add_executable(topsy main.cpp)

link_directories(/usr/local/lib)
include_directories(/usr/local/include)

find_package(libpqxx REQUIRED)
find_package(RapidJSON REQUIRED)

target_link_libraries(topsy libpqxx::pqxx_shared)

