cmake_minimum_required(VERSION 3.21)

project(Complementily VERSION 1.0.0)

set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

if (NOT DEFINED GEODE_SDK)
    message(FATAL_ERROR "GEODE_SDK no está definido")
endif()

setup_geode_mod(
    TARGET Complementily
    VERSION ${PROJECT_VERSION}
    ID angel.complementily
)

target_sources(Complementily PRIVATE
    src/main.cpp
)