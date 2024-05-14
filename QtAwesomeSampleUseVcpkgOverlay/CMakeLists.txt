cmake_minimum_required(VERSION 3.16)
project(QtAwesomeSample)

find_package(QT NAMES Qt6 Qt5 REQUIRED COMPONENTS Core)
find_package(Qt${QT_VERSION_MAJOR} REQUIRED COMPONENTS Core Widgets)

set(CMAKE_AUTOUIC ON)
set(CMAKE_AUTOMOC ON)
set(CMAKE_AUTORCC ON)

find_package(QtAwesome REQUIRED)

add_executable(QtAwesomeSample
  mainwindow.cpp
  main.cpp
  )

target_link_libraries(QtAwesomeSample
  PUBLIC QtAwesome::QtAwesome
)
