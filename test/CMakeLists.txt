# 测试，主要用于生成测试可执行文件
cmake_minimum_required(VERSION 3.26)
project(test)

aux_source_directory(./ SRC)

link_directories(${LIB_PATH})
link_libraries(${CONFIG_LIB_NAME} ${UTILS_LIB_NAME})

set(EXECUTABLE_OUTPUT_PATH ${EXEC_PATH})
add_executable(test ${SRC})