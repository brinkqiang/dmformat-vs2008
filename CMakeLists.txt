cmake_minimum_required(VERSION 2.8)

PROJECT(dmformat)

LIST(APPEND CMAKE_MODULE_PATH ${CMAKE_CURRENT_SOURCE_DIR}/cmake)
INCLUDE(cmake/ModuleImport.cmake)
INCLUDE(cmake/ModuleCompileOptions.cmake)
ModuleSetCompileOptions()
ModuleSetWinCompilerFlags()

ADD_DEFINITIONS(-DUSE_DMFORMAT)

LibImport("dmformat" "src")
ExeImport("test" "dmformat")
