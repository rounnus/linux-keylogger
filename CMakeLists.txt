cmake_minimum_required(VERSION 3.20)
project(linux_keylogger C)

set(CMAKE_C_STANDARD 99)

add_executable(linux_keylogger main.c tools/include/file/file_handler.h tools/file_handler.c mapper/kb_mapper.c mapper/include/kb_mapper.h worker/kb_worker.c worker/include/kb_worker.h logger/include/logs/logger.h mem/include/mem.h kb_logger/include/kb_decoder.h kb_logger/kb_decoder.c tools/include/constants/constants.h)

set(GCC_COVERAGE_COMPILE_FLAGS "-pthread")
set(CMAKE_C_FLAGS "${CMAKE_C_FLAGS} ${GCC_COVERAGE_COMPILE_FLAGS}")

file(MAKE_DIRECTORY /home/$ENV{USER}/.local/share/keylogger/)
file(MAKE_DIRECTORY /home/$ENV{USER}/.local/share/keylogger/logs)

include_directories(
        tools/include
        worker/include
        mapper/include
        kb_logger/include
        data_structures/include
        logger/include
        mem/include
)