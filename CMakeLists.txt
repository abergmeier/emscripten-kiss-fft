project( kissfft )

cmake_minimum_required( VERSION 2.8.11 )

set( LIBNAME kiss_fft )

add_library( ${LIBNAME} SHARED
	kiss_fft.c
	tools/kiss_fftr.c
)

target_include_directories( ${LIBNAME}
	PRIVATE
	${CMAKE_CURRENT_SOURCE_DIR}
)

install(
	FILES
		kiss_fft.h
		tools/kiss_fftr.h
	DESTINATION include
)

install(
	TARGETS ${LIBNAME}
	DESTINATION lib
)

