cmake_minimum_required( VERSION 2.8 )

Project( HelloSLAM )

add_executable( helloSLAM helloSLAM.cpp ) 

add_library( hello libHelloSLAM.cpp )

add_library( hello_shared SHARED libHelloSLAM.cpp )

add_executable( useHello useHello.cpp )

target_link_libraries( useHello hello_shared )

set( CMAKE_BUILD_TYPE "Debug" )
