PROJECT(librvm)

FILE(GLOB LIBRVM_SOURCE_FILES
    AddGroupBBox.cpp
    AddGroupBBox.h
    AddStats.cpp
    AddStats.h
    Align.cpp
    ChunkTiny.cpp
    ChunkTiny.h
    Colorizer.cpp
    Colorizer.h
    Common.cpp
    Common.h
    Connect.cpp
    DiscardGroups.cpp
    DumpNames.cpp
    DumpNames.h
    ExportJson.cpp
    ExportObj.cpp
    ExportObj.h
    Flatten.cpp
    Flatten.h
    LinAlg.h
    LinAlgOps.cpp
    LinAlgOps.h
    Parser.h
    ParserAtt.cpp
    ParserRVM.cpp
    Store.cpp
    Store.h
    StoreVisitor.h
    Tessellator.cpp
    Tessellator.h
    TriangulationFactory.cpp
    ../libtess2/Source/*.h
    ../libtess2/Source/*.c
    )

ADD_LIBRARY(librvm STATIC
    ${LIBRVM_SOURCE_FILES}
    )

target_include_directories(librvm PUBLIC 
    ../rapidjson/include
    ../libtess2/Include)

SET_PROPERTY(TARGET "librvm"  PROPERTY FOLDER "lib")
    