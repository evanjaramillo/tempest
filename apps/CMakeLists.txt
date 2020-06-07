MESSAGE( STATUS "Resolving apps ..." )

LISTDIRS( SUBDIRS ${CMAKE_CURRENT_SOURCE_DIR} )

FOREACH( subdir ${SUBDIRS} )

    MESSAGE( STATUS "Adding directory: ${subdir}" )
    ADD_SUBDIRECTORY( ${subdir} )

ENDFOREACH( )
