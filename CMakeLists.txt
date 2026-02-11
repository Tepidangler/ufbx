cmake_minimum_required(VERSION 4.1)
set(CMAKE_CXX_STANDARD 20)


set(UFBX_INC_DIR
        ${CMAKE_CURRENT_SOURCE_DIR}
)
project(ufbx)

add_library(ufbx STATIC
        ufbx.c
        ufbx.h
        ufbx_libc.c
        ufbx_libc.h
        ufbx_math.c
        ufbx_math.h
        ufbx_os.h
        ufbx_stl.h
)

set_property(TARGET ufbx PROPERTY
        MSVC_RUNTIME_LIBRARY "MultiThreaded$<$<CONFIG:Debug>:Debug>")