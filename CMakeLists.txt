cmake_minimum_required(VERSION 2.8 FATAL_ERROR)

project(color)

find_package(PCL 1.7 REQUIRED)
find_package(OpenCV REQUIRED )

include_directories( ${OPENCV_INCLUDE_DIR} )
include_directories(${PCL_INCLUDE_DIRS})
link_directories(${PCL_LIBRARY_DIRS})
add_definitions(${PCL_DEFINITIONS})

add_executable (color src/color.cpp)


target_link_libraries (color  ${PCL_LIBRARIES} opencv_core opencv_highgui
opencv_flann opencv_imgproc opencv_highgui opencv_ml opencv_video opencv_objdetect
          opencv_features2d opencv_calib3d opencv_legacy opencv_contrib
)

