INCLUDE(test_macros)
INCLUDE_DIRECTORIES(${CMAKE_BINARY_DIR}/fem/src)

CONFIGURE_FILE( case.sif case.sif COPYONLY)

file(COPY ELMERSOLVER_STARTINFO mesh surfaceflat.geo DESTINATION "${CMAKE_CURRENT_BINARY_DIR}/")

ADD_ELMER_TEST(periodic3)
ADD_ELMER_LABEL(periodic3 quick)
