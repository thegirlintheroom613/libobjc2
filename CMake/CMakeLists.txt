cmake_minimum_required(VERSION 3.1)
project(test_cxx_runtime)

add_executable(test_cxx_runtime typeinfo_test.cc)
add_executable(test_cxx_stdlib typeinfo_test.cc)
if (CXX_RUNTIME)
	target_link_libraries(test_cxx_runtime ${CXX_RUNTIME})
	set_target_properties(test_cxx_runtime PROPERTIES
		LINKER_LANGUAGE C)
endif()
