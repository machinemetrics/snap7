target_sources(snap7 PUBLIC
    ${CMAKE_CURRENT_SOURCE_DIR}/s7_client.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/s7_isotcp.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/s7_micro_client.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/s7_partner.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/s7_peer.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/s7_server.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/s7_text.cpp
)

target_include_directories(snap7 PUBLIC ${CMAKE_CURRENT_SOURCE_DIR})