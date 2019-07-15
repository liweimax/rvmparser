INCLUDE_DIRECTORIES( ${librvm_SOURCE_DIR}/src )
ADD_EXECUTABLE(rvmparser main.cpp)
TARGET_LINK_LIBRARIES(rvmparser librvm)
