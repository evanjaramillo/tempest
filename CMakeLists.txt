CMAKE_MINIMUM_REQUIRED( VERSION 3.11...3.16 )

PROJECT( Tempest LANGUAGES C CXX )

##
## Set the path to the cmake modules:
##

SET( CMAKE_MODULE_PATH "${PROJECT_SOURCE_DIR}/cmake" ${CMAKE_MODULE_PATH} )

INCLUDE( ListDirs )

##
## Make sure that the code is built out of the source directory:
##

FILE( TO_CMAKE_PATH "${PROJECT_BINARY_DIR}/CMakeLists.txt" LOC_PATH )

IF( EXISTS "${LOC_PATH}" )

	MESSAGE( FATAL_ERROR "This project requires out of source builds. Make a build dir." )

ENDIF( )

##
## Add dependencies
##

ADD_SUBDIRECTORY( extern/ )

##
## Add core library
##

ADD_SUBDIRECTORY( lib/ )

##
## Add apps
##

ADD_SUBDIRECTORY( apps/ )

