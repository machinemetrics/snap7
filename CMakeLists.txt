cmake_minimum_required(VERSION 3.16)
project(snap7 VERSION 1.4.2 LANGUAGES CXX)
add_library(snap7 STATIC "")

target_include_directories(snap7 PUBLIC ${CMAKE_CURRENT_SOURCE_DIR})

add_subdirectory(src/core)
add_subdirectory(src/lib)
add_subdirectory(src/sys)

install(
    TARGETS snap7
    LIBRARY DESTINATION ${PROJECT_INSTALL_LIBRARY_DIR}
    PUBLIC_HEADER DESTINATION ${PROJECT_INSTALL_INCLUDE_DIR}
)