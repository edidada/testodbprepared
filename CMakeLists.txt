cmake_minimum_required(VERSION 3.13)
project(testodbprepared)

set(CMAKE_CXX_STANDARD 11)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11 -DDATABASE_MYSQL")

add_executable(testodbprepared driver.cxx person-odb.cxx)

target_link_libraries(testodbprepared libodb-mysql.so)

target_link_libraries(testodbprepared libodb.so)