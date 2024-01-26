cmake_minimum_required(VERSION 3.16)

add_library(json STATIC
	src/json/json.cpp
	include/json/json.h
)

set(CMAKE_CXX_VISIBILITY_PRESET hidden)

target_include_directories(json
	PUBLIC
		./include/
		./include/json
)

include(GenerateExportHeader)
generate_export_header(json EXPORT_FILE_NAME ${CMAKE_CURRENT_SOURCE_DIR}/include/json/Exports.h)
