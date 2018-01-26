cmake_minimum_required(VERSION 2.8)


add_library(lwftp-object OBJECT lwftp/lwftp.c)
add_library(lwftp-static STATIC lwftp/lwftp.c)

target_include_directories(lwftp-static PUBLIC ${CMAKE_CURRENT_LIST_DIR})
