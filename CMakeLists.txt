cmake_minimum_required(VERSION 3.1)

Project(mirror)

set(SourcesPath ${PROJECT_SOURCE_DIR}/Engine/Source)
SET(SRC_LIST Game.cpp)
#MESSAGE(STATUS "This is BINARY dir " ${mirror_BINARY_DIR})
#MESSAGE(STATUS "This is SOURCE dir "${mirror_SOURCE_DIR})
ADD_EXECUTABLE(mirror ${SourcesPath}/Programs/Game.cpp)