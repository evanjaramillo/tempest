MESSAGE( STATUS "Resolving 3rd party dependecies ..." )

LISTDIRS( SUBDIRS ${CMAKE_CURRENT_SOURCE_DIR} )

FOREACH( subdir ${SUBDIRS} )

    MESSAGE( STATUS "Adding directory: ${subdir}" )
    ADD_SUBDIRECTORY( ${subdir} )

ENDFOREACH( )
