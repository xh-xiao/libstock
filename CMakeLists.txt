cmake_minimum_required (VERSION 2.6)
project (libstock)
add_subdirectory (src)

#find_package( Boost 1.60 COMPONENTS program_options regex )

#include_directories(${Boost_INCLUDE_DIRS}) 
#target_link_libraries(progname ${Boost_LIBRARIES})
#add_executable( test test/timeseries_test.cpp )

include_directories( "test/include" )
target_link_libraries("test/libs/libgtest.a")
add_executable( gtest test/timeseries_gtest.cpp )

