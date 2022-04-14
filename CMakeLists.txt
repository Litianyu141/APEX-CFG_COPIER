# CMake 最低版本号要求
cmake_minimum_required (VERSION 2.8)
# 项目名称
set(target_name "APEXcfgCopier")

#设置头文件路径
file(GLOB HEAD ${CMAKE_CURRENT_SOURCE_DIR}/source/include/*.h)
#设置cpp文件路径
file(GLOB SRC ${CMAKE_CURRENT_SOURCE_DIR}/source/*.cpp)

#set(3RD_OUTPUT_LIB_PATH ${PROJECT_SOURCE_DIR}/output/bin/x64)
#设置输出exe的目录
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${PROJECT_SOURCE_DIR}/output/bin/x64/${CMAKE_BUILD_TYPE})
set(CMAKE_ARCHIVE_OUTPUT_DIRECTORY ${PROJECT_SOURCE_DIR}/output/bin/x64/${CMAKE_BUILD_TYPE})
set(CMAKE_LIBARAY_OUTPUT_DIRECTORY ${PROJECT_SOURCE_DIR}/output/bin/x64/${CMAKE_BUILD_TYPE})
# 指定生成目标
add_executable(${target_name} ${SRC} ${HEAD})
#设置include的路径

include_directories(${CMAKE_CURRENT_SOURCE_DIR}/source/include)

MESSAGE( STATUS "dir = ${CMAKE_CURRENT_SOURCE_DIR}/source/include")