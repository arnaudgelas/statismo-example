project( StatismoExamples )

cmake_minimum_required( VERSION 2.8 )

set( CMAKE_MODULE_PATH
  ${CMAKE_MODULE_PATH}
  ${CMAKE_CURRENT_SOURCE_DIR}/cmake
)
find_package( statismo REQUIRED )
include_directories( ${statismo_INCLUDE_DIRS} )

find_package( Eigen3 REQUIRED )
include_directories( ${EIGEN3_INCLUDE_DIR} )

add_executable( example1 example1.cxx )
target_link_libraries( example1 )
