cmake_minimum_required(VERSION 3.10)
project(nodes)

file(GLOB NODES_SOURCES
    crude_json.cpp
    imgui_canvas.cpp
    imgui_node_editor.cpp
    imgui_node_editor_api.cpp
)

add_library(nodes STATIC ${NODES_SOURCES})

 target_include_directories(nodes PUBLIC ${CMAKE_CURRENT_SOURCE_DIR})

target_link_libraries(nodes PUBLIC imgui)

