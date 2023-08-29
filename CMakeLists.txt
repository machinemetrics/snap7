cmake_minimum_required(VERSION 3.16)
project(snap7 VERSION 1.4.2 LANGUAGES CXX)
#add_subdirectory(src)


add_custom_command(
     OUTPUT ${CMAKE_CURRENT_SOURCE_DIR}/build/bin/x86_64-linux/libsnap7.so
     COMMAND make -f x86_64_linux.mk all
     WORKING_DIRECTORY ./build/unix
)

add_custom_target(
     snap7_target
     DEPENDS ${CMAKE_CURRENT_SOURCE_DIR}/build/bin/x86_64-linux/libsnap7.so
)

add_library(snap7 STATIC IMPORTED GLOBAL)
add_dependencies(snap7 snap7_target)

set_target_properties(
    snap7
    PROPERTIES
    IMPORTED_LOCATION ${CMAKE_CURRENT_SOURCE_DIR}/build/bin/x86_64-linux/libsnap7.so
    INTERFACE_INCLUDE_DIRECTORIES ${CMAKE_CURRENT_SOURCE_DIR}/src/core ${CMAKE_CURRENT_SOURCE_DIR}/src/lib ${CMAKE_CURRENT_SOURCE_DIR}/src/sys
)