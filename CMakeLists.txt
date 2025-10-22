cmake_minimum_required(VERSION 3.15)

project(Plugin)

include(ZeekPlugin)

find_package(Napatech REQUIRED)

zeek_add_plugin(Zeek Napatech
    INCLUDE_DIRS ${NAPATECH_INCLUDE_DIR}
    DEPENDENCIES ${NAPATECH_LIBRARY}
    SOURCES src/Plugin.cc src/Napatech.cc
    BIFS src/Napatech.bif
)
