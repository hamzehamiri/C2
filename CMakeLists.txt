cmake_minimum_required(VERSION 3.23)
project(C2)

set(CMAKE_CXX_STANDARD 23)
set(CMAKE_MODULE_PATH ${CMAKE_MODULE_PATH} "${CMAKE_CURRENT_SOURCE_DIR}/cmake")
set(DCMAKE_TOOLCHAIN_FILE /opt/Tools/vcpkg/scripts/buildsystems/vcpkg.cmake)
#set(SQLITE3_INCLUDE_DIRS /opt/Tools/vcpkg/packages/sqlite3_x64-linux/include)
#set(SQLITE3_LIBRARIES /opt/Tools/vcpkg/packages/sqlite3_x64-linux/lib/libsqlite3.a)

add_executable(C2 main.cpp)

#find_package (SQLite3)

#find_package(unofficial-sqlite3 CONFIG REQUIRED)
find_package(yaml-cpp CONFIG REQUIRED)

#include_directories(${SQLITE3_INCLUDE_DIRS})
#target_link_libraries (C2 ${SQLITE3_LIBRARIES})
#target_link_libraries (C2 PRIVATE unofficial::sqlite3::sqlite3)
target_link_libraries (C2 PRIVATE yaml-cpp)

if (SQLITE3_FOUND)

endif (SQLITE3_FOUND)
