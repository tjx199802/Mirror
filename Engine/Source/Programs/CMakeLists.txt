cmake_minimum_required(VERSION 3.1)
Project(mirror)

set(CMAKE_BUILD_TYPE Debug CACHE STRING "Choose the type of build." FORCE)
set_property(CACHE CMAKE_BUILD_TYPE PROPERTY STRINGS "Debug" "Release"
    "MinSizeRel" "RelWithDebInfo")
include_directories(../Fondation)
include_directories(${PROJECT_SOURCE_DIR}/../Fondation/Platform)
include_directories(${PROJECT_SOURCE_DIR}/../Fondation/Archtect)
include_directories(${PROJECT_SOURCE_DIR}/../Fondation/Assert)
include_directories(${PROJECT_SOURCE_DIR}/../Fondation/BuildType)

add_executable(Game Game.cpp)
# use mainCRTStartup as entry point and it will call main function in our source.
# use WinMainCRTStartup as entry point and it will call WinMain corresponding.
#set_target_properties(Game PROPERTIES LINK_FLAGS "/SUBSYSTEM:WINDOWS /ENTRY:mainCRTStartup")

target_link_libraries(Game mirror)

#install( TARGETS Game Gameapp DESTINATION "${PROJECT_SOURCE_DIR}/Binary")

INSTALL(TARGETS Game DESTINATION ${PROJECT_SOURCE_DIR}}
)
