#cmake 最新要求版本
cmake_minimum_required(VERSION 3.10)
# 工程名称
project(parse_account)
#c14标准
set(CMAKE_CXX_STANDARD 14)
#包含子模块"yaml-cpp-master"
add_subdirectory(yaml-cpp-master)
add_subdirectory(lighttpd1.4)
# 生成可执行文件
add_executable(parse_account parse_account.cpp)
# 连接库,yaml-cpp 是“yal-cpp-master"目录下的CMakeLists.txt中的library 名称
target_link_libraries(parse_account yaml-cpp)
