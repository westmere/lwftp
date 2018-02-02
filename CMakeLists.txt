cmake_minimum_required(VERSION 2.8)

option(USE_STATIC_LWFTP_LIBRARY "Build LWFTP static library." OFF)
option(USE_OBJECT_LWFTP_LIBRARY "Build LWFTP object library." ON)

if(USE_STATIC_LWFTP_LIBRARY)
    add_library(lwftp-static STATIC lwftp/lwftp.c)
    target_include_directories(lwftp-static PUBLIC ${CMAKE_CURRENT_LIST_DIR})
endif(USE_STATIC_LWFTP_LIBRARY)
    
if(USE_OBJECT_LWFTP_LIBRARY)
    add_library(lwftp-object OBJECT lwftp/lwftp.c)
endif(USE_OBJECT_LWFTP_LIBRARY)
