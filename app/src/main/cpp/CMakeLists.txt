cmake_minimum_required(VERSION 3.12)

# ADICIONE ESTA LINHA ABAIXO:
project(sasamp_native) 

include_directories(
        ${CMAKE_CURRENT_LIST_DIR}/opus/include
)

find_package(shadowhook REQUIRED CONFIG)
add_subdirectory(opus)
add_subdirectory(multiplayer)

target_compile_options(opus PRIVATE -O3)
