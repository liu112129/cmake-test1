project(main)

#有两个子目录
add_subdirectory(pnc_map)
add_subdirectory(process)


#有一个头文件，需要声明位置和连接动态库（main文件不生成动态库，而是生成可执行文件）
#生成可执行文件
add_executable(${PROJECT_NAME} planning_main.cpp)

#声明头文件位置
target_include_directories(${PROJECT_NAME}
    PUBLIC
    ${CMAKE_SOURCE_DIR}/src/process
)

#链接动态库
target_link_libraries(${PROJECT_NAME}
PUBLIC
process
)
