project(libinfo-rpc)

cmake_minimum_required(VERSION 2.4.0)

include_directories(${CMAKE_CURRENT_SOURCE_DIR}/../../libc/locale)
include_directories(${CMAKE_CURRENT_SOURCE_DIR}/../../libc/locale/FreeBSD)
include_directories(${CMAKE_CURRENT_SOURCE_DIR}/../../libc/pthreads)
include_directories(${CMAKE_CURRENT_SOURCE_DIR}/../../libc/stdtime/FreeBSD)
include_directories(${CMAKE_CURRENT_SOURCE_DIR}/../../external/libdispatch/)
include_directories(${CMAKE_CURRENT_SOURCE_DIR}/../../external/libdispatch/private)
include_directories(${DARLING_TOP_DIRECTORY}/src/libresolv)
include_directories(${DARLING_TOP_DIRECTORY}/src/libresolv/dnsinfo)
include_directories(${CMAKE_CURRENT_SOURCE_DIR})

set(CMAKE_C_FLAGS "${CMAKE_C_FLAGS} -fblocks")

set(info-rpc_sources
	bindresvport.c
)

add_library(info-rpc OBJECT ${info-rpc_sources})
