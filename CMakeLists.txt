project( kissfft )

cmake_minimum_required( VERSION 2.8.11 )

set( LIBNAME kiss_fft )

add_library( ${LIBNAME} SHARED
	kiss_fft.c
)

install(
	FILES kiss_fft.h
	DESTINATION include
)

install(
	TARGETS ${LIBNAME}
	DESTINATION lib
)

