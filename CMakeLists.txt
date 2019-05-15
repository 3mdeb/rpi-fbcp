cmake_minimum_required(VERSION 2.8)

SET(COMPILE_DEFINITIONS -Werror)

add_executable(fbcp main.c)

find_library(LIB_VCHOSTIF vchostif)
find_library(LIB_BCM_HOST bcm_host)

target_link_libraries(fbcp "${LIB_VCHOSTIF} ${LIB_BCM_HOST}")
