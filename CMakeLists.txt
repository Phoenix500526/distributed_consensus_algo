cmake_minimum_required(VERSION 3.13)
project(distributed_consensus_algo)

set(CMAKE_CXX_STANDARD 17)

find_file(CLANG_FORMAT_BIN_NAME clang-format)
if(CLANG_FORMAT_BIN_NAME)
    message(STATUS "Code Formatter: ${CLANG_FORMAT_BIN_NAME}")
    add_custom_target(
        format
        COMMAND ${CLANG_FORMAT_BIN_NAME}
        -i
        ${ALL_SOURCE_FILES}
    )
endif()