INCLUDE(test_macros)
INCLUDE_DIRECTORIES(${CMAKE_BINARY_DIR}/fem/src)

CONFIGURE_FILE( shellplate.sif shellplate.sif COPYONLY)

file(COPY ELMERSOLVER_STARTINFO plates DESTINATION "${CMAKE_CURRENT_BINARY_DIR}/")

ADD_ELMER_TEST(Shell_PlateCase_Quad LABELS quick)

