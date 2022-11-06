cmake_minimum_required(VERSION 3.2)

project(giflib VERSION 5.1.2 LANGUAGES C)

if(MSVC)
    set(CMAKE_DEBUG_POSTFIX "d")
endif()

add_library(giflib
    dgif_lib.c
    egif_lib.c
    gif_err.c
    gif_font.c
    gif_hash.c
    gifalloc.c
    openbsd-reallocarray.c
    quantize.c
)

target_include_directories(giflib PUBLIC ./)