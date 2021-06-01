cmake_minimum_required(VERSION 3.0.0)

project(Calculator_Project VERSION 1.0.0)

add_subdirectory(my_math_dir)
add_subdirectory(my_print_dir)

add_executable(calculator 
main.cpp)

set(restclient-cpp_DIR ${CMAKE_PREFIX_PATH})

include(/home/alphapro/vcpkg/scripts/buildsystems/vcpkg.cmake)

find_package(restclient-cpp CONFIG REQUIRED)
    
if(restclient-cpp_FOUND)
    message("Founded")
    target_link_libraries(calculator PRIVATE restclient-cpp)
else()
    message("Not found")
endif()

target_link_libraries(calculator PRIVATE my_math my_print)

message(${CMAKE_INSTALL_PREFIX})