###############################################################################
#
# CMake configuration file to build libxtiff library
#
# Author: Mateusz Loskot <mateusz@loskot.net>
#
###############################################################################
ADD_LIBRARY( xtiff STATIC xtiff.c )

ADD_LIBRARY( xtiff_i SHARED xtiff.c )

TARGET_LINK_LIBRARIES( xtiff_i ${TIFF_LIBRARIES} )

INSTALL( TARGETS xtiff xtiff_i
	RUNTIME DESTINATION bin
	LIBRARY DESTINATION lib
	ARCHIVE DESTINATION lib )
