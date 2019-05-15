cmake_minimum_required(VERSION 2.8)

# project name
project(fbcp)

# version number
set(fbcp_VERSION_MAJOR 1)
set(fbcp_VERSION_MINIOR 0)
set(fbcp_VERSION_PATCH 0)

set(COMPILE_DEFINITIONS -Werror)

add_executable(fbcp main.c)

find_library(LIB_VCHOSTIF vchostif)
find_library(LIB_BCM_HOST bcm_host)

target_link_libraries(fbcp "${LIB_VCHOSTIF}" "${LIB_BCM_HOST}")
install(TARGETS fbcp DESTINATION bin)
