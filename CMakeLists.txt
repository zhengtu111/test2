

cmake_minimum_required(VERSION 3.20)
project(MyProject)
# set(SOURCE_FILES main.cpp swap.cpp swap.h)
# add_executable(MyProject ${SOURCE_FILES})
# add_executable(main main.cpp)

# set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CMAKE_CURRENT_SOURCE_DIR}/build)
include_directories(MyProject include) # 指定头文件目录
aux_source_directory(MyProject src)    # 指定源文件目录
add_executable(MyProject src/main.cpp src/swap.cpp) # 指定程序入口


set(CMAKE_BUILD_TYPE Debug)
# set(CMAKE_BUILD_TYPE Release)

set(CMAKE_CXX_STANDARD 17)
# set(CMAKE_CXX_STANDARD_REQUIRED ON)
# set(CMAKE_CXX_EXTENSIONS OFF)

# add_executable(${PROJECT_NAME} src/main.cpp)


add_compile_options("/utf-8")  # MSVC 编译器专用选项[5,7](@ref)
