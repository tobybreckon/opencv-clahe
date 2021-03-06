# OpenCV CLAHE cmake configuration file

# Author : Toby Breckon, toby.breckon@durham.ac.uk

# Copyright (c) 2017 Engineering and Computer Science, Durham University
# License : GPL - http://www.gnu.org/licenses/gpl.html

cmake_minimum_required (VERSION 2.6)

# linux specific stuff

IF ( UNIX )
   set( CMAKE_CXX_FLAGS "-O3 -Wall -march=native ${CMAKE_CXX_FLAGS}" )
   set( CMAKE_PREFIX_PATH "/opt/opencv" )
   set_property(GLOBAL PROPERTY TARGET_SUPPORTS_SHARED_LIBS TRUE)
   MESSAGE( "LINUX/UNIX SPECIFIC CONFIG" )
ENDIF ( UNIX )

# windows (also for 64-bit as WIN32 defined on MS WIN 64-bit also - ?!)

IF ( WIN32 )
   set( CMAKE_PREFIX_PATH "C:/OpenCV/build" )
   set( OpenCV_DIR "C:/OpenCV/build" )
   MESSAGE( "WINDOWS CONFIG - assuming OpenCV in C:/OpenCV/build" )
ENDIF ( WIN32 )

find_package( OpenCV REQUIRED )

project(adapthistequal)
add_executable(adapthistequal adapthistequal.cpp clahe.cpp)
target_link_libraries(adapthistequal ${OpenCV_LIBS} )
