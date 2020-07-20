cmake_minimum_required(VERSION 2.8)
project( DisplayImage )

find_package( OpenCV REQUIRED )

file(GLOB SOURCES
	"${ROOT_DIR}/include/*.h"
	"${ROOT_DIR}/src/*.cpp"
	"${ROOT_DIR}/main.cpp")

add_executable( DisplayImage DisplayImage.cpp )
target_link_libraries( DisplayImage ${OpenCV_LIBS} )