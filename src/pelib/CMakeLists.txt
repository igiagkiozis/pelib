
if(NOT TARGET pelib)
    file(GLOB PELIB_HEADERS "../../include/pelib/*.h")

	set(PELIB_SOURCES
		BoundImportDirectory.cpp
		CoffSymbolTable.cpp
		ComHeaderDirectory.cpp
		DebugDirectory.cpp
		ExportDirectory.cpp
		IatDirectory.cpp
		InputBuffer.cpp
		MzHeader.cpp
		OutputBuffer.cpp
		PeFile.cpp
		PeHeader.cpp
		PeLibAux.cpp
		RelocationsDirectory.cpp
		ResourceDirectory.cpp
		RichHeader.cpp
		SecurityDirectory.cpp
	)

	add_library(pelib STATIC ${PELIB_SOURCES} ${PELIB_HEADERS})
    source_group("Headers" FILES ${PELIB_HEADERS})
	target_include_directories(pelib SYSTEM PUBLIC ${PROJECT_SOURCE_DIR}/include/)

endif()
