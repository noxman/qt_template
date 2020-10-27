cmake_minimum_required(VERSION 3.17)
project(qt)

set(CMAKE_CXX_STANDARD 14)
set(CMAKE_CXX_FLAGS -s)

#set(CMAKE_PREFIX_PATH "D:\\msys64\\mingw64")
set(CMAKE_PREFIX_PATH "D:\\msys64\\mingw64\\qt5-static")

set(CMAKE_AUTOMOC ON)
set(CMAKE_AUTOUIC ON)
set(CMAKE_AUTORCC ON)

add_executable(
        qt WIN32
        main.cpp mainwindow.cpp
        mainwindow.ui)
find_package(Qt5Widgets REQUIRED)
find_package(Qt5Core REQUIRED)
target_link_libraries(qt Qt5::Widgets)