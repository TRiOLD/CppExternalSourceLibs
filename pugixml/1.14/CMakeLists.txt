cmake_minimum_required(VERSION 3.10)
project(pugixml)

set(PUGIXML_DIR ${CMAKE_CURRENT_SOURCE_DIR})

set(PUGIXML_FILES
    ${PUGIXML_DIR}/source/pugixml.cpp
)

add_library(pugixml SHARED ${PUGIXML_FILES})
target_include_directories(pugixml PUBLIC ${PUGIXML_DIR}/include)