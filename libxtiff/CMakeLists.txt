###############################################################################
#
# CMake configuration file to build libxtiff library
#
# Author: Mateusz Loskot <mateusz@loskot.net>
#
###############################################################################

ADD_LIBRARY(xtiff STATIC xtiff.c)

INSTALL( TARGETS xtiff
	RUNTIME DESTINATION bin
	LIBRARY DESTINATION lib
	ARCHIVE DESTINATION lib )
