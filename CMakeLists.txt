cmake_minimum_required(VERSION 3.5.0)
project(cv1 VERSION 0.1.0 LANGUAGES C CXX)

include(CTest)
enable_testing()

set(CMAKE_PREFIX_PATH ${CMAKE_PREFIX_PATH} C:/Users/evahn/Desktop/Cours Kyushu/Computer Vision/opencv/build/x64/vc16/lib)
find_package( OpenCV REQUIRED )
include_directories( ${OpenCV_INCLUDE_DIRS} )

add_executable(cv1 main.cpp)

target_link_libraries( cv1 ${OpenCV_LIBS} )

set(CPACK_PROJECT_NAME ${PROJECT_NAME})
set(CPACK_PROJECT_VERSION ${PROJECT_VERSION})
include(CPack)
