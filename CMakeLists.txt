cmake_minimum_required(VERSION 3.14)
add_library (tinyhttp
chunk.c
chunk.h
header.c
header.h
http.c
http.h
)
set_target_properties(tinyhttp PROPERTIES POSITION_INDEPENDENT_CODE ON)

add_executable(example example.cpp)
target_link_libraries(example tinyhttp)

