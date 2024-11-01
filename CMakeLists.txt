cmake_minimum_required(VERSION 3.10)

project(test1
    VERSION 0.01
    DESCRIPTION "a demo"
    HOMEPAGE_URL "https://github.com/liu112129/cmake-test1"
    LANGUAGES CXX
)

set(CMAKE_CXX_STANDARD 11)
#变量设置
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${PROJECT_SOURCE_DIR}/bin)


#添加子目录
add_subdirectory(src)