project(process)

#生成动态库
add_library(${PROJECT_NAME}
SHARED
process.cpp)

#声明头文件和链接动态库

target_include_directories(${PROJECT_NAME}
PUBLIC
${CMAKE_SOURCE_DIR}/src/pnc_map
)

target_link_libraries(${PROJECT_NAME}
PUBLIC
pnc_map
)

