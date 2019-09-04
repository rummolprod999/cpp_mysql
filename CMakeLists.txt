cmake_minimum_required(VERSION 3.14)
project(cpp_mysql)

set(CMAKE_CXX_STANDARD 17)

set(FULL_PATH_TO_MYSQL_CONNECTOR_CPP_DIR /usr)
include_directories(${FULL_PATH_TO_MYSQL_CONNECTOR_CPP_DIR}/include)
include_directories(${FULL_PATH_TO_MYSQL_CONNECTOR_CPP_DIR}/include/cppconn)
include_directories(${FULL_PATH_TO_MYSQL_CONNECTOR_CPP_DIR}/include/jdbc)
link_directories(${FULL_PATH_TO_MYSQL_CONNECTOR_CPP_DIR}/lib)
add_executable(cpp_mysql main.cpp)
target_link_libraries(cpp_mysql curl mysqlcppconn)
target_compile_features(cpp_mysql PRIVATE cxx_range_for)