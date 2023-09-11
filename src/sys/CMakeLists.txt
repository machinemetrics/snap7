target_sources(snap7 PUBLIC
    ${CMAKE_CURRENT_SOURCE_DIR}/snap_msgsock.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/snap_sysutils.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/snap_tcpsrvr.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/snap_threads.cpp
)

target_include_directories(snap7 PUBLIC ${CMAKE_CURRENT_SOURCE_DIR})