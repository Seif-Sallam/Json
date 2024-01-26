cmake_minimum_required(VERSION 3.16)

add_executable(playground
	main.cpp
)

target_link_libraries(playground
	PRIVATE
	json)