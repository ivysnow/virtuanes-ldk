cmake_minimum_required(VERSION 3.21 FATAL_ERROR)

project(LDK)

add_library(LDK MODULE
    LDK.cpp
    LDK.def
    VirtuaNES.rc
    VirtuaNESres.h
)
target_compile_definitions(LDK
PRIVATE
    _MBCS
    _USRDLL
    LDK_EXPORTS
)
set_target_properties(LDK PROPERTIES
    OUTPUT_NAME "Japanese"
    SUFFIX ".vlp"
)
